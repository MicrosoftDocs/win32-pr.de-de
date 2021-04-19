---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: Stellt ein directml-Gerät dar, das zum Erstellen von Operatoren, Bindungs Tabellen, Befehls Recorder und anderen Objekten verwendet wird.
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
ms.openlocfilehash: a23d6ec4299a2aa3ca7e9f6873167412d094af8d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106361746"
---
# <a name="idmldevice1-interface-directmlh"></a><span data-ttu-id="9a4e6-103">IDMLDevice1-Schnittstelle (directml. h)</span><span class="sxs-lookup"><span data-stu-id="9a4e6-103">IDMLDevice1 interface (directml.h)</span></span>

<span data-ttu-id="9a4e6-104">Stellt ein directml-Gerät dar, das zum Erstellen von Operatoren, Bindungs Tabellen, Befehls Recorder und anderen Objekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a4e6-104">Represents a DirectML device, which is used to create operators, binding tables, command recorders, and other objects.</span></span> <span data-ttu-id="9a4e6-105">Die **IDMLDevice1** -Schnittstelle erbt von [idmldevice](/windows/win32/api/directml/nn-directml-idmldevice).</span><span class="sxs-lookup"><span data-stu-id="9a4e6-105">The **IDMLDevice1** interface inherits from [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

<span data-ttu-id="9a4e6-106">Ein directml-Gerät ist immer genau einem zugrunde liegenden Direct3D 12-Gerät zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9a4e6-106">A DirectML device is always associated with exactly one underlying Direct3D 12 device.</span></span> <span data-ttu-id="9a4e6-107">Alle Objekte, die vom directml-Gerät erstellt wurden, behalten einen starken Verweis auf das übergeordnete Gerät bei.</span><span class="sxs-lookup"><span data-stu-id="9a4e6-107">All objects created by the DirectML device maintain a strong reference to their parent device.</span></span> <span data-ttu-id="9a4e6-108">Im Gegensatz zum Direct3D 12-Gerät ist das DML-Gerät kein Singleton.</span><span class="sxs-lookup"><span data-stu-id="9a4e6-108">Unlike the Direct3D 12 device, the DML device is not a singleton.</span></span> <span data-ttu-id="9a4e6-109">Daher ist es möglich, mehrere directml-Geräte über das gleiche Direct3D 12-Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a4e6-109">Therefore, it's possible to create multiple DirectML devices over the same Direct3D 12 device.</span></span> <span data-ttu-id="9a4e6-110">Dies wird jedoch nicht empfohlen, da das directml-Gerät keinen änderbaren Zustand aufweist. es gibt also wenig Vorteil beim Erstellen mehrerer DML-Geräte über dasselbe Direct3D 12-Gerät.</span><span class="sxs-lookup"><span data-stu-id="9a4e6-110">However, this isn't recommended as the DirectML device has no mutable state, so there's little advantage to creating multiple DML devices over the same Direct3D 12 device.</span></span>

<span data-ttu-id="9a4e6-111">Dieses Objekt ist Thread sicher.</span><span class="sxs-lookup"><span data-stu-id="9a4e6-111">This object is thread-safe.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a4e6-112">Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)).</span><span class="sxs-lookup"><span data-stu-id="9a4e6-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="9a4e6-113">Siehe auch [Versionsverlauf der directml](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="9a4e6-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="availability"></a><span data-ttu-id="9a4e6-114">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="9a4e6-114">Availability</span></span>
<span data-ttu-id="9a4e6-115">Diese API wurde in der directml-Version eingeführt `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="9a4e6-115">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="9a4e6-116">Tensor-Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="9a4e6-116">Tensor constraints</span></span>
<span data-ttu-id="9a4e6-117">**Zielplattform**: Windows</span><span class="sxs-lookup"><span data-stu-id="9a4e6-117">**Target Platform**: Windows</span></span>


## <a name="inheritance"></a><span data-ttu-id="9a4e6-118">Vererbung</span><span class="sxs-lookup"><span data-stu-id="9a4e6-118">Inheritance</span></span>


<span data-ttu-id="9a4e6-119">Die IDMLDevice1-Schnittstelle erbt von der idmldevice-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9a4e6-119">The IDMLDevice1 interface inherits from the IDMLDevice interface.</span></span>



## <a name="methods"></a><span data-ttu-id="9a4e6-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="9a4e6-120">Methods</span></span>

<p><span data-ttu-id="9a4e6-121">Die <b>IDMLDevice1</b> -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9a4e6-121">The <b>IDMLDevice1</b> interface has these methods.</span></span></p>

| <span data-ttu-id="9a4e6-122">Methode</span><span class="sxs-lookup"><span data-stu-id="9a4e6-122">Method</span></span> | <span data-ttu-id="9a4e6-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a4e6-123">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="9a4e6-124">IDMLDevice1:: compilegraph</span><span class="sxs-lookup"><span data-stu-id="9a4e6-124">IDMLDevice1::CompileGraph</span></span>](../directml/nf-directml-idmldevice1-compilegraph.md) | <span data-ttu-id="9a4e6-125">Kompiliert ein Diagramm von directml-Operatoren in ein Objekt, das an die GPU gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9a4e6-125">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span> |


## <a name="requirements"></a><span data-ttu-id="9a4e6-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a4e6-126">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9a4e6-127">**Zielplattform**</span><span class="sxs-lookup"><span data-stu-id="9a4e6-127">**Target Platform**</span></span> | <span data-ttu-id="9a4e6-128">Windows</span><span class="sxs-lookup"><span data-stu-id="9a4e6-128">Windows</span></span> |
| <span data-ttu-id="9a4e6-129">**Header**</span><span class="sxs-lookup"><span data-stu-id="9a4e6-129">**Header**</span></span> | <span data-ttu-id="9a4e6-130">directml. h</span><span class="sxs-lookup"><span data-stu-id="9a4e6-130">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="9a4e6-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a4e6-131">See also</span></span>

[<span data-ttu-id="9a4e6-132">Idmldevice-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9a4e6-132">IDMLDevice interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)