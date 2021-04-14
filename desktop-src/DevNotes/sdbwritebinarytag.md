---
description: Schreibt Binärdaten in die angegebene Datenbank.
ms.assetid: 935321b8-904e-46be-ad11-77d89670a072
title: Sdbschreitebinarytag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e79de8549eb4c0a0f1b8a914c59d21ccfb3bcf7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523323"
---
# <a name="sdbwritebinarytag-function"></a>Sdbschreitebinarytag-Funktion

Schreibt Binärdaten in die angegebene Datenbank.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbWriteBinaryTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ PBYTE pBuffer,
  _In_ DWORD dwSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDB* \[ in\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> <dt>

*ttag* \[ in\]
</dt> <dd>

Das-Tag für den Eintrag. Dieses Tag muss vom Typ " **Tag \_ Type \_ Binary**" sein.

</dd> <dt>

*pbuffer* \[ in\]
</dt> <dd>

Der Puffer, der die Daten enthält. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*dwSize* \[ in\]
</dt> <dd>

Die Größe des *pbuffer* -Puffers in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei einem Fehler gibt die Funktion **true** oder **false** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbschreitebinarytagfromfile**](sdbwritebinarytagfromfile.md)
</dt> <dt>

[**Sdbschreitedwordtag**](sdbwritedwordtag.md)
</dt> <dt>

[**Sdbschreiteqwordtag**](sdbwriteqwordtag.md)
</dt> <dt>

[**Sdbschreitestringtag**](sdbwritestringtag.md)
</dt> <dt>

[**Sdbschreitewordtag**](sdbwritewordtag.md)
</dt> </dl>

 

 




