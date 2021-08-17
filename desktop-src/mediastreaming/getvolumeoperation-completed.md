---
title: GetVolumeOperation.Completed-Eigenschaft
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von GetVolumeAsync gestartete asynchrone Vorgang abgeschlossen wird, oder legt diesen fest.
ms.assetid: 34100EE7-C4CB-4AE0-BD3E-9E23A643F87E
keywords:
- Abgeschlossene Eigenschaft Medienstreaming-API
- Abgeschlossene Eigenschaft Medienstreaming-API , GetVolumeOperation-Schnittstelle
- GetVolumeOperation-Schnittstelle Medienstreaming-API , Completed-Eigenschaft
topic_type:
- apiref
api_name:
- GetVolumeOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 84668f41f12c4920ec45bf70a3a931e6fc9234e213fe0a359ab93f3e34aac724
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735756"
---
# <a name="getvolumeoperationcompleted-property"></a>GetVolumeOperation.Completed-Eigenschaft

Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**GetVolumeAsync gestartete asynchrone**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) Vorgang abgeschlossen wird, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  GetVolumeCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetVolumeCompletedHandler **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Ereignishandler.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetVolumeOperation**](getvolumeoperation.md)
</dt> </dl>

 

 