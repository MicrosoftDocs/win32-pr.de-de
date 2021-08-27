---
description: Proxyfunktion für die GetChannelMask-Methode.
ms.assetid: c96e6078-4648-4333-8a25-bcb03a2cd50b
title: IWICPixelFormatInfo_GetChannelMask_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelMask_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ee200dddf0b2cd736ca2ad435b63e774076465ad3d1f6215f1c558f1abb6c194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056600"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a>IWICPixelFormatInfo \_ \_ GetChannelMask-Proxyfunktion

Proxyfunktion für die [**GetChannelMask-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICPixelFormatInfo_GetChannelMask_Proxy(
  _In_    IWICPixelFormatInfo *THIS_PTR,
  _In_    UINT                uiChannelIndex,
  _In_    UINT                cbMaskBuffer,
  _Inout_ BYTE                *pbMaskBuffer,
  _Out_   UINT                *pcbActual
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\***

Zeiger auf dieses [**IWICPixelFormatInfo-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)

</dd> <dt>

*uiChannelIndex* \[ In\]
</dt> <dd>

Typ: **UINT**

Der Index für die abzurufende Kanalmaske.

</dd> <dt>

*cbMaskBuffer* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Größe des *pbMaskBuffer-Puffers.*

</dd> <dt>

*pbMaskBuffer* \[ in, out\]
</dt> <dd>

Typ: **BYTE \***

Zeiger auf den Maskenpuffer.

</dd> <dt>

*beiactual* \[ out\]
</dt> <dd>

Typ: **UINT \***

Die tatsächliche Puffergröße, die zum Abrufen der Kanalmaske erforderlich ist.

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



 

 




