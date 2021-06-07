---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: Stellt ein DirectML-Gerät dar, das zum Erstellen von Operatoren, Bindungstabellen, Befehlsaufzeichnungen und anderen Objekten verwendet wird.
helpviewer_keywords:
- IDMLDevice1
- IDMLDevice1 interface
- IDMLDevice1 interface
- described
- direct3d12.idmldevice1
- directml/IDMLDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1
- directml/IDMLDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.h
api_name:
- IDMLDevice1
ms.openlocfilehash: 7a10cf2c9fe683775d163c7b5cb0e30fe07de08f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417178"
---
# <a name="idmldevice1-interface-directmlh"></a><span data-ttu-id="ae24e-103">IDMLDevice1-Schnittstelle (directml.h)</span><span class="sxs-lookup"><span data-stu-id="ae24e-103">IDMLDevice1 interface (directml.h)</span></span>

<span data-ttu-id="ae24e-104">Stellt ein DirectML-Gerät dar, das zum Erstellen von Operatoren, Bindungstabellen, Befehlsaufzeichnungen und anderen Objekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae24e-104">Represents a DirectML device, which is used to create operators, binding tables, command recorders, and other objects.</span></span> <span data-ttu-id="ae24e-105">Die **IDMLDevice1-Schnittstelle** erbt von [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span><span class="sxs-lookup"><span data-stu-id="ae24e-105">The **IDMLDevice1** interface inherits from [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

<span data-ttu-id="ae24e-106">Ein DirectML-Gerät ist immer genau einem zugrunde liegenden Direct3D 12-Gerät zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ae24e-106">A DirectML device is always associated with exactly one underlying Direct3D 12 device.</span></span> <span data-ttu-id="ae24e-107">Alle vom DirectML-Gerät erstellten Objekte behalten einen starken Verweis auf ihr übergeordnetes Gerät bei.</span><span class="sxs-lookup"><span data-stu-id="ae24e-107">All objects created by the DirectML device maintain a strong reference to their parent device.</span></span> <span data-ttu-id="ae24e-108">Im Gegensatz zum Direct3D 12-Gerät ist das DML-Gerät kein Singleton.</span><span class="sxs-lookup"><span data-stu-id="ae24e-108">Unlike the Direct3D 12 device, the DML device is not a singleton.</span></span> <span data-ttu-id="ae24e-109">Daher ist es möglich, mehrere DirectML-Geräte über dasselbe Direct3D 12-Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae24e-109">Therefore, it's possible to create multiple DirectML devices over the same Direct3D 12 device.</span></span> <span data-ttu-id="ae24e-110">Dies wird jedoch nicht empfohlen, da das DirectML-Gerät über keinen veränderlichen Zustand verfügt, sodass es wenig Vorteile bietet, mehrere DML-Geräte über dasselbe Direct3D 12-Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae24e-110">However, this isn't recommended as the DirectML device has no mutable state, so there's little advantage to creating multiple DML devices over the same Direct3D 12 device.</span></span>

<span data-ttu-id="ae24e-111">Dieses Objekt ist threadsicher.</span><span class="sxs-lookup"><span data-stu-id="ae24e-111">This object is thread-safe.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae24e-112">Diese API ist als Teil des eigenständigen weiterverteilten DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher).</span><span class="sxs-lookup"><span data-stu-id="ae24e-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="ae24e-113">Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="ae24e-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="availability"></a><span data-ttu-id="ae24e-114">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="ae24e-114">Availability</span></span>
<span data-ttu-id="ae24e-115">Diese API wurde in der DirectML-Version `1.1.0` eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ae24e-115">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ae24e-116">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="ae24e-116">Tensor constraints</span></span>
<span data-ttu-id="ae24e-117">**Zielplattform:** Windows</span><span class="sxs-lookup"><span data-stu-id="ae24e-117">**Target Platform**: Windows</span></span>


## <a name="inheritance"></a><span data-ttu-id="ae24e-118">Vererbung</span><span class="sxs-lookup"><span data-stu-id="ae24e-118">Inheritance</span></span>


<span data-ttu-id="ae24e-119">Die IDMLDevice1-Schnittstelle erbt von der IDMLDevice-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ae24e-119">The IDMLDevice1 interface inherits from the IDMLDevice interface.</span></span>



## <a name="methods"></a><span data-ttu-id="ae24e-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="ae24e-120">Methods</span></span>

<p><span data-ttu-id="ae24e-121">Die <b>IDMLDevice1-Schnittstelle</b> verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ae24e-121">The <b>IDMLDevice1</b> interface has these methods.</span></span></p>

| <span data-ttu-id="ae24e-122">Methode</span><span class="sxs-lookup"><span data-stu-id="ae24e-122">Method</span></span> | <span data-ttu-id="ae24e-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae24e-123">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="ae24e-124">IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="ae24e-124">IDMLDevice1::CompileGraph</span></span>](../directml/nf-directml-idmldevice1-compilegraph.md) | <span data-ttu-id="ae24e-125">Kompiliert ein Diagramm von DirectML-Operatoren in ein Objekt, das an die GPU gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae24e-125">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span> |


## <a name="requirements"></a><span data-ttu-id="ae24e-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ae24e-126">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ae24e-127">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="ae24e-127">**Target Platform**</span></span> | <span data-ttu-id="ae24e-128">Windows</span><span class="sxs-lookup"><span data-stu-id="ae24e-128">Windows</span></span> |
| <span data-ttu-id="ae24e-129">**Header**</span><span class="sxs-lookup"><span data-stu-id="ae24e-129">**Header**</span></span> | <span data-ttu-id="ae24e-130">directml.h</span><span class="sxs-lookup"><span data-stu-id="ae24e-130">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="ae24e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae24e-131">See also</span></span>

[<span data-ttu-id="ae24e-132">IDMLDevice-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ae24e-132">IDMLDevice interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)