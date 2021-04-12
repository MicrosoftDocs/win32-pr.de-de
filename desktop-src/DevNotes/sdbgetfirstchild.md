---
description: Sucht nach einem untergeordneten Tag innerhalb des angegebenen übergeordneten Elements und gibt die TagID des ersten untergeordneten Elements zurück.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: Sdbgetfirstchild-Funktion
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
ms.openlocfilehash: abc06ae0e4b5d842a968d0f3fbeb7a15702660b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522803"
---
# <a name="sdbgetfirstchild-function"></a>Sdbgetfirstchild-Funktion

Sucht nach einem untergeordneten Tag innerhalb des angegebenen übergeordneten Elements und gibt die **TagID** des ersten untergeordneten Elements zurück.

## <a name="syntax"></a>Syntax


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
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

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **TagID** des ersten untergeordneten Elements oder **TagID \_ null** ist kein untergeordnetes Element wurde gefunden.

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

[**Sdbgetnextchild**](sdbgetnextchild.md)
</dt> </dl>

 

 




