---
title: Streamselectoperation. abgeschlossene Eigenschaft
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von selectbeststreamasync gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.
ms.assetid: 693CC002-2D91-4656-954D-8A556480155C
keywords:
- Abgeschlossene Eigenschaft Medien Streaming-API
- Abgeschlossene Eigenschaft Medien Streaming-API, streamselectoperation-Schnittstelle
- Streamselectoperation-Schnittstelle Medien Streaming-API, abgeschlossene Eigenschaft
topic_type:
- apiref
api_name:
- StreamSelectOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74cfdf1a3db4f6843a5f12522b688e889e156f33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338055"
---
# <a name="streamselectoperationcompleted-property"></a>Streamselectoperation. abgeschlossene Eigenschaft

Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**selectbeststreamasync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Ereignishandler.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Streamselectoperation**](streamselectoperation.md)
</dt> </dl>

 

 