# 游戏内Sweep and Prune系统

## 项目描述

游戏内Sweep and Prune系统的bug修复项目。核心模块 `collision/sap.py` 存在多个已知bug，需要修复后使测试全部通过。

## 已知问题

- 宽相碰撞完全没做宽相碰撞是O(n²)
- 排序轴完全没做不能排序轴
- 重叠对完全没做不能管理重叠对
- 增量更新完全没做不能增量更新
- SAP性能完全没做不能优化SAP性能

## 运行测试

```bash
python -m pytest tests/test_sap.py -q
```

修复目标：所有 14 个测试全部通过。

## 技术要求

- 纯Python标准库，不引入第三方依赖
- 不修改测试文件
- 保持现有API接口不变
