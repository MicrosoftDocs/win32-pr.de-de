---
description: Bestimmt, ob die angegebene Datenbank eine der Standarddatenbanken (Sysmain, Apphelp, Drvmain oder Msimain) ist.
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: SdbIsStandardDatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbIsStandardDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7ef30f54b4d8eb4df4d8f136de6357a072cdb0183f462cb3af8a9340ce68b0c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045190"
---
# <a name="sdbisstandarddatabase-function"></a>SdbIsStandardDatabase-Funktion

Bestimmt, ob die angegebene Datenbank eine der Standarddatenbanken (Sysmain, Apphelp, Drvmain oder Msimain) ist.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*GuidDB* \[ In\]
</dt> <dd>

Die GUID für die Datenbank.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **TRUE zurück,** wenn die GUID eine Standarddatenbank darstellt, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




