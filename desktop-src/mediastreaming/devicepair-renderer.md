---
title: DevicePair-Renderer (Eigenschaft)
description: Ruft den Renderer für das aktive Basisgerätepaar ab.
ms.assetid: DB2ED5D3-CCDF-4704-A29A-F1A13F7B953A
keywords:
- Renderereigenschaft Media Streaming-API
- Renderereigenschaft Media Streaming-API, DevicePair-Schnittstelle
- DevicePair-Schnittstelle Medienstreaming-API, Renderereigenschaft
topic_type:
- apiref
api_name:
- DevicePair.Renderer
- DevicePair.get_Renderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05707fd65e2ac8998fa2412ec15c12d3b003b88990641aad6510d87bd7692e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236083"
---
# <a name="devicepairrenderer-property"></a>DevicePair::Renderer-Eigenschaft

Ruft den Renderer für das aktive Basisgerätepaar ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Renderer(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Empfängt ein [**ActiveBasicDevice-Objekt,**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) das das Renderergerät darstellt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

 