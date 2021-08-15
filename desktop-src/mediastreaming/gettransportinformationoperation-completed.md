---
title: GetTransportInformationOperation Completed (Eigenschaft)
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von GetTransportInformationAsync gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.
ms.assetid: 11E60E00-75B5-4412-B115-4438255AEB8A
keywords:
- Abgeschlossene Eigenschaft Media Streaming-API
- Abgeschlossene Eigenschaft Media Streaming-API, GetTransportInformationOperation-Schnittstelle
- GetTransportInformationOperation-Schnittstelle Media Streaming-API , Completed-Eigenschaft
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.Completed
- GetTransportInformationOperation.get_Completed
- GetTransportInformationOperation.put_Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 389d7b281c10458e854407f9ce02bd2656fe6d4b16574408d75ae06ccc06d7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735783"
---
# <a name="gettransportinformationoperationcompleted-property"></a>GetTransportInformationOperation::Completed (Eigenschaft)

Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Ereignishandler.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetTransportInformationOperation**](gettransportinformationoperation.md)
</dt> </dl>

 

 