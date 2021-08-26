---
description: Proxyfunktion für die InitializeFromIStream-Methode.
ms.assetid: 3ab780bb-7fe7-4abe-9ea7-86f54ea15d91
title: IWICStream_InitializeFromIStream_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromIStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 491a2a67881929eba86dc317645161dee28ee9062d01fee63a9f6d4a7995cf72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056560"
---
# <a name="iwicstream_initializefromistream_proxy-function"></a>IWICStream \_ \_ InitializeFromIStream-Proxyfunktion

Proxyfunktion für die [**InitializeFromIStream-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICStream_InitializeFromIStream_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ IStream    *pIStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DIES \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***

Zeiger auf dieses [**IWICStream-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)

</dd> <dt>

*pIStream* \[ In\]
</dt> <dd>

Typ: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***

Der Initialisierungsstream.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows NUR XP mit SP2, Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

