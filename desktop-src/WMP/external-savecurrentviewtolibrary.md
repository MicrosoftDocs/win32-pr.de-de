---
title: Extern. savecurrentviewylibrary-Methode
description: Die savecurrentviewylibrary-Methode erstellt eine Wiedergabeliste aus den Medien Elementen in der aktuellen Ansicht und speichert die Wiedergabeliste in der lokalen Bibliothek.
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- savecurrentviewylibrary-Methode, Windows Media Player
- savecurrentviewylibrary-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, savecurrentviewylibrary-Methode
topic_type:
- apiref
api_name:
- External.saveCurrentViewToLibrary
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 212f590f03c32821c0774c4898720c92558ecc73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369545"
---
# <a name="externalsavecurrentviewtolibrary-method"></a><span data-ttu-id="3082f-106">Extern. savecurrentviewylibrary-Methode</span><span class="sxs-lookup"><span data-stu-id="3082f-106">External.saveCurrentViewToLibrary method</span></span>

<span data-ttu-id="3082f-107">Die **savecurrentviewylibrary** -Methode erstellt eine Wiedergabeliste aus den Medien Elementen in der aktuellen Ansicht und speichert die Wiedergabeliste in der lokalen Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="3082f-107">The **saveCurrentViewToLibrary** method creates a playlist from the media items in the current view and saves the playlist in the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="3082f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3082f-108">Syntax</span></span>


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a><span data-ttu-id="3082f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3082f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3082f-110">*Friendlylistname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3082f-110">*FriendlyListName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3082f-111">Eine **Zeichenfolge** , die einen anzeigen Amen für die Wiedergabeliste angibt.</span><span class="sxs-lookup"><span data-stu-id="3082f-111">**String** that specifies a friendly name for the playlist.</span></span> <span data-ttu-id="3082f-112">In Windows Media Player wird dieser Name in der Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3082f-112">Windows Media Player displays this name in its user interface.</span></span>

</dd> <dt>

<span data-ttu-id="3082f-113">*Lokal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3082f-113">*Local* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3082f-114">**Boolescher** Wert, der angibt, ob die Wiedergabeliste dynamisch oder statisch ist.</span><span class="sxs-lookup"><span data-stu-id="3082f-114">**Boolean** that specifies whether the playlist is dynamic or static.</span></span> <span data-ttu-id="3082f-115">**True** gibt Dynamic an, und **false** gibt Static an.</span><span class="sxs-lookup"><span data-stu-id="3082f-115">**TRUE** specifies dynamic, and **FALSE** specifies static.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3082f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3082f-116">Return value</span></span>

<span data-ttu-id="3082f-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3082f-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3082f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3082f-118">Requirements</span></span>



| <span data-ttu-id="3082f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3082f-119">Requirement</span></span> | <span data-ttu-id="3082f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3082f-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3082f-121">Version</span><span class="sxs-lookup"><span data-stu-id="3082f-121">Version</span></span><br/> | <span data-ttu-id="3082f-122">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="3082f-122">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="3082f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3082f-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="3082f-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3082f-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3082f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3082f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3082f-126">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="3082f-126">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





