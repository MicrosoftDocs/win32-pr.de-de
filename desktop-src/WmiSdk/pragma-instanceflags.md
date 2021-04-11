---
description: Steuert die Art und Weise, in der Instanzen abhängig von den angegebenen Flags erstellt oder aktualisiert werden.
ms.assetid: 9932edf2-2e5f-4c5e-9889-f2be4af11bf2
ms.tgt_platform: multiple
title: pragma instanceflags
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: acc05e201fcf153ab2156d4a360ce36b4539cd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218314"
---
# <a name="pragma-instanceflags"></a>pragma instanceflags

Der **pragma instanceflags** -Präprozessorbefehl steuert die Art und Weise, in der Instanzen abhängig von den angegebenen Flags erstellt oder aktualisiert werden.

Im folgenden wird die Syntax beschrieben:


```mof
#pragma instanceflags ([Flag])
```



Das *\[ Flag \]* muss eines der folgenden Argumente aufweisen.



| Flag       | Beschreibung                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| createonly | Verhindert, dass der Compiler vorhandene Instanzen in der MOF-Datei ändert.                                |
| updateonly | Verhindert, dass der Compiler neue Instanzen erstellt, wenn eine Instanz, die in der MOF-Datei angegeben ist, nicht vorhanden ist. |



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie dieser Befehl verwendet wird.


```mof
#pragma instanceflags("createonly")
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 




