---
Description: Ruft den DWORD-Wert für die angegebene TagID ab.
ms.assetid: 6610e101-9068-4812-b0ca-528658b62535
title: Sdbreaddwordtag-Funktion
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
ms.openlocfilehash: 0f1f7acc113bc40388d62927b6d98f8ff7bdebf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105927"
---
# <a name="sdbreaddwordtag-function"></a>Sdbreaddwordtag-Funktion

Ruft den **DWORD** -Wert für die angegebene **TagID** ab.

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

*PDB* \[ in\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> <dt>

*tiwhat* \[ in\]
</dt> <dd>

Die **TagID** , die den abzurufenden Daten entspricht.

</dd> <dt>

*dwdefault* \[ in\]
</dt> <dd>

Der Standardwert, der bei einem Fehler zurückgegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt bei einem Fehler den Wert bei Erfolg oder *dwdefault* zurück.

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

[**Sdbreadqwordtag**](sdbreadqwordtag.md)
</dt> <dt>

[**Sdbreadstringtag**](sdbreadstringtag.md)
</dt> </dl>

 

 




