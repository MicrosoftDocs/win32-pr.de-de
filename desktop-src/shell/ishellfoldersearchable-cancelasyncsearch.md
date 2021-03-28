---
description: Startet das Abbrechen einer ausstehenden asynchronen Suche.
title: 'Ishellfoldersearchable:: cancelasyncsearch-Methode'
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
ms.openlocfilehash: e9e3231e8cc602a4e00b6ee79a25392717b6e68b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977953"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a>Ishellfoldersearchable:: cancelasyncsearch-Methode

Startet das Abbrechen einer ausstehenden asynchronen Suche.

## <a name="syntax"></a>Syntax


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pidlsearch* \[ in\]
</dt> <dd>

Typ: **lpcitemittellist**

Ein Zeiger auf eine [**itemittel List**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) für die Suche.

</dd> <dt>

*pdwflags* \[ in\]
</dt> <dd>

Typ: **DWORD \** _

Zurzeit sind keine Flags definiert. Legen Sie auf _ * NULL * * fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Gibt s \_ OK zurück, wenn abgebrochen wird, oder s \_ false, wenn die Suche nicht ausgeführt wird.

## <a name="remarks"></a>Bemerkungen

Wenn die Suche tatsächlich abgebrochen wird, wird [**RunEnd**](ishellfoldersearchablecallback-runend.md) aufgerufen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




