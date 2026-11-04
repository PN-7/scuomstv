# Real GitHub download test

Requires Maple2Patcher 1.1.0 locally. Extract the v1 release asset `test-client-baseline.zip` to a new empty folder.

```powershell
Maple2Patcher.exe update D:/PatcherTest ./tests/version-1-config.json
Maple2Patcher.exe verify D:/PatcherTest
Maple2Patcher.exe update D:/PatcherTest ./patcher-config.json
Maple2Patcher.exe verify D:/PatcherTest
```

After the first update, `Demo/settings.txt` is `version=1`. After the second it is `version=3`. The common text file is unchanged and must not be downloaded or rewritten during 1->3. Repeating the latest update must not download payloads. `restore D:/PatcherTest` returns 3->1, and repeating restore returns to the original test baseline.

Do not point this test configuration at a real game installation. No dye/outfit patch is included.
