---
description: Wird von Anwendungen verwendet, um IWiaItem2-Objekte im aktuellen Ordner der Elementstruktur aufzulisten.
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: IEnumWiaItem2-Schnittstelle (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f6e41b3172793f696a9ea3c2d319bdee6ca3d691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348453"
---
# <a name="ienumwiaitem2-interface"></a><span data-ttu-id="babf5-103">IEnumWiaItem2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="babf5-103">IEnumWiaItem2 interface</span></span>

<span data-ttu-id="babf5-104">Wird von Anwendungen verwendet, um [**IWiaItem2**](-wia-iwiaitem2.md) -Objekte im aktuellen Ordner der Elementstruktur aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="babf5-104">Used by applications to enumerate [**IWiaItem2**](-wia-iwiaitem2.md) objects in the item tree's current folder.</span></span>

## <a name="members"></a><span data-ttu-id="babf5-105">Member</span><span class="sxs-lookup"><span data-stu-id="babf5-105">Members</span></span>

<span data-ttu-id="babf5-106">Die **IEnumWiaItem2** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="babf5-106">The **IEnumWiaItem2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="babf5-107">**IEnumWiaItem2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="babf5-107">**IEnumWiaItem2** also has these types of members:</span></span>

-   [<span data-ttu-id="babf5-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="babf5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="babf5-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="babf5-109">Methods</span></span>

<span data-ttu-id="babf5-110">Die **IEnumWiaItem2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="babf5-110">The **IEnumWiaItem2** interface has these methods.</span></span>



| <span data-ttu-id="babf5-111">Methode</span><span class="sxs-lookup"><span data-stu-id="babf5-111">Method</span></span>                                          | <span data-ttu-id="babf5-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="babf5-112">Description</span></span>                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="babf5-113">**Klon**</span><span class="sxs-lookup"><span data-stu-id="babf5-113">**Clone**</span></span>](-wia-ienumwiaitem2-clone.md)       | <span data-ttu-id="babf5-114">Erstellt eine zusätzliche Instanz der **IEnumWiaItem2** -Schnittstelle und sendet einen Zeiger darauf zurück.</span><span class="sxs-lookup"><span data-stu-id="babf5-114">Creates an additional instance of the **IEnumWiaItem2** interface and sends back a pointer to it.</span></span> <br/>                  |
| [<span data-ttu-id="babf5-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="babf5-115">**GetCount**</span></span>](-wia-ienumwiaitem2-getcount.md) | <span data-ttu-id="babf5-116">Gibt die Anzahl von Elementen zurück, die von diesem Enumerator gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="babf5-116">Returns the number of elements stored by this enumerator.</span></span> <br/>                                                          |
| [<span data-ttu-id="babf5-117">**Weiter**</span><span class="sxs-lookup"><span data-stu-id="babf5-117">**Next**</span></span>](-wia-ienumwiaitem2-next.md)         | <span data-ttu-id="babf5-118">Füllt ein Array von Zeigern auf [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstellen auf.</span><span class="sxs-lookup"><span data-stu-id="babf5-118">Fills an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span><br/>                                       |
| [<span data-ttu-id="babf5-119">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="babf5-119">**Reset**</span></span>](-wia-ienumwiaitem2-reset.md)       | <span data-ttu-id="babf5-120">Setzt den enumerationsverweis auf das erste [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="babf5-120">Resets the enumeration reference to the first [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span> <br/>                          |
| [<span data-ttu-id="babf5-121">**Überspringen**</span><span class="sxs-lookup"><span data-stu-id="babf5-121">**Skip**</span></span>](-wia-ienumwiaitem2-skip.md)         | <span data-ttu-id="babf5-122">Überspringt die angegebene Anzahl von Elementen während einer Enumeration verfügbarer [**IWiaItem2**](-wia-iwiaitem2.md) -Objekte.</span><span class="sxs-lookup"><span data-stu-id="babf5-122">Skips the specified number of items during an enumeration of available [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="babf5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="babf5-123">Requirements</span></span>



| <span data-ttu-id="babf5-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="babf5-124">Requirement</span></span> | <span data-ttu-id="babf5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="babf5-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="babf5-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="babf5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="babf5-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="babf5-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="babf5-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="babf5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="babf5-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="babf5-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="babf5-130">Header</span><span class="sxs-lookup"><span data-stu-id="babf5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="babf5-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="babf5-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="babf5-132">IDL</span><span class="sxs-lookup"><span data-stu-id="babf5-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="babf5-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="babf5-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 
