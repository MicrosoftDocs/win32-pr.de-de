---
description: Macht diesen Zeiger auf eine Elementbezeichnerliste (PIDL) zu einem ungültigen Teil des Shellordners.
title: IShellFolderSearchable::InvalidateSearch-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 5f443f3abd4a5cf2c1d0fc473c9267660d05c183a02c7f7705c1fabcbc9a8918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596570"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a>IShellFolderSearchable::InvalidateSearch-Methode

Macht diesen Zeiger auf eine Elementbezeichnerliste (PIDL) zu einem ungültigen Teil des Shellordners.

## <a name="syntax"></a>Syntax


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pidlSearch* \[ In\]
</dt> <dd>

Typ: **LPCITEMIDLIST**

Ein Zeiger auf die [**ITEMIDLIST-Struktur**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) für den Suchordner.

</dd> <dt>

*pdwFlags* \[ In\]
</dt> <dd>

Typ: **DWORD \***

Derzeit sind keine Flags definiert. legen Sie auf **NULL** fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn ein Suchordner für ungültig erklärt wird, kann er eine Bereinigung aller ressourcen durchführen, die er verwendet hat. Die **IShellFolderSearchable::InvalidateSearch-Methode** kann dazu führen, dass eine asynchrone Suche abgebrochen wird, was zur endgültigen Veröffentlichung des [**IShellFolderSearchableCallback-Schnittstellenobjekts**](ishellfoldersearchablecallback.md) führt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




