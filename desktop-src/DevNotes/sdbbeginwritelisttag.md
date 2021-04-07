---
description: Erstellt ein neues listentag für Schreibvorgänge.
ms.assetid: 3a52e2f2-9648-45fb-b487-ccfe5ed24f7f
title: Sdbbeginschreitelisttag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbBeginWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a9dcf6bdd3798b18e08b796eb268f93dc4ec6bbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748745"
---
# <a name="sdbbeginwritelisttag-function"></a>Sdbbeginschreitelisttag-Funktion

Erstellt ein neues listentag für Schreibvorgänge.

## <a name="syntax"></a>Syntax


```C++
TAGID WINAPI SdbBeginWriteListTag(
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

Das-Tag für den neuen Eintrag. Dieser Wert muss vom Typ " **\_ Tagtyp \_ Liste**" sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt bei einem Fehler die [**TagID**](tagid.md) der neuen Liste bei Erfolg oder **TagID \_ null** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbclosedatabase**](sdbclosedatabase.md)
</dt> <dt>

[**Sdbclosedatabasewrite**](sdbclosedatabasewrite.md)
</dt> <dt>

[**Sdbendschreitelisttag**](sdbendwritelisttag.md)
</dt> <dt>

[**Tag**](tag.md)
</dt> <dt>

[Tagtypen](tag-types.md)
</dt> <dt>

[**TagID**](tagid.md)
</dt> </dl>

 

 




