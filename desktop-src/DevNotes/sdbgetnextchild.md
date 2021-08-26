---
description: Sucht innerhalb des angegebenen übergeordneten Elements nach dem nächsten untergeordneten TAG und gibt die TAGID des nächsten untergeordneten Elements zurück.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: SdbGetNextChild-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 210e0aab8cb5e43bfc649e8abb72cf565c4d4f892f651708286f7a3f87d11ce2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045311"
---
# <a name="sdbgetnextchild-function"></a>SdbGetNextChild-Funktion

Sucht innerhalb des angegebenen übergeordneten Elements nach dem nächsten untergeordneten TAG und gibt die **TAGID** des nächsten untergeordneten Elements zurück.

## <a name="syntax"></a>Syntax


```C++
TAGID WINAPI SdbGetNextChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
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

Die **TAGID** des Suchstarts. Dieser Parameter kann **TAGID \_ ROOT oder** **TAG TYPE LIST \_ \_ sein.**

</dd> <dt>

*tiPrev* \[ In\]
</dt> <dd>

Die **TAGID** des vorherigen untergeordneten -

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **TAGID des** untergeordneten Oder **TAGID \_ NULL,** wenn kein untergeordnetes Objekt gefunden wird.

## <a name="remarks"></a>Hinweise

Rufen Sie vor dem Aufrufen dieser Funktion die [**SdbGetFirstChild-Funktion**](sdbgetfirstchild.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbGetFirstChild**](sdbgetfirstchild.md)
</dt> </dl>

 

 




