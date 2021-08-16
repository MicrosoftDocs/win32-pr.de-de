---
title: GetMuteOperation.Completed-Eigenschaft
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von GetMuteAsync gestartete asynchrone Vorgang abgeschlossen wird, oder legt diesen fest.
ms.assetid: B8E1DE71-46AC-4F6A-B873-AE3239BE492C
keywords:
- Abgeschlossene Eigenschaft Medienstreaming-API
- Abgeschlossene Eigenschaft Medienstreaming-API , GetMuteOperation-Schnittstelle
- GetMuteOperation-Schnittstelle Medienstreaming-API , Completed-Eigenschaft
topic_type:
- apiref
api_name:
- GetMuteOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb27715f284b96af4ba9e6cf8ff825a7237ba027d46d30d77859018d4d8b5574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100674"
---
# <a name="getmuteoperationcompleted-property"></a>GetMuteOperation.Completed-Eigenschaft

Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**GetMuteAsync gestartete asynchrone**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) Vorgang abgeschlossen wird, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  GetMuteCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetMuteCompletedHandler **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Ereignishandler.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetMuteOperation**](getmuteoperation.md)
</dt> </dl>

 

 