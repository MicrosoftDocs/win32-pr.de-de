---
description: Bestimmt, ob die angegebene Datenbank eine der Standard Datenbanken (sysmain, AppHelp, drvmain oder msimain) ist.
ms.assetid: 7d7e3ca7-535e-40b3-b635-299eff8abea5
title: Sdbisstandarddatabase-Funktion
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
ms.openlocfilehash: 9e9e445162c2bfc171ccf975981876f81a8bb804
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041325"
---
# <a name="sdbisstandarddatabase-function"></a>Sdbisstandarddatabase-Funktion

Bestimmt, ob die angegebene Datenbank eine der Standard Datenbanken (sysmain, AppHelp, drvmain oder msimain) ist.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbIsStandardDatabase(
  _In_ GUID GuidDB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Guiddb* \[ in\]
</dt> <dd>

Die GUID für die Datenbank.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **true** zurück, wenn die GUID eine Standarddatenbank darstellt, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




