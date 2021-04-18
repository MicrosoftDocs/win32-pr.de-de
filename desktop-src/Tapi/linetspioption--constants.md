---
description: Die linetspioption- \_ Konstanten beschreiben, welche Bestell Dienstanbieter aufgerufen werden müssen.
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: LINETSPIOPTION_ Konstanten (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e8fa13047dcbad60472fac371b255f7533809c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365415"
---
# <a name="linetspioption_-constants"></a><span data-ttu-id="6c1ad-103">Linetspioption- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="6c1ad-103">LINETSPIOPTION\_ Constants</span></span>

<span data-ttu-id="6c1ad-104">Die **linetspioption- \_ Konstanten** beschreiben, welche Bestell Dienstanbieter aufgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="6c1ad-104">The **LINETSPIOPTION\_ constants** describes the order service providers should be called.</span></span>

<dl> <dt>

<span data-ttu-id="6c1ad-105"><span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**linetspioption \_ nicht Wiedereinstiegs fähig**</span><span class="sxs-lookup"><span data-stu-id="6c1ad-105"><span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION\_NONREENTRANT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6c1ad-106">TAPI sollte Funktionen in diesem Dienstanbieter nacheinander aufzurufen. vor dem Aufrufen der gleichen oder einer anderen Funktion, entweder auf demselben oder einem anderen Thread, auf demselben oder einem anderen Prozessor, sollte von jeder Funktion auf die Rückgabe gewartet werden (aber nicht für asynchrone Funktionen).</span><span class="sxs-lookup"><span data-stu-id="6c1ad-106">TAPI should call functions in this service provider one at a time; it should wait from each function to return (but not for asynchronous functions to complete) before calling the same or another function, either on the same or a different thread, on the same or a different processor.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c1ad-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c1ad-107">Requirements</span></span>



| <span data-ttu-id="6c1ad-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c1ad-108">Requirement</span></span> | <span data-ttu-id="6c1ad-109">Wert</span><span class="sxs-lookup"><span data-stu-id="6c1ad-109">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6c1ad-110">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="6c1ad-110">TAPI version</span></span><br/> | <span data-ttu-id="6c1ad-111">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="6c1ad-111">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6c1ad-112">Header</span><span class="sxs-lookup"><span data-stu-id="6c1ad-112">Header</span></span><br/>       | <dl> <span data-ttu-id="6c1ad-113"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c1ad-113"><dt>Tspi.h</dt></span></span> </dl> |



 

 




