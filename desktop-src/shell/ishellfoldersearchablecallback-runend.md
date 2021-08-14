---
description: Gibt an, dass eine Suche abgeschlossen wurde.
title: IShellFolderSearchableCallback::RunEnd-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunEnd
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91700764-6cdf-488d-adc0-e34d9b4cb71d
ms.openlocfilehash: 077ed97ad05ae3b12f3d00f695b15844a7b9ba05d693035b5ca8036b1d8da283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220366"
---
# <a name="ishellfoldersearchablecallbackrunend-method"></a>IShellFolderSearchableCallback::RunEnd-Methode

Gibt an, dass eine Suche abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT RunEnd(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwReserved* \[ In\]
</dt> <dd>

Typ: **DWORD**

Reserviert. Muss auf 0 festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




