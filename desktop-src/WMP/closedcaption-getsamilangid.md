---
title: Closedcaption. getsamilangid-Methode
description: Die getsamilangid-Methode ruft den Gebiets Schema Bezeichner (LCID) einer Sprache ab, die von der aktuellen Sami-Datei unterstützt wird.
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- getsamilangid-Methode, Windows-Media Player
- getsamilangid-Methode, Windows Media Player, closedcaption-Klasse
- Closedcaption-Klasse, Windows Media Player, getsamilangid-Methode
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd543c9cb9d884022d78a875a2f8de078c479b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367160"
---
# <a name="closedcaptiongetsamilangid-method"></a><span data-ttu-id="399e5-106">Closedcaption. getsamilangid-Methode</span><span class="sxs-lookup"><span data-stu-id="399e5-106">ClosedCaption.getSAMILangID method</span></span>

<span data-ttu-id="399e5-107">Die **getsamilangid** -Methode ruft den Gebiets Schema Bezeichner (LCID) einer Sprache ab, die von der aktuellen Sami-Datei unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="399e5-107">The **getSAMILangID** method retrieves the locale identifier (LCID) of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="399e5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="399e5-108">Syntax</span></span>


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="399e5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="399e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="399e5-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="399e5-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="399e5-111">**Zahl** (**Long**), die den Index der abzurufenden LCID angibt.</span><span class="sxs-lookup"><span data-stu-id="399e5-111">**Number** (**long**) specifying the index of the LCID to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="399e5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="399e5-112">Return value</span></span>

<span data-ttu-id="399e5-113">Diese Methode gibt eine **Zahl** (**Long**) zurück, die die LCID der Sprache mit dem angegebenen Index enthält.</span><span class="sxs-lookup"><span data-stu-id="399e5-113">This method returns a **Number** (**long**) containing the LCID of the language with the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="399e5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="399e5-114">Remarks</span></span>

<span data-ttu-id="399e5-115">Die Sprachen in einer Sami-Datei werden in der in der Datei gezeigten Reihenfolge indiziert, beginnend mit 0 (null).</span><span class="sxs-lookup"><span data-stu-id="399e5-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="399e5-116">Diese Methode kann erst verwendet werden, wenn eine digitale Mediendatei (*Player*) geöffnet ist.**openstate** ist gleich 13).</span><span class="sxs-lookup"><span data-stu-id="399e5-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="399e5-117">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="399e5-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="399e5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="399e5-118">Requirements</span></span>



| <span data-ttu-id="399e5-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="399e5-119">Requirement</span></span> | <span data-ttu-id="399e5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="399e5-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="399e5-121">Version</span><span class="sxs-lookup"><span data-stu-id="399e5-121">Version</span></span><br/> | <span data-ttu-id="399e5-122">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="399e5-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="399e5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="399e5-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="399e5-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="399e5-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="399e5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="399e5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="399e5-126">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="399e5-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="399e5-127">**Closedcaption-Objekt**</span><span class="sxs-lookup"><span data-stu-id="399e5-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





