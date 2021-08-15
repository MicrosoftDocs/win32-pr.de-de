---
description: Löscht eine vorhandene Instanz einer Klasse aus dem Repository.
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma deleteinstance
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
ms.openlocfilehash: 29739f1d95cf5c8352c2b7822dbc3da7777f41f69fc5086631e0069c3b832623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316844"
---
# <a name="pragma-deleteinstance"></a>pragma deleteinstance

Der **Befehl pragma deleteinstance** löscht eine vorhandene Instanz einer Klasse aus dem Repository.

Im Folgenden wird die Syntax für diesen Befehl beschrieben:


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



*InstanceId* ist ein eindeutiger Bezeichner der Instanz, die der MOF-Compiler aus dem aktuellen Namespace löscht.

*\[ Das \] Flag* muss eines der folgenden Argumente sein.



| Flag   | Beschreibung                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| fehlerhaft   | Bewirkt, dass der MOF-Compiler mit einer Fehlermeldung beendet wird, wenn die Klasse nicht bereits im Repository vorhanden ist. |
| nofail | Bewirkt, dass der MOF-Compiler fortgesetzt wird, auch wenn die Klasse noch nicht vorhanden ist.                                |



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung dieses Befehls veranschaulicht.


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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 




