---
Description: Ruft die Binärdaten für die angegebene TagID ab.
ms.assetid: b349f2af-2505-4efc-bd59-203f7666ce61
title: Sdbreadbinarytag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 024b432c3210b98721a0cf3058bad0f765287fde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337929"
---
# <a name="sdbreadbinarytag-function"></a>Sdbreadbinarytag-Funktion

Ruft die Binärdaten für die angegebene **TagID** ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbReadBinaryTag(
  _In_  PDB   pdb,
  _In_  TAGID tiWhich,
  _Out_ PBYTE pBuffer,
  _In_  DWORD dwBufferSize
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

*pbuffer* \[ vorgenommen\]
</dt> <dd>

Der Puffer, der die Binärdaten empfängt. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*dwbuffersize* \[ in\]
</dt> <dd>

Die Größe des *pbuffer* -Puffers in Bytes.

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

[**Sdbreaddwordtag**](sdbreaddwordtag.md)
</dt> <dt>

[**Sdbreadstringtag**](sdbreadstringtag.md)
</dt> </dl>

 

 




