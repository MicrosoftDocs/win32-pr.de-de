---
description: Sucht eine tagübereinstimmung innerhalb des angegebenen übergeordneten Elements und gibt die TagID der ersten Übereinstimmung zurück.
ms.assetid: ecbe216c-1e46-4472-b1d1-e2ac7ace82ab
title: Sdbfindfirsttag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: dc8b752d536be83d90ded55474166d14521f0f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958121"
---
# <a name="sdbfindfirsttag-function"></a>Sdbfindfirsttag-Funktion

Sucht eine tagübereinstimmung innerhalb des angegebenen übergeordneten Elements und gibt die **TagID** der ersten Übereinstimmung zurück.

## <a name="syntax"></a>Syntax


```C++
TAGID WINAPI SdbFindFirstTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAG   tTag
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

*ttag* \[ in\]
</dt> <dd>

Das Tag, das abgeglichen werden soll. Eine Liste möglicher Werte finden Sie unter [Tag](tag.md) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **TagID** der ersten Übereinstimmung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbfindnexttag**](sdbfindnexttag.md)
</dt> <dt>

[**Sdbtagrebtotagid**](sdbtagreftotagid.md)
</dt> </dl>

 

 




