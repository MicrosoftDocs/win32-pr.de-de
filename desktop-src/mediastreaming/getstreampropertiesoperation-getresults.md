---
title: Getstreampropertiesoperation. GetResults-Methode
description: Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von getstreampropertiesasync gestartet wurde.
ms.assetid: D09DCDF5-2B9E-4E03-908B-AEEC7DC228C1
keywords:
- GetResults-Methode Medien Streaming-API
- GetResults-Methode Medien Streaming-API, getstreampropertiesoperation-Schnittstelle
- Getstreampropertiesoperation-Schnittstelle Medien Streaming-API, GetResults-Methode
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 312703c28f5cdbb888b46d6ccd312dd358aa6b6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390235"
---
# <a name="getstreampropertiesoperationgetresults-method"></a><span data-ttu-id="274f6-106">Getstreampropertiesoperation. GetResults-Methode</span><span class="sxs-lookup"><span data-stu-id="274f6-106">GetStreamPropertiesOperation.GetResults method</span></span>

<span data-ttu-id="274f6-107">Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**getstreampropertiesasync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="274f6-107">Returns the results of the asynchronous operation started by [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span>

## <a name="syntax"></a><span data-ttu-id="274f6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="274f6-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="274f6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="274f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="274f6-110">*Wert* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="274f6-110">*value* \[out, retval\]</span></span>
<span data-ttu-id="274f6-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="274f6-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="274f6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="274f6-112">Return value</span></span>

<span data-ttu-id="274f6-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="274f6-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="274f6-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="274f6-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="274f6-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="274f6-115">Return code</span></span>                                                                          | <span data-ttu-id="274f6-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="274f6-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="274f6-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="274f6-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="274f6-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="274f6-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="274f6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="274f6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="274f6-120">**Getstreampropertiesoperation**</span><span class="sxs-lookup"><span data-stu-id="274f6-120">**GetStreamPropertiesOperation**</span></span>](getstreampropertiesoperation.md)
</dt> </dl>

 

