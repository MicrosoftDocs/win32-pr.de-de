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
# <a name="mediarendereractioninformation-property"></a><span data-ttu-id="cc476-106">MediaRenderer. Action Information (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cc476-106">MediaRenderer.ActionInformation property</span></span>

<span data-ttu-id="cc476-107">Ruft Informationen darüber ab, welche Methoden derzeit für den DMR aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="cc476-107">Gets information about which methods can currently be invoked on the DMR.</span></span>

<span data-ttu-id="cc476-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cc476-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc476-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc476-109">Syntax</span></span>


```C++
HRESULT get_ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="property-value"></a><span data-ttu-id="cc476-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cc476-110">Property value</span></span>

<span data-ttu-id="cc476-111">Ein Verweis auf eine [**imediarendereraktioninformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cc476-111">A reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc476-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc476-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc476-113">**MediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="cc476-113">**MediaRenderer**</span></span>](mediarenderer.md)
</dt> </dl>

 

 