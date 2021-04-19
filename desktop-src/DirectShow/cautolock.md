---
description: Die cautolock-Klasse enthält einen kritischen Abschnitt für den Bereich eines Codeblocks.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: Cautolock-Klasse (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 866ca7164fdaef5a93679da000779c51fb4ddb24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356477"
---
# <a name="cautolock-class"></a><span data-ttu-id="89665-103">Cautolock-Klasse</span><span class="sxs-lookup"><span data-stu-id="89665-103">CAutoLock class</span></span>

<span data-ttu-id="89665-104">Die- `CAutoLock` Klasse enthält einen kritischen Abschnitt für den Bereich eines Codeblocks.</span><span class="sxs-lookup"><span data-stu-id="89665-104">The `CAutoLock` class holds a critical section for the scope of a code block.</span></span>

<span data-ttu-id="89665-105">Diese Klasse funktioniert in Verbindung mit der [**ccritsec**](ccritsec.md) -Klasse, bei der es sich um einen Wrapper für kritische Abschnitts Objekte handelt.</span><span class="sxs-lookup"><span data-stu-id="89665-105">This class works in conjunction with the [**CCritSec**](ccritsec.md) class, which is a wrapper for critical section objects.</span></span> <span data-ttu-id="89665-106">Der `CAutoLock` -Konstruktor sperrt den kritischen Abschnitt, und der Dekonstruktor entsperrt ihn.</span><span class="sxs-lookup"><span data-stu-id="89665-106">The `CAutoLock` constructor locks the critical section, and the destructor unlocks it.</span></span> <span data-ttu-id="89665-107">Indem Sie ein- `CAutoLock` Objekt als lokale Variable verwenden, können Sie einen kritischen Abschnitt mit der Garantie sperren, dass alle Codepfade den kritischen Abschnitt entsperren werden.</span><span class="sxs-lookup"><span data-stu-id="89665-107">By using a `CAutoLock` object as a local variable, you can lock a critical section with the guarantee that all code paths will unlock the critical section.</span></span>

<span data-ttu-id="89665-108">Im folgenden Codebeispiel wird gezeigt, wie diese Klasse verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="89665-108">The following code example shows how to use this class:</span></span>


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



<span data-ttu-id="89665-109">Die Methoden in dieser Klasse können nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="89665-109">The methods in this class are not designed to be overridden.</span></span>



| <span data-ttu-id="89665-110">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="89665-110">Protected Member Variables</span></span>                 | <span data-ttu-id="89665-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89665-111">Description</span></span>                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="89665-112">**m \_ Plock**</span><span class="sxs-lookup"><span data-stu-id="89665-112">**m\_pLock**</span></span>](cautolock-m-plock.md)      | <span data-ttu-id="89665-113">Kritischer Abschnitt für diese Sperre.</span><span class="sxs-lookup"><span data-stu-id="89665-113">Critical section for this lock.</span></span>                                  |
| <span data-ttu-id="89665-114">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="89665-114">Public Methods</span></span>                             | <span data-ttu-id="89665-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89665-115">Description</span></span>                                                      |
| [<span data-ttu-id="89665-116">**Cautolock**</span><span class="sxs-lookup"><span data-stu-id="89665-116">**CAutoLock**</span></span>](cautolock-cautolock.md)   | <span data-ttu-id="89665-117">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="89665-117">Constructor method.</span></span> <span data-ttu-id="89665-118">Sperrt das angegebene kritische Abschnitts Objekt.</span><span class="sxs-lookup"><span data-stu-id="89665-118">Locks the specified critical section object.</span></span> |
| [<span data-ttu-id="89665-119">**~ Cautolock**</span><span class="sxs-lookup"><span data-stu-id="89665-119">**~CAutoLock**</span></span>](cautolock--cautolock.md) | <span data-ttu-id="89665-120">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="89665-120">Destructor method.</span></span> <span data-ttu-id="89665-121">Entsperrt das Objekt des kritischen Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="89665-121">Unlocks the critical section object.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="89665-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89665-122">Requirements</span></span>



| <span data-ttu-id="89665-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89665-123">Requirement</span></span> | <span data-ttu-id="89665-124">Wert</span><span class="sxs-lookup"><span data-stu-id="89665-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89665-125">Header</span><span class="sxs-lookup"><span data-stu-id="89665-125">Header</span></span><br/>  | <dl> <span data-ttu-id="89665-126"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89665-126"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="89665-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="89665-127">Library</span></span><br/> | <dl> <span data-ttu-id="89665-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="89665-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




