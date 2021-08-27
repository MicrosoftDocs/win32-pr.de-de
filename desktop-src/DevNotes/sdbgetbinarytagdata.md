---
description: Ruft die Binärdaten für die angegebene TAGID ab.
ms.assetid: 18992406-67b4-4c48-9629-04d6bf1c5824
title: SdbGetBinaryTagData-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetBinaryTagData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5bb2155c7fe2ff1ae2d9784777e39740e5b3224cfc60881fbe0d961ddb422360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058520"
---
# <a name="sdbgetbinarytagdata-function"></a>SdbGetBinaryTagData-Funktion

Ruft die Binärdaten für die angegebene **TAGID** ab.

## <a name="syntax"></a>Syntax


```C++
PVOID WINAPI SdbGetBinaryTagData(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdb* \[ In\]
</dt> <dd>

Ein Handle für die Shim-Datenbank.

</dd> <dt>

*tiWhich* \[ In\]
</dt> <dd>

Die **TAGID,** die den abzurufenden Daten entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt einen Zeiger auf die Binärdaten oder **NULL** zurück, wenn die **TAGID** ungültig ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> <dt>

[**SdbReadQWORDTag**](sdbreadqwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 




