---
description: Erstellt ein Farb Transformations Objekt, das iwiccolortransform implementiert. Dieses com-Objekt unterstützt das frei Hand Thread-Objektmodell.
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: WICCreateColorTransform_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorTransform_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 451b549aa44e785e406f50ccf4eb7a8317edf6b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366921"
---
# <a name="wiccreatecolortransform_proxy-function"></a>Wickreatecolortransform- \_ Proxy Funktion

Erstellt ein Farb Transformations Objekt, das [**iwiccolortransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform)implementiert. Dieses com-Objekt unterstützt das frei Hand Thread-Objektmodell.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppicolortransform* \[ vorgenommen\]
</dt> <dd>

Die erstellte Farb Transformation.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 
