---
title: GetStreamPropertiesOperation.Completed (Eigenschaft)
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von GetStreamPropertiesAsync gestartete asynchrone Vorgang abgeschlossen wird, oder legt diesen fest.
ms.assetid: 97194F8E-DE36-4DC6-ADB5-F1EDE8AEF079
keywords:
- Abgeschlossene Eigenschaft Media Streaming-API
- Abgeschlossene Eigenschaft Media Streaming-API, GetStreamPropertiesOperation-Schnittstelle
- GetStreamPropertiesOperation-Schnittstelle Media Streaming-API , Completed-Eigenschaft
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6fc6982866ed97f70467d13cb5e899d94a1459266ca0149d12400d154aad784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100664"
---
# <a name="getstreampropertiesoperationcompleted-property"></a>GetStreamPropertiesOperation.Completed (Eigenschaft)

Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) gestartete asynchrone Vorgang abgeschlossen wird, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  IGetStreamPropertiesCompletedHandler *value
);

HRESULT get_Completed(
  [out] IGetStreamPropertiesCompletedHandler **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Ereignishandler.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetStreamPropertiesOperation**](getstreampropertiesoperation.md)
</dt> </dl>

 

 