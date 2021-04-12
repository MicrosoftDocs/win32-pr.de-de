---
description: Diese Methode gibt ein Gerät zurück, das den Videodaten zugeordnet ist.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: 'Ivideoframenative:: getdevice-Methode'
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
ms.openlocfilehash: d012ae79b1cb2c83e916dc74113cc3d0560da4c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393517"
---
# <a name="ivideoframenativegetdevice-method"></a>Ivideoframenative:: getdevice-Methode

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

*riid* \[ in\]
</dt> <dd>

Die IID des abzurufenden Geräts.

</dd> <dt>

*PPV* \[ vorgenommen\]
</dt> <dd>

Wenn diese Methode erfolgreich zurückgegeben wird, enthält Sie den im *riid* -Parameter angeforderten Geräte Zeiger.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ beim erfolgreichen Abschluss S OK zurück.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivideoframenative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



