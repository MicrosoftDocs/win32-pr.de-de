---
description: Löscht eine vorhandene Klasse und deren Instanzen aus dem Repository.
ms.assetid: 6f96d14a-16ab-4e83-a75f-5dbf162d1692
ms.tgt_platform: multiple
title: pragma deleteclass
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
ms.openlocfilehash: 0d3b5b1fa209be7fd472a87aec25a5e590d93c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868591"
---
# <a name="pragma-deleteclass"></a>pragma deleteclass

Der **pragma deleteclass** -Präprozessorbefehl löscht eine vorhandene Klasse und deren Instanzen aus dem Repository.

Im folgenden wird die Syntax beschrieben:


```mof
#pragma deleteclass("ClassName", [Flag])
```



*ClassName* ist der Name der Klasse, die der MOF-Compiler aus dem aktuellen Namespace löscht.

Das *\[ Flag \]* muss eines der folgenden Argumente aufweisen.



| Flag   | Beschreibung                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| fehlerhaft   | Bewirkt, dass der MOF-Compiler mit einer Fehlermeldung beendet wird, wenn die Klasse nicht bereits im Repository vorhanden ist. |
| "nofail" | Bewirkt, dass der MOF-Compiler fortgesetzt wird, auch wenn die Klasse nicht bereits vorhanden ist.                                |



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie dieser Befehl verwendet wird.


```mof
#pragma deleteclass("MyClass1",FAIL)
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

 

 




