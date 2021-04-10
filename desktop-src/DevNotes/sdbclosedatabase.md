---
description: Schließt die angegebene Shimdatenbank.
ms.assetid: e4480860-8055-4134-b6ed-926c010d462f
title: Sdbclosedatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 376d97b8386f127a945cb118639be1e38ae68737
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041421"
---
# <a name="sdbclosedatabase-function"></a>Sdbclosedatabase-Funktion

Schließt die angegebene Shimdatenbank.

## <a name="syntax"></a>Syntax


```C++
void WINAPI SdbCloseDatabase(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDB* \[ in, out\]
</dt> <dd>

Ein Handle für die Shimdatenbank. Dieser Parameter darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbopendatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




