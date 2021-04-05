---
description: Löscht eine vorhandene Instanz einer Klasse aus dem Repository.
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma Delta einstance
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
ms.openlocfilehash: 10d4c735f1e59533b57ae1814cfb8e36b2c1ad76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041889"
---
# <a name="pragma-deleteinstance"></a>pragma Delta einstance

Der **pragma-Delta** Befehl löscht eine vorhandene Instanz einer Klasse aus dem Repository.

Im folgenden wird die Syntax für diesen Befehl beschrieben:


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



*InstanceId* ist ein eindeutiger Bezeichner der Instanz, die der MOF-Compiler aus dem aktuellen Namespace löscht.

Das *\[ Flag \]* muss eines der folgenden Argumente aufweisen.



| Flag   | Beschreibung                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| fehlerhaft   | Bewirkt, dass der MOF-Compiler mit einer Fehlermeldung beendet wird, wenn die Klasse nicht bereits im Repository vorhanden ist. |
| "nofail" | Bewirkt, dass der MOF-Compiler fortgesetzt wird, auch wenn die Klasse nicht bereits vorhanden ist.                                |



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie dieser Befehl verwendet wird.


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
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

 

 




