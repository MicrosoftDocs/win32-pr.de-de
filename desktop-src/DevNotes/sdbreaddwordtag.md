---
Description: Ruft den DWORD-Wert für die angegebene TAGID ab.
ms.assetid: 6610e101-9068-4812-b0ca-528658b62535
title: SdbReadDWORDTag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4ce168aab7755dcd11f145caf44678a489bca152753ea010edbd7387b3e730f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044950"
---
# <a name="sdbreaddwordtag-function"></a>SdbReadDWORDTag-Funktion

Ruft den **DWORD-Wert** für die angegebene **TAGID** ab.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI SdbReadDWORDTag(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich,
  _In_ DWORD dwDefault
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

</dd> <dt>

*dwDefault* \[ In\]
</dt> <dd>

Der Standardwert, der bei einem Fehler zurückgegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt den Wert bei Erfolg oder *dwDefault* bei einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
</dt> <dt>

[**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
</dt> <dt>

[**SdbReadQWORDTag**](sdbreadqwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 




