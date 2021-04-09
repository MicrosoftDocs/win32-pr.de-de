---
description: Sucht im angegebenen übergeordneten Element nach der nächsten tagübereinstimmung und gibt die TagID der Übereinstimmung zurück.
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: Sdbfindnexttag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a5baf728a75e4c02c20ed4207b7d6b9a968af1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860892"
---
# <a name="sdbfindnexttag-function"></a>Sdbfindnexttag-Funktion

Sucht im angegebenen übergeordneten Element nach der nächsten tagübereinstimmung und gibt die **TagID** der Übereinstimmung zurück.

## <a name="syntax"></a>Syntax


```C++
TAGID WINAPI SdbFindNextTag(
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

Die **TagID** der vorherigen Übereinstimmung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **TagID** der Entsprechung.

## <a name="remarks"></a>Bemerkungen

Bevor Sie diese Funktion aufrufen, rufen Sie die [**sdbfindfirsttag**](sdbfindfirsttag.md) -Funktion auf.

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

[**Sdbtagrebtotagid**](sdbtagreftotagid.md)
</dt> </dl>

 

 




