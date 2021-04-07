---
title: Getmuteoperation. abgeschlossene-Eigenschaft
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von getmuteasync gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.
ms.assetid: B8E1DE71-46AC-4F6A-B873-AE3239BE492C
keywords:
- Abgeschlossene Eigenschaft Medien Streaming-API
- Abgeschlossene Eigenschaft Medien Streaming-API, getmuteoperation-Schnittstelle
- Getmuteoperation-Schnittstelle Medien Streaming-API, abgeschlossene Eigenschaft
topic_type:
- apiref
api_name:
- GetMuteOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40c360dc3597d8cf04d1a8c505e479a38136f592
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726577"
---
# <a name="getmuteoperationcompleted-property"></a>Getmuteoperation. abgeschlossene-Eigenschaft

Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**getmuteasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  GetMuteCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetMuteCompletedHandler **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Ereignishandler.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getmuteoperation**](getmuteoperation.md)
</dt> </dl>

 

 