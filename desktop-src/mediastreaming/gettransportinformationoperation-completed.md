---
title: Abgeschlossene gettransportinformationoperation-Eigenschaft
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von gettransportinformationasync gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.
ms.assetid: 11E60E00-75B5-4412-B115-4438255AEB8A
keywords:
- Abgeschlossene Eigenschaft Medien Streaming-API
- Abgeschlossene Eigenschaft Medien Streaming-API, gettransportinformationoperation-Schnittstelle
- Gettransportinformationoperation-Schnittstelle Medien Streaming-API, abgeschlossene Eigenschaft
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
ms.openlocfilehash: 2948af2ed84a70c9f37efbc4aae985e9b1ab5804
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339062"
---
# <a name="gettransportinformationoperationcompleted-property"></a>Gettransportinformationoperation:: Abgeschlossene Eigenschaft

Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**gettransportinformationasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Ereignishandler.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Gettransportinformationoperation**](gettransportinformationoperation.md)
</dt> </dl>

 

 