---
description: Sucht das nächste untergeordnete Tag innerhalb des angegebenen übergeordneten Elements und gibt die TagID des nächsten untergeordneten Elements zurück.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: Sdbgetnextchild-Funktion
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
ms.openlocfilehash: 4f2943eaf0baec84a9473b679743b9eafad3b7fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861048"
---
# <a name="sdbgetnextchild-function"></a>Sdbgetnextchild-Funktion

Sucht das nächste untergeordnete Tag innerhalb des angegebenen übergeordneten Elements und gibt die **TagID** des nächsten untergeordneten Elements zurück.

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

*PDB* \[ in\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> <dt>

*tiparent* \[ in\]
</dt> <dd>

Die **TagID** des Such Starts. Dieser Parameter kann eine **TagID \_** -Stamm-oder **\_ Tagtyp \_ Liste** sein.

</dd> <dt>

*tiprev* \[ in\]
</dt> <dd>

Die **TagID** des vorherigen untergeordneten Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **TagID** des untergeordneten Elements oder der **TagID \_ null** , wenn kein untergeordnetes Element gefunden wurde.

## <a name="remarks"></a>Bemerkungen

Bevor Sie diese Funktion aufrufen, rufen Sie die [**sdbgetfirstchild**](sdbgetfirstchild.md) -Funktion auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbfindfirsttag**](sdbfindfirsttag.md)
</dt> <dt>

[**Sdbfindnexttag**](sdbfindnexttag.md)
</dt> <dt>

[**Sdbgetfirstchild**](sdbgetfirstchild.md)
</dt> </dl>

 

 




