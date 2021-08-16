---
description: Diese Methode gibt eine Schnittstelle zurück, die Zugriff auf die Videodaten bietet.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: IVideoFrameNative::GetData-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: 832b2e300887699b926362ce9cbfc6f334c181805bacb3546532920c684251d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993770"
---
# <a name="ivideoframenativegetdata-method"></a>IVideoFrameNative::GetData-Methode

Diese Methode gibt eine Schnittstelle zurück, die Zugriff auf die Videodaten bietet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*riid* \[ In\]
</dt> <dd>

Die IID der abzurufenden Schnittstelle.

</dd> <dt>

*ppv* \[ out\]
</dt> <dd>

Enthält nach erfolgreicher Rückgabe dieser Methode den schnittstellenzeiger, der im *riid-Parameter angefordert* wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK nach erfolgreichem Abschluss zurück. Gibt E \_ NOINTERFACE zurück, wenn die angeforderte Schnittstelle nicht gefunden werden kann.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



