---
description: Erstellt ein Farbtransformationsobjekt, das IWICColorTransform implementiert. Dieses COM-Objekt unterstützt das Freethread-Objektmodell.
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
ms.openlocfilehash: 89c7476bc32546f0a9fe77a8731f239702c6a2a874dbfb830b9d4bbafbd872b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709217"
---
# <a name="wiccreatecolortransform_proxy-function"></a>WICCreateColorTransform-Proxyfunktion \_

Erstellt ein Farbtransformationsobjekt, das [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform)implementiert. Dieses COM-Objekt unterstützt das Freethread-Objektmodell.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppIColorTransform* \[ out\]
</dt> <dd>

Die erstellte Farbtransformation.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 
