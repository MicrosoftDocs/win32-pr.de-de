---
title: BasicDevice.Icons (Eigenschaft)
description: Ruft einen Vektor von IDeviceIcon-Schnittstellen ab.
ms.assetid: 54933FD0-27A6-48D8-A49A-200AD9214B9A
keywords:
- Symboleigenschaft Medienstreaming-API
- Symboleigenschaft Media Streaming-API, BasicDevice-Schnittstelle
- BasicGeräteschnittstelle Medienstreaming-API, Icons-Eigenschaft
topic_type:
- apiref
api_name:
- BasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9807c41680c042ee74b2ddc659ad1558dd13ff8b4000d08cfa0591768c301bb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554660"
---
# <a name="basicdeviceicons-property"></a>BasicDevice.Icons (Eigenschaft)

Ruft einen Vektor von [**IDeviceIcon-Schnittstellen**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine aufzählbare Auflistung von [**IDeviceIcon-Schnittstellenzeigern.**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

 