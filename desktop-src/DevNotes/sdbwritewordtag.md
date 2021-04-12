---
description: Schreibt einen Word-Wert in die angegebene Datenbank.
ms.assetid: 8f921e14-4a82-4d8e-83fa-beb78118ecb8
title: Sdbschreitewordtag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75a5b3eb430901de36d5aca325f928aae266bc39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523315"
---
# <a name="sdbwritewordtag-function"></a>Sdbschreitewordtag-Funktion

Schreibt einen **Word** -Wert in die angegebene Datenbank.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbWriteWORDTag(
  _In_ PDB  pdb,
  _In_ TAG  tTag,
  _In_ WORD wData
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

Das-Tag für den Eintrag. Dieses Tag muss vom Typ " **\_ Tagtyp \_ Wort**" sein.

</dd> <dt>

*wdata* \[ in\]
</dt> <dd>

Der Wert.

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

[**Sdbschreitebinarytag**](sdbwritebinarytag.md)
</dt> <dt>

[**Sdbschreitedwordtag**](sdbwritedwordtag.md)
</dt> <dt>

[**Sdbschreiteqwordtag**](sdbwriteqwordtag.md)
</dt> <dt>

[**Sdbschreitestringtag**](sdbwritestringtag.md)
</dt> </dl>

 

 




