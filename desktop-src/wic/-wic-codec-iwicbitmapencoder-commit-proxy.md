---
description: 'IWICBitmapEncoder_Commit_Proxy-Funktion: Proxyfunktion für die Commit-Methode.'
ms.assetid: f7f1be43-fe44-47eb-a5ba-3446c0db22a6
title: IWICBitmapEncoder_Commit_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 934b2e21097a671c2b52ea77ab07caf25ab521a3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091188"
---
# <a name="iwicbitmapencoder_commit_proxy-function"></a>IWICBitmapEncoder-Commitproxyfunktion \_ \_

Proxyfunktion für [](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) die Commit-Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapEncoder_Commit_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DIES \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***

Zeiger auf dieses [**IWICBitmapEncoder-Objekt.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




