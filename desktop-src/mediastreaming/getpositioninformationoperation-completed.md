---
title: Getpositioninformationoperation. abgeschlossene (Eigenschaft)
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von getpositioninformationasync gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.
ms.assetid: 144065AE-6C23-4E9D-B9D0-6849E7FB74C4
keywords:
- Abgeschlossene Eigenschaft Medien Streaming-API
- Abgeschlossene Eigenschaft Medien Streaming-API, getpositioninformationoperation-Schnittstelle
- Getpositioninformationoperation-Schnittstelle Medien Streaming-API, abgeschlossene Eigenschaft
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90b4ed4a6402b8c7bfc1ee559bd0b43765a64cec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390284"
---
# <a name="getpositioninformationoperationcompleted-property"></a>Getpositioninformationoperation. abgeschlossene (Eigenschaft)

Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**getpositioninformationasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  GetPositionInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetPositionInformationCompletedHandler **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Ereignishandler.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getpositioninformationoperation**](getpositioninformationoperation.md)
</dt> </dl>

 

 