---
title: MirrorIcon-Funktion
description: Kehrt Symbole (Spiegelungen) um, sodass sie ordnungsgemäß in einem gespiegelten Gerätekontext angezeigt werden.
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- MirrorIcon-Windows Steuerelemente
topic_type:
- apiref
api_name:
- MirrorIcon
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e597c344b5499272778ced3ff4cc2269fd7685ba6f554568c8493a6f65826bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078944"
---
# <a name="mirroricon-function"></a>MirrorIcon-Funktion

\[**MirrorIcon** ist über Windows XP mit Service Pack 2 (SP2) verfügbar. Sie kann in nachfolgenden Versionen geändert oder nicht verfügbar sein.\]

Kehrt Symbole (Spiegelungen) um, sodass sie ordnungsgemäß in einem gespiegelten Gerätekontext angezeigt werden.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phIconSmall* \[ in, out, optional\]
</dt> <dd>

Typ: **[ **HICON**](/windows/desktop/WinProg/windows-data-types)\***

Ein Zeiger auf das Symbolhand handle, das auf eine kleine Version eines Symbols verweist.

</dd> <dt>

*phIconLarge* \[ in, out, optional\]
</dt> <dd>

Typ: **[ **HICON**](/windows/desktop/WinProg/windows-data-types)\***

Ein Zeiger auf das Symbolhand handle, das auf eine große Version eines Symbols verweist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE,** wenn erfolgreich; andernfalls **FALSE**.

## <a name="remarks"></a>Hinweise

**MirrorIcon** wird nicht nach Namen exportiert oder in einer öffentlichen Headerdatei deklariert. Um sie zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden und die Ordnungszahl 414 von ComCtl32.dll anfordern, um einen Funktionszeiger zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 5.81 oder höher)</dt> </dl> |



 

