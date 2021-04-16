---
description: Die currentsubpicturestream-Eigenschaft legt den aktuellen teilbildstream fest oder ruft ihn ab.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Currentsubpicturestream (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c954ad7cfb7aba6dd9bc800ac983d86b6325843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522568"
---
# <a name="currentsubpicturestream-property"></a><span data-ttu-id="3146a-103">Currentsubpicturestream (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3146a-103">CurrentSubpictureStream Property</span></span>

> [!Note]  
> <span data-ttu-id="3146a-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3146a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3146a-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3146a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3146a-106">Die- `CurrentSubpictureStream` Eigenschaft legt den aktuellen teilbildstream fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="3146a-106">The `CurrentSubpictureStream` property sets or retrieves the current subpicture stream.</span></span>

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a><span data-ttu-id="3146a-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3146a-107">Return Value</span></span>

<span data-ttu-id="3146a-108">Gibt einen Integer-Wert zurück, der den Stream darstellt.</span><span class="sxs-lookup"><span data-stu-id="3146a-108">Returns an integer value representing the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="3146a-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3146a-109">Remarks</span></span>

<span data-ttu-id="3146a-110">Mögliche Werte für diese Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="3146a-110">The possible values of this property are:</span></span>



| <span data-ttu-id="3146a-111">Wert</span><span class="sxs-lookup"><span data-stu-id="3146a-111">Value</span></span>   | <span data-ttu-id="3146a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3146a-112">Description</span></span>              |
|---------|--------------------------|
| <span data-ttu-id="3146a-113">0 bis 31</span><span class="sxs-lookup"><span data-stu-id="3146a-113">0 to 31</span></span> | <span data-ttu-id="3146a-114">Der teilbildstream</span><span class="sxs-lookup"><span data-stu-id="3146a-114">The subpicture stream</span></span>    |
| <span data-ttu-id="3146a-115">63</span><span class="sxs-lookup"><span data-stu-id="3146a-115">63</span></span>      | <span data-ttu-id="3146a-116">Gedämpfter Datenstrom mit niedriger Bitrate</span><span class="sxs-lookup"><span data-stu-id="3146a-116">Muted low-bitrate stream</span></span> |



 

<span data-ttu-id="3146a-117">Diese Eigenschaft ist Lese-/Schreibzugriff und hat keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="3146a-117">This property is read/write with no default value.</span></span> <span data-ttu-id="3146a-118">Bevor Sie einen neuen teilbildstream festlegen, wenden Sie [**issubpicturestreamaktivian**](issubpicturestreamenabled-method.md) , um zu überprüfen, ob der Stream verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3146a-118">Before setting a new subpicture stream, call [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) to verify that the stream is available.</span></span>

<span data-ttu-id="3146a-119">Das Festlegen dieser Eigenschaft bewirkt, dass die Eigenschaft " [**subpictureon**](subpictureon-property.md) " in " **true**" gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="3146a-119">Setting this property causes the [**SubpictureOn**](subpictureon-property.md) property to toggle to **True**.</span></span>

## <a name="see-also"></a><span data-ttu-id="3146a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3146a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3146a-121">**Subpictureon**</span><span class="sxs-lookup"><span data-stu-id="3146a-121">**SubpictureOn**</span></span>](subpictureon-property.md)
</dt> <dt>

[<span data-ttu-id="3146a-122">**Subpicturestreamsavailable**</span><span class="sxs-lookup"><span data-stu-id="3146a-122">**SubpictureStreamsAvailable**</span></span>](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



