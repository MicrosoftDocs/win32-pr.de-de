---
description: Ein herkenzer-Handle wird verwendet, um einen Erkennungs Kontext zu erstellen, die Attribute und Eigenschaften der Erkennungsfunktion abzurufen und zu bestimmen, welche Paket Eigenschaften die Erkennung zum Durchführen der Erkennung benötigt.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: Herkenzer-handle ("recapis. h")
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e78086ff86453ef8b0157bb3b274f3c47be0dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343748"
---
# <a name="hrecognizer-handle"></a><span data-ttu-id="7ec54-103">Herkenzer-handle</span><span class="sxs-lookup"><span data-stu-id="7ec54-103">HRECOGNIZER Handle</span></span>

<span data-ttu-id="7ec54-104">Ein **herkenzer** -Handle wird verwendet, um einen Erkennungs Kontext zu erstellen, die Attribute und Eigenschaften der Erkennungsfunktion abzurufen und zu bestimmen, welche Paket Eigenschaften die Erkennung zum Durchführen der Erkennung benötigt.</span><span class="sxs-lookup"><span data-stu-id="7ec54-104">An **HRECOGNIZER** handle is used to create a recognizer context, retrieve the recognizer's attributes and properties, and determine which packet properties the recognizer requires to perform recognition.</span></span>


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a><span data-ttu-id="7ec54-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ec54-105">Remarks</span></span>

<span data-ttu-id="7ec54-106">Die folgenden Funktionen verwenden einen **herkenzer**.</span><span class="sxs-lookup"><span data-stu-id="7ec54-106">The following functions use an **HRECOGNIZER**.</span></span>



| <span data-ttu-id="7ec54-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="7ec54-107">Function</span></span>                                                               | <span data-ttu-id="7ec54-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ec54-108">Description</span></span>                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ec54-109">**"Kreaterecognizer"**</span><span class="sxs-lookup"><span data-stu-id="7ec54-109">**CreateRecognizer**</span></span>](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | <span data-ttu-id="7ec54-110">Erstellt eine Erkennung.</span><span class="sxs-lookup"><span data-stu-id="7ec54-110">Creates a recognizer.</span></span><br/>                                                                   |
| [<span data-ttu-id="7ec54-111">**Destroyerkenzer**</span><span class="sxs-lookup"><span data-stu-id="7ec54-111">**DestroyRecognizer**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | <span data-ttu-id="7ec54-112">Zerstört eine Erkennung.</span><span class="sxs-lookup"><span data-stu-id="7ec54-112">Destroys a recognizer.</span></span><br/>                                                                  |
| [<span data-ttu-id="7ec54-113">**Getrecoattribute**</span><span class="sxs-lookup"><span data-stu-id="7ec54-113">**GetRecoAttributes**</span></span>](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | <span data-ttu-id="7ec54-114">Gibt die Attribute des Erkennungs Moduls zurück.</span><span class="sxs-lookup"><span data-stu-id="7ec54-114">Returns the attributes of the recognizer.</span></span><br/>                                               |
| [<span data-ttu-id="7ec54-115">**CreateContext**</span><span class="sxs-lookup"><span data-stu-id="7ec54-115">**CreateContext**</span></span>](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | <span data-ttu-id="7ec54-116">Erstellt einen Erkennungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="7ec54-116">Creates a recognizer context.</span></span><br/>                                                           |
| [<span data-ttu-id="7ec54-117">**Destroycontext**</span><span class="sxs-lookup"><span data-stu-id="7ec54-117">**DestroyContext**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | <span data-ttu-id="7ec54-118">Zerstört einen Erkennungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="7ec54-118">Destroys a recognizer context.</span></span><br/>                                                          |
| [<span data-ttu-id="7ec54-119">**Getallerkenzers**</span><span class="sxs-lookup"><span data-stu-id="7ec54-119">**GetAllRecognizers**</span></span>](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | <span data-ttu-id="7ec54-120">Ruft alle erkenzer ab.</span><span class="sxs-lookup"><span data-stu-id="7ec54-120">Gets all recognizers.</span></span><br/>                                                                   |
| [<span data-ttu-id="7ec54-121">**Getresultpropertylist**</span><span class="sxs-lookup"><span data-stu-id="7ec54-121">**GetResultPropertyList**</span></span>](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | <span data-ttu-id="7ec54-122">Ruft eine Liste von Eigenschaften ab, die die Erkennung für einen Ergebnisbereich zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="7ec54-122">Retrieves a list of properties the recognizer can return for a result range.</span></span><br/>            |
| [<span data-ttu-id="7ec54-123">**Getpreferredpacketdescription**</span><span class="sxs-lookup"><span data-stu-id="7ec54-123">**GetPreferredPacketDescription**</span></span>](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | <span data-ttu-id="7ec54-124">Ruft eine Paketbeschreibung ab, die die Paket Eigenschaften enthält, die die Erkennung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ec54-124">Retrieves a packet description that contains the packet properties the recognizer uses.</span></span><br/> |
| [<span data-ttu-id="7ec54-125">**GetUnicodeRanges**</span><span class="sxs-lookup"><span data-stu-id="7ec54-125">**GetUnicodeRanges**</span></span>](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | <span data-ttu-id="7ec54-126">Ruft die Bereiche von Unicode-Punkten ab, die von der Erkennung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7ec54-126">Retrieves the ranges of Unicode points that the recognizer supports.</span></span><br/>                    |
| [<span data-ttu-id="7ec54-127">**Loadcachedattributes**</span><span class="sxs-lookup"><span data-stu-id="7ec54-127">**LoadCachedAttributes**</span></span>](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | <span data-ttu-id="7ec54-128">Lädt die zwischengespeicherten Attribute einer Erkennung.</span><span class="sxs-lookup"><span data-stu-id="7ec54-128">Loads the cached attributes of a recognizer.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="7ec54-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ec54-129">Requirements</span></span>



| <span data-ttu-id="7ec54-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ec54-130">Requirement</span></span> | <span data-ttu-id="7ec54-131">Wert</span><span class="sxs-lookup"><span data-stu-id="7ec54-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec54-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ec54-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7ec54-133">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ec54-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="7ec54-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ec54-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7ec54-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7ec54-135">None supported</span></span><br/>                                                            |
| <span data-ttu-id="7ec54-136">Header</span><span class="sxs-lookup"><span data-stu-id="7ec54-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ec54-137"><dt>"Recapis. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7ec54-137"><dt>Recapis.h</dt></span></span> </dl> |



 

 




