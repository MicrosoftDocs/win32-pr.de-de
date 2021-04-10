---
description: Schreibt einen NULL-Eintrag in die angegebene Datenbank.
ms.assetid: 2a29389b-d4f6-4527-a429-c9459b095f2f
title: Sdbschreitenulltag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteNULLTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 662d5c4db31f199df8b3b9f7368aba118ea6e8fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214095"
---
# <a name="sdbwritenulltag-function"></a>Sdbschreitenulltag-Funktion

Schreibt einen **null** -Eintrag in die angegebene Datenbank.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbWriteNULLTag(
  _In_ PDB pdb,
  _In_ TAG tTag
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

Das-Tag für den Eintrag. Dieses Tag muss vom Typ " **\_ Tagtyp \_ null**" sein.

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

 

 




