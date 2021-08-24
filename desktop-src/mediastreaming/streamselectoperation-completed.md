---
title: StreamSelectOperation.Completed-Eigenschaft
description: Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von SelectBestStreamAsync gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.
ms.assetid: 693CC002-2D91-4656-954D-8A556480155C
keywords:
- Abgeschlossene Eigenschaft Medienstreaming-API
- Abgeschlossene Eigenschaft Medienstreaming-API , StreamSelectOperation-Schnittstelle
- StreamSelectOperation-Schnittstelle Medienstreaming-API , Completed-Eigenschaft
topic_type:
- apiref
api_name:
- StreamSelectOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 554874c19054f4b2ee46fbfe29fb4dfb8149e476ff96d040ffdbdd9b39de4612
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847580"
---
# <a name="streamselectoperationcompleted-property"></a>StreamSelectOperation.Completed-Eigenschaft

Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Ereignishandler.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**StreamSelectOperation**](streamselectoperation.md)
</dt> </dl>

 

 