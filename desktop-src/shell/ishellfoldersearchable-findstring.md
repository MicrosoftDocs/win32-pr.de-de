---
description: Beginnt eine Suche nach einer angegebenen Suchzeichenfolge.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: IShellFolderSearchable::FindString-Methode (Mmc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 947cda4094491702fa0f847e6a8abd4fed7bcbe9bd3504c5f8aec2097b0d6b8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220936"
---
# <a name="ishellfoldersearchablefindstring-method"></a>IShellFolderSearchable::FindString-Methode

Beginnt eine Suche nach einer angegebenen Suchzeichenfolge.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszTarget* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine Zeichenfolge, die das Suchschlüsselwort angibt.

</dd> <dt>

*pdwFlags* \[ In\]
</dt> <dd>

Typ: **DWORD \***

Derzeit sind keine Flags definiert. auf **NULL festgelegt.**

</dd> <dt>

*dateiOnAsyncSearch* \[ In\]
</dt> <dd>

Typ: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Ein Zeiger auf ein Objekt vom Typ [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Dieses Objekt muss die [**IShellFolderSearchableCallback-Schnittstelle**](ishellfoldersearchablecallback.md) unterstützen. Wird auf **NULL festgelegt,** wenn kein Rückruf erforderlich ist.

</dd> <dt>

*dldlOut* \[ out\]
</dt> <dd>

Typ: **LPITEMIDLIST**

Ein Zeiger auf eine [**ITEMIDLIST-Struktur**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) für den Suchordner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Mmc.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
