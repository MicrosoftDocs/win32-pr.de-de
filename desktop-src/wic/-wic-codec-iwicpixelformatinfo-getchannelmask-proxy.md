---
description: Proxy Funktion für die getchannelmask-Methode.
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
ms.openlocfilehash: 0db2c14e89aba2b13cb95209b81f6d0da5d9d949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218039"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a>Iwicpixelformatinfo- \_ Funktion "getchannelmask" \_

Proxy Funktion für die [**getchannelmask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) -Methode.

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

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**iwicpixelformatinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _

Zeiger auf dieses [_ *iwicpixelformatinfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) -Objekt.

</dd> <dt>

*uichannelindex* \[ in\]
</dt> <dd>

Typ: **uint**

Der Index für die abzurufende Kanalmaske.

</dd> <dt>

*cbmaskbuffer* \[ in\]
</dt> <dd>

Typ: **uint**

Die Größe des *pbmaskbuffer* -Puffers.

</dd> <dt>

*pbmaskbuffer* \[ in, out\]
</dt> <dd>

Typ: **Byte \** _

Zeiger auf den Masken Puffer.

</dd> <dt>

_pcbActual * \[ out\]
</dt> <dd>

Typ: **uint \** _

Die tatsächliche Puffergröße, die zum Abrufen der Kanalmaske benötigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




