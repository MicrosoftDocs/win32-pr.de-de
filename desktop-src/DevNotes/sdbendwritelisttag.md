---
description: Beendet die Schreibvorgänge für die angegebene Liste.
ms.assetid: 318aa5dc-b562-47f8-8cd6-daa97f28c0f0
title: Sdbendschreitelisttag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbEndWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f5f203e3b643fcae174eae3634b5d337a0d7276a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344583"
---
# <a name="sdbendwritelisttag-function"></a>Sdbendschreitelisttag-Funktion

Beendet die Schreibvorgänge für die angegebene Liste.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbEndWriteListTag(
  _Inout_ PDB   pdb,
  _In_    TAGID tiList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDB* \[ in, out\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> <dt>

*tilist* \[ in\]
</dt> <dd>

Die [**TagID**](tagid.md) der Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei einem Fehler gibt die Funktion **true** oder **false** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion nach dem Schreiben aller Listeneinträge aufzurufen. das Ende der Liste wird markiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbbeginschreitelisttag**](sdbbeginwritelisttag.md)
</dt> <dt>

[**Sdbclosedatabase**](sdbclosedatabase.md)
</dt> <dt>

[**Sdbclosedatabasewrite**](sdbclosedatabasewrite.md)
</dt> </dl>

 

 




