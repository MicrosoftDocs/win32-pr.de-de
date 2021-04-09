---
Description: Ruft die Zeichenfolge für die angegebene TagID ab.
ms.assetid: d67d386d-a2c5-46e2-8887-9ee20ea427f9
title: Sdbreadstringtag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3f368d66e0fbc144a46683a04655cd7f650c3bce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957089"
---
# <a name="sdbreadstringtag-function"></a>Sdbreadstringtag-Funktion

Ruft die Zeichenfolge für die angegebene **TagID** ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbReadStringTag(
  _In_  PDB    pdb,
  _In_  TAGID  tiWhich,
  _Out_ LPTSTR pwszBuffer,
  _In_  DWORD  cchBufferSize
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

*pwszbuffer* \[ vorgenommen\]
</dt> <dd>

Der Puffer, der die Zeichenfolge empfängt. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*cchbuffersize* \[ in\]
</dt> <dd>

Die Größe des *pwszbuffer* -Puffers in Zeichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei einem Fehler gibt die Funktion **true** oder **false** zurück.

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

[**Sdbreadbinarytag**](sdbreadbinarytag.md)
</dt> <dt>

[**Sdbreaddwordtag**](sdbreaddwordtag.md)
</dt> </dl>

 

 




