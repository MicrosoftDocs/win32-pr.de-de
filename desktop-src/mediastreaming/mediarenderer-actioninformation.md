---
title: MediaRenderer. Action Information (Eigenschaft)
description: Ruft Informationen darüber ab, welche Methoden derzeit für den DMR aufgerufen werden können.
ms.assetid: c36d45cb-c01a-4418-8f21-906c95950d6f
keywords:
- Aktions Informations Eigenschaft Medien Streaming-API
- Action Information-Eigenschaft Medien Streaming-API, MediaRenderer-Schnittstelle
- MediaRenderer-Schnittstelle Medien Streaming-API, Action Information-Eigenschaft
topic_type:
- apiref
api_name:
- MediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f5ce6c0bf9baf30cd8184d5271ed996c6406ddf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339268"
---
# <a name="mediarendereractioninformation-property"></a>MediaRenderer. Action Information (Eigenschaft)

Ruft Informationen darüber ab, welche Methoden derzeit für den DMR aufgerufen werden können.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Verweis auf eine [**imediarendereraktioninformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) -Schnittstelle.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 