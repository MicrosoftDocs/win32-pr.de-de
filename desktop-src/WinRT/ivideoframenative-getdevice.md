---
description: Diese Methode gibt ein Gerät zurück, das den Videodaten zugeordnet ist.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: IVideoFrameNative::GetDevice-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetDevice
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: 7f204cc0d44690a2b80c8642d590ef38510cebedbc00332720ec51529fe34ad2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323109"
---
# <a name="ivideoframenativegetdevice-method"></a>IVideoFrameNative::GetDevice-Methode

Diese Methode gibt ein Gerät zurück, das den Videodaten zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDevice(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*riid* \[ In\]
</dt> <dd>

Die IID des abzurufenden Geräts.

</dd> <dt>

*ppv* \[ out\]
</dt> <dd>

Enthält nach erfolgreicher Rückgabe dieser Methode den im *riid-Parameter angeforderten* Gerätezeiger.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK nach erfolgreichem Abschluss zurück.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



