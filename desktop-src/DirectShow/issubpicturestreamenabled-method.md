---
description: Die issubpicturestreamaktivierte-Methode ruft einen Wert ab, der angibt, ob der angegebene subbildstream im aktuellen Titel aktiviert ist.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Issubpicturestreamaktivierte Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 818b4ff18dac87ea3346a1a503764b2e5e9cd02a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860428"
---
# <a name="issubpicturestreamenabled-method"></a><span data-ttu-id="12f7b-103">Issubpicturestreamaktivierte Methode</span><span class="sxs-lookup"><span data-stu-id="12f7b-103">IsSubpictureStreamEnabled Method</span></span>

> [!Note]  
> <span data-ttu-id="12f7b-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="12f7b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="12f7b-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="12f7b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="12f7b-106">Die- `IsSubpictureStreamEnabled` Methode ruft einen Wert ab, der angibt, ob der angegebene teilbildstream im aktuellen Titel aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="12f7b-106">The `IsSubpictureStreamEnabled` method retrieves a value indicating whether the specified subpicture stream is enabled in the current title.</span></span>

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a><span data-ttu-id="12f7b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="12f7b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12f7b-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*IStream*</span><span class="sxs-lookup"><span data-stu-id="12f7b-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="12f7b-109">Gibt den subbildstream als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="12f7b-109">Specifies the subpicture stream as an Integer.</span></span>



| <span data-ttu-id="12f7b-110">Wert</span><span class="sxs-lookup"><span data-stu-id="12f7b-110">Value</span></span>   | <span data-ttu-id="12f7b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12f7b-111">Description</span></span>              |
|---------|--------------------------|
| <span data-ttu-id="12f7b-112">0 bis 31</span><span class="sxs-lookup"><span data-stu-id="12f7b-112">0 to 31</span></span> | <span data-ttu-id="12f7b-113">subbildstream</span><span class="sxs-lookup"><span data-stu-id="12f7b-113">subpicture stream</span></span>        |
| <span data-ttu-id="12f7b-114">63</span><span class="sxs-lookup"><span data-stu-id="12f7b-114">63</span></span>      | <span data-ttu-id="12f7b-115">gedämpfter Datenstrom mit niedriger Bitrate</span><span class="sxs-lookup"><span data-stu-id="12f7b-115">muted low-bitrate stream</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12f7b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12f7b-116">Return Value</span></span>

<span data-ttu-id="12f7b-117">Gibt einen booleschen Wert zurück, der angibt, ob der angegebene Audiostream im aktuellen Titel verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="12f7b-117">Returns a Boolean value indicating whether the specified audio stream is available in the current title.</span></span> <span data-ttu-id="12f7b-118">"True" bedeutet, dass Sie verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="12f7b-118">True means it is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="12f7b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12f7b-119">Remarks</span></span>

<span data-ttu-id="12f7b-120">Obwohl eine CD bis zu 32 unter bildstreams enthalten kann, ist jeder Stream nicht notwendigerweise für jeden Titel verfügbar.</span><span class="sxs-lookup"><span data-stu-id="12f7b-120">Although a disc can contain up to 32 subpicture streams, each stream is not necessarily available for each title.</span></span> <span data-ttu-id="12f7b-121">Überprüfen Sie vor dem Festlegen der [**currentsubpicturestream**](currentsubpicturestream-property.md) -Eigenschaft immer, ob ein Datenstrom für einen Titel verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="12f7b-121">Always verify that a stream is available for a title before setting the [**CurrentSubpictureStream**](currentsubpicturestream-property.md) property.</span></span>

 

 



