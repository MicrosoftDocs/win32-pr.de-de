---
description: 'IWICBitmap_SetResolution_Proxy-Funktion: Proxyfunktion für die SetResolution-Methode.'
ms.assetid: c4e3927c-6f9d-401d-acd7-711674cdbb53
title: IWICBitmap_SetResolution_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a32fa4e0d830d5307bc2927a1d5b6cb0a40e5b21f86517dc4421a0ce246a2ab8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056700"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a>IWICBitmap \_ \_ SetResolution-Proxyfunktion

Proxyfunktion für die [**SetResolution-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***

Zeiger auf dieses [**IWICBitmap-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)

</dd> <dt>

*dpiX* \[ In\]
</dt> <dd>

Typ: **double**

Die horizontale Auflösung.

</dd> <dt>

*dpiY* \[ In\]
</dt> <dd>

Typ: **double**

Die vertikale Auflösung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




