---
description: Löscht eine vorhandene Klasse und ihre Instanzen aus dem Repository.
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
ms.openlocfilehash: 3cb62c9d90d5ac6346e25eaa3c254e0c6dd595805ec6901376ce9dccdf648289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996290"
---
# <a name="pragma-deleteclass"></a>pragma deleteclass

Der **Pragma deleteclass-Präprozessorbefehl** löscht eine vorhandene Klasse und ihre Instanzen aus dem Repository.

Im Folgenden wird die Syntax beschrieben:


```mof
#pragma deleteclass("ClassName", [Flag])
```



*ClassName* ist der Name der Klasse, die der MOF-Compiler aus dem aktuellen Namespace löscht.

*\[ Das \] Flag* muss eines der folgenden Argumente sein.



| Flag   | Beschreibung                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| fehlerhaft   | Bewirkt, dass der MOF-Compiler mit einer Fehlermeldung beendet wird, wenn die Klasse nicht bereits im Repository vorhanden ist. |
| nofail | Bewirkt, dass der MOF-Compiler fortgesetzt wird, auch wenn die Klasse noch nicht vorhanden ist.                                |



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung dieses Befehls veranschaulicht.


```mof
#pragma deleteclass("MyClass1",FAIL)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 




