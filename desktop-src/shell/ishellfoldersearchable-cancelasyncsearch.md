---
description: Startet den Prozess des Abbrechens einer ausstehenden asynchronen Suche.
title: IShellFolderSearchable::CancelAsyncSearch-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.CancelAsyncSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5c920dca-fbca-48e1-9dce-38713cf1fcef
ms.openlocfilehash: 3146fea4f6c8d8547c8c86096b434cbaea5b5926
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842991"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a>IShellFolderSearchable::CancelAsyncSearch-Methode

Startet den Prozess des Abbrechens einer ausstehenden asynchronen Suche.

## <a name="syntax"></a>Syntax


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pidlSearch* \[ In\]
</dt> <dd>

Typ: **LPJSMIDLIST**

Ein Zeiger auf eine [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) für die Suche.

</dd> <dt>

*pdwFlags* \[ In\]
</dt> <dd>

Typ: **DWORD \***

Derzeit sind keine Flags definiert. auf **NULL festgelegt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Gibt S \_ OK zurück, wenn der Vorgang abgebrochen wird, oder S \_ FALSE, wenn die Suche nicht ausgeführt wird.

## <a name="remarks"></a>Hinweise

Wenn die Suche tatsächlich abgebrochen wird, [**wird RunEnd**](ishellfoldersearchablecallback-runend.md) aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




