---
title: Streamselectoperation. GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von selectbeststreamasync gestartet wurde.
ms.assetid: 2D9887E7-17C8-4161-984F-FA44591D2052
keywords:
- GetResults-Methode Medien Streaming-API
- GetResults-Methode Medien Streaming-API, streamselectoperation-Schnittstelle
- Streamselectoperation-Schnittstelle Medien Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- StreamSelectOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c52479949413d32ca54654f355a06a2dee70866e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106342124"
---
# <a name="streamselectoperationgetresults-method"></a><span data-ttu-id="f748e-106">Streamselectoperation. GetResults-Methode</span><span class="sxs-lookup"><span data-stu-id="f748e-106">StreamSelectOperation.GetResults method</span></span>

<span data-ttu-id="f748e-107">Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**selectbeststreamasync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="f748e-107">Returns the results of the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span>

## <a name="syntax"></a><span data-ttu-id="f748e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f748e-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="f748e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f748e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f748e-110">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f748e-110">*value* \[out, retval\]</span></span>
<span data-ttu-id="f748e-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f748e-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="f748e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f748e-112">Return value</span></span>

<span data-ttu-id="f748e-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="f748e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f748e-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f748e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f748e-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f748e-115">Return code</span></span>                                                                          | <span data-ttu-id="f748e-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f748e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f748e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f748e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f748e-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f748e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f748e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f748e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f748e-120">**Streamselectoperation**</span><span class="sxs-lookup"><span data-stu-id="f748e-120">**StreamSelectOperation**</span></span>](streamselectoperation.md)
</dt> </dl>

 

