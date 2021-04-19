---
title: D1105 Threading Verletzung
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Auf eine Verleih Thread Schnittstelle wurde gleichzeitig von mehreren Threads aus zugegriffen.
keywords:
- D1105 Threading Verletzung Direct2D
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe83baa32be8ae18948ae5a80e3e0b218cd4fa4a
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2021
ms.locfileid: "106370892"
---
# <a name="d1105-threading-violation"></a><span data-ttu-id="6fbdd-104">D1105: Threading Verletzung</span><span class="sxs-lookup"><span data-stu-id="6fbdd-104">D1105: Threading Violation</span></span>

<span data-ttu-id="6fbdd-105">Auf eine Verleih Thread Schnittstellen \[ *Schnittstelle* \] wurde gleichzeitig von mehreren Threads aus zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-105">A rental threaded interface \[*interface*\] was simultaneously accessed from multiple threads.</span></span>

## <a name="placeholders"></a><span data-ttu-id="6fbdd-106">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="6fbdd-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="6fbdd-107"><span id="interface"></span><span id="INTERFACE"></span>*berfläche*</span><span class="sxs-lookup"><span data-stu-id="6fbdd-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="6fbdd-108">Die Adresse der Schnittstelle, auf die von mehreren Threads zugegriffen wurde.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-108">The address of the interface that was accessed by multiple threads.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="6fbdd-109">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="6fbdd-109">Possible Causes</span></span>

<span data-ttu-id="6fbdd-110">Verwenden einer Objektinstanz aus derselben Single Thread Factory aus zwei verschiedenen Threads.</span><span class="sxs-lookup"><span data-stu-id="6fbdd-110">Using an object instance from the same single-threaded factory from two different threads.</span></span>

 

 




