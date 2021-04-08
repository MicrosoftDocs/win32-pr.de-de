---
description: Schreibt einen QWORD-Wert in die angegebene Datenbank.
ms.assetid: 8ce566ea-a941-45fa-b031-26c3144ca02c
title: Sdbschreiteqwordtag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 58dcaad3487bb1f59a75dd6a671ecb43c9cf1751
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748089"
---
# <a name="sdbwriteqwordtag-function"></a>Sdbschreiteqwordtag-Funktion

Schreibt einen **QWORD** -Wert in die angegebene Datenbank.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbWriteQWORDTag(
  _In_ PDB       pdb,
  _In_ TAG       tTag,
  _In_ ULONGLONG qwData
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

Das-Tag für den Eintrag. Dieses Tag muss den Typ " **\_ Tagtyp \_ QWORD**" aufweisen.

</dd> <dt>

*qwdata* \[ in\]
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

[**Sdbschreitestringtag**](sdbwritestringtag.md)
</dt> <dt>

[**Sdbschreitewordtag**](sdbwritewordtag.md)
</dt> </dl>

 

 




