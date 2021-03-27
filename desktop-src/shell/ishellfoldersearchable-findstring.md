---
description: Startet eine Suche nach einer angegebenen Such Zeichenfolge.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: 'Ishellfoldersearchable:: FindString-Methode (MMC. h)'
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
ms.openlocfilehash: 3e256329bc235f7fe5a0428ba33710fa6b838f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753064"
---
# <a name="ishellfoldersearchablefindstring-method"></a>Ishellfoldersearchable:: FindString-Methode

Startet eine Suche nach einer angegebenen Such Zeichenfolge.

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

*pwsztarget* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf eine Zeichenfolge, die das Schlüsselwort für die Suche angibt.

</dd> <dt>

*pdwflags* \[ in\]
</dt> <dd>

Typ: **DWORD \** _

Zurzeit sind keine Flags definiert. Legen Sie auf _ * NULL * * fest.

</dd> <dt>

*punkonasyncsearch* \[ in\]
</dt> <dd>

Typ: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Ein Zeiger auf ein Objekt vom Typ [_ *IUnknown* *](/windows/win32/api/unknwn/nn-unknwn-iunknown). Dieses Objekt muss die [**ishellfoldersearchablecallback**](ishellfoldersearchablecallback.md) -Schnittstelle unterstützen. Auf **null** festgelegt, wenn kein Rückruf erforderlich ist.

</dd> <dt>

*ppidlout* \[ vorgenommen\]
</dt> <dd>

Typ: **lpitemittellist**

Ein Zeiger auf eine [**itemittel List**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) -Struktur für den Suchordner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>MMC. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
