---
title: Mirroricon-Funktion
description: Kehrt Symbole (Spiegelung) so um, dass Sie ordnungsgemäß in einem gespiegelten Gerätekontext angezeigt werden.
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- Windows-Steuerelemente der mirroricon-Funktion
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
ms.openlocfilehash: 02f180d509464b63e5ec73c5fb74e4d70386bdea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040237"
---
# <a name="mirroricon-function"></a>Mirroricon-Funktion

\[**Mirroricon** ist über Windows XP mit Service Pack 2 (SP2) verfügbar. Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar.\]

Kehrt Symbole (Spiegelung) so um, dass Sie ordnungsgemäß in einem gespiegelten Gerätekontext angezeigt werden.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phisubsmall* \[ in, out, optional\]
</dt> <dd>

Typ: **[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _

Ein Zeiger auf das Symbol Handle, das auf eine kleine Version eines Symbols verweist.

</dd> <dt>

_phIconLarge * \[ in, out, optional\]
</dt> <dd>

Typ: **[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _

Ein Zeiger auf das Symbol Handle, das auf eine große Version eines Symbols verweist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: _ *[**bool**](/windows/desktop/WinProg/windows-data-types)**

**True** , wenn erfolgreich; andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

**Mirroricon** wird nicht nach Name exportiert oder in einer öffentlichen Header Datei deklariert. Um es zu verwenden, müssen Sie [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und Request Ordnungszahl 414 aus ComCtl32.dll verwenden, um einen Funktionszeiger zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (Version 5,81 oder höher)</dt> </dl> |



 

