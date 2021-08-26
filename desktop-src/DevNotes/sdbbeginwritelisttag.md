---
description: Erstellt ein neues Listentag für Schreibvorgänge.
ms.assetid: 3a52e2f2-9648-45fb-b487-ccfe5ed24f7f
title: SdbBeginWriteListTag-Funktion
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
ms.openlocfilehash: 448b57e73bec0115d4c2ae87be96630cad6542833da66a2de8e02037c264de83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058580"
---
# <a name="sdbbeginwritelisttag-function"></a>SdbBeginWriteListTag-Funktion

Erstellt ein neues Listentag für Schreibvorgänge.

## <a name="syntax"></a>Syntax


```C++
TAGID WINAPI SdbBeginWriteListTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdb* \[ In\]
</dt> <dd>

Ein Handle für die Shim-Datenbank.

</dd> <dt>

*tTag* \[ In\]
</dt> <dd>

Das TAG für den neuen Eintrag. Dieser Wert muss vom Typ **\_ \_ TAGTYPLISTE** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt die [**TAGID**](tagid.md) der neuen Liste bei Erfolg oder **TAGID \_ NULL** bei einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbCloseDatabase**](sdbclosedatabase.md)
</dt> <dt>

[**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
</dt> <dt>

[**SdbEndWriteListTag**](sdbendwritelisttag.md)
</dt> <dt>

[**Etikett**](tag.md)
</dt> <dt>

[TAG-Typen](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




