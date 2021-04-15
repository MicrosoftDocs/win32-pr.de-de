---
Description: Ruft den QWORD-Wert für die angegebene TagID ab.
ms.assetid: 5fa94a95-c7f3-477b-ab7c-931e8d62d501
title: Sdbreadqwordtag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 15227f3d7c3177a226f1b3cc77fc78efd34379d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392182"
---
# <a name="sdbreadqwordtag-function"></a>Sdbreadqwordtag-Funktion

Ruft den **QWORD** -Wert für die angegebene **TagID** ab.

## <a name="syntax"></a>Syntax


```C++
ULONGLONG WINAPI SdbReadQWORDTag(
  _In_ PDB       pdb,
  _In_ TAGID     tiWhich,
  _In_ ULONGLONG qwDefault
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDB* \[ in\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> <dt>

*tiwhat* \[ in\]
</dt> <dd>

Die **TagID** , die den abzurufenden Daten entspricht.

</dd> <dt>

*qwdefault* \[ in\]
</dt> <dd>

Der Standardwert, der bei einem Fehler zurückgegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt bei einem Fehler den Wert bei Erfolg oder *qwdefault* zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbgetbinarytagdata**](sdbgetbinarytagdata.md)
</dt> <dt>

[**Sdbgetstringtagptr**](sdbgetstringtagptr.md)
</dt> <dt>

[**Sdbreaddwordtag**](sdbreaddwordtag.md)
</dt> <dt>

[**Sdbreadstringtag**](sdbreadstringtag.md)
</dt> </dl>

 

 




