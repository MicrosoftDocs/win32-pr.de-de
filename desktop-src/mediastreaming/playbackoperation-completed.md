---
title: Playbackoperation. abgeschlossene-Eigenschaft
description: Dient zum Abrufen oder Festlegen eines Ereignis Handlers, der aufgerufen wird, wenn der asynchrone Vorgang, der von einer der MediaRenderer-Wiedergabe Methoden gestartet wurde, abgeschlossen ist.
ms.assetid: E8F8D3FC-C31F-485C-A30B-2457F4B1DE82
keywords:
- Abgeschlossene Eigenschaft Medien Streaming-API
- Abgeschlossene Eigenschaft Medien Streaming-API, playbackoperation-Schnittstelle
- Playbackoperation-Schnittstelle Medien Streaming-API, abgeschlossene Eigenschaft
topic_type:
- apiref
api_name:
- PlaybackOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bf305b4028e223c36df0c8a59c5246228c5b8d40
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338226"
---
# <a name="playbackoperationcompleted-property"></a>Playbackoperation. abgeschlossene-Eigenschaft

Dient zum Abrufen oder Festlegen eines Ereignis Handlers, der aufgerufen wird, wenn der asynchrone Vorgang, der von einer der [**MediaRenderer**](mediarenderer.md) -Wiedergabe Methoden gestartet wurde, abgeschlossen ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  PlaybackOperationCompletedHandler *value
);

HRESULT get_Completed(
  [out] PlaybackOperationCompletedHandler **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Ereignishandler.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Playbackoperation**](playbackoperation.md)
</dt> </dl>

 

 




