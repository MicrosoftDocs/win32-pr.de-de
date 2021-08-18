---
description: Sucht innerhalb des angegebenen übergeordneten Elements nach einem untergeordneten TAG und gibt die TAGID des ersten untergeordneten Elements zurück.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: SdbGetFirstChild-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 58e63b3c1c8b3e56c9610ec795c1706fe58990e4611c36886ee4a3061d0816fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075974"
---
# <a name="sdbgetfirstchild-function"></a>SdbGetFirstChild-Funktion

Sucht innerhalb des angegebenen übergeordneten Elements nach einem untergeordneten TAG und gibt die **TAGID** des ersten untergeordneten Elements zurück.

## <a name="syntax"></a>Syntax


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdb* \[ In\]
</dt> <dd>

Ein Handle für die Shim-Datenbank.

</dd> <dt>

*tiParent* \[ In\]
</dt> <dd>

Die **TAGID** des Suchstarts. Dieser Parameter kann **TAGID \_ ROOT** oder **TAG TYPE \_ \_ LIST** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **TAGID** des ersten untergeordneten Oder **TAGID \_ NULL** ist kein untergeordnetes Element wurde gefunden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbGetNextChild**](sdbgetnextchild.md)
</dt> </dl>

 

 




