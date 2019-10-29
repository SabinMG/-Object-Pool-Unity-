Object Pool (Unity)
=================

An object pool implementation for Unity.

Overview
----
Object pooling helps to avoid memmory foot print issues while creating new objects dynamically. Here you will find the implementation of the
object pool inside the unity.

Usage
----
1. Create an empty gameObject in the scene. Name it as "PoolInitializer".
2. Add the component PoolInitializer.cs to it.
3. Rezise the Objects To Pooled array.
4. Assigne the prefab to the array.
5. Also assigne the pool max size as well.


```csharp
//Spawn pooled objects
void CreatEnemy(string enemyName, Vector3 position, Quaternion rotation)
{
          GameObject enemy = poolManager.Instance.GetObjectFromPool(enemyName, position, rotation);	
}

void RecycleEnemy()
{
        poolManager.Instance.PutObjectBacktoPool(GameObject enemyGO)
}

```

Licence
---
MIT
