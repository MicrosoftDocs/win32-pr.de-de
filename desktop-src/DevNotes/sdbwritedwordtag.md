---
description: Schreibt einen DWORD-Wert in die angegebene Datenbank.
ms.assetid: 2ecbfcac-5bb1-4129-9501-79210672aa1b
title: Sdbschreitedwordtag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5b549a91037aa308b5b88d0e3e2a51e153002bd5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214096"
---
# <a name="sdbwritedwordtag-function"></a>Sdbschreitedwordtag-Funktion

Schreibt einen **DWORD** -Wert in die angegebene Datenbank.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbWriteDWORDTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ DWORD dwData
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

Das-Tag für den Eintrag. Dieses Tag muss den Typ " **Tag \_ Type \_ DWORD**" aufweisen.

</dd> <dt>

*dwdata* \[ in\]
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

[**Sdbschreiteqwordtag**](sdbwriteqwordtag.md)
</dt> <dt>

[**Sdbschreitestringtag**](sdbwritestringtag.md)
</dt> <dt>

[**Sdbschreitewordtag**](sdbwritewordtag.md)
</dt> </dl>

 

 




