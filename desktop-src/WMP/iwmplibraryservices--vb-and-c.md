---
title: Iwmplibraryservices (VB und C)-Schnittstelle (WMP. h)
description: Stellt Methoden zum Aufzählen von Bibliotheken bereit.
ms.assetid: f2a72731-6e61-4f78-b0ca-ae907004eb7d
keywords:
- Windows Media Player der iwmplibraryservices (VB und C)-Schnittstelle
- Iwmplibraryservices (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPLibraryServices (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3493d5c94dcbd9db1e4f281a8fddfadbd2e336f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370539"
---
# <a name="iwmplibraryservices-vb-and-c-interface"></a><span data-ttu-id="b49d2-105">Iwmplibraryservices (VB und c#)-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b49d2-105">IWMPLibraryServices (VB and C#) interface</span></span>

<span data-ttu-id="b49d2-106">Stellt Methoden zum Aufzählen von Bibliotheken bereit.</span><span class="sxs-lookup"><span data-stu-id="b49d2-106">Provides methods to enumerate libraries.</span></span>

## <a name="members"></a><span data-ttu-id="b49d2-107">Member</span><span class="sxs-lookup"><span data-stu-id="b49d2-107">Members</span></span>

<span data-ttu-id="b49d2-108">Die **iwmplibraryservices (VB und c#)** -Schnittstelle verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b49d2-108">The **IWMPLibraryServices (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="b49d2-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="b49d2-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b49d2-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="b49d2-110">Methods</span></span>

<span data-ttu-id="b49d2-111">Die **iwmplibraryservices (VB und c#)** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b49d2-111">The **IWMPLibraryServices (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="b49d2-112">Methode</span><span class="sxs-lookup"><span data-stu-id="b49d2-112">Method</span></span>                                                                                               | <span data-ttu-id="b49d2-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b49d2-113">Description</span></span>                                                                                                        |
|:-----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b49d2-114">**getcountrytbytype**</span><span class="sxs-lookup"><span data-stu-id="b49d2-114">**getCountByType**</span></span>](wmplibiwmplibraryservices-iwmplibraryservices-getcountbytype--vb-and-c.md)     | <span data-ttu-id="b49d2-115">Gibt die Anzahl der verfügbaren Bibliotheken eines angegebenen Typs zurück.</span><span class="sxs-lookup"><span data-stu-id="b49d2-115">Returns the count of available libraries of a specified type.</span></span><br/>                                           |
| [<span data-ttu-id="b49d2-116">**getlibrarybytype**</span><span class="sxs-lookup"><span data-stu-id="b49d2-116">**getLibraryByType**</span></span>](wmplibiwmplibraryservices-iwmplibraryservices-getlibrarybytype--vb-and-c.md) | <span data-ttu-id="b49d2-117">Gibt eine **iwmplibrary** -Schnittstelle zurück, die die Bibliothek mit dem angegebenen Typ und Index darstellt.</span><span class="sxs-lookup"><span data-stu-id="b49d2-117">Returns an **IWMPLibrary** interface that represents the library that has the specified type and index.</span></span><br/> |



 

<span data-ttu-id="b49d2-118">Sie erhalten eine **iwmplibraryservices** -Schnittstelle durch Umwandeln des Objekts, das von der **AxWindowsMediaPlayer. gedecx** -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b49d2-118">Get an **IWMPLibraryServices** interface by casting the object returned from the **AxWindowsMediaPlayer.GetOcx** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b49d2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b49d2-119">Requirements</span></span>



| <span data-ttu-id="b49d2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b49d2-120">Requirement</span></span> | <span data-ttu-id="b49d2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b49d2-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b49d2-122">Header</span><span class="sxs-lookup"><span data-stu-id="b49d2-122">Header</span></span><br/> | <dl> <span data-ttu-id="b49d2-123"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="b49d2-123"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b49d2-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b49d2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b49d2-125">**Schnittstellen für Visual Basic .net und C #**</span><span class="sxs-lookup"><span data-stu-id="b49d2-125">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="b49d2-126">**Iwmplibrary-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="b49d2-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





