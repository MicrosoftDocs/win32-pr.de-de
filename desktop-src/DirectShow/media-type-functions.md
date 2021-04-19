---
description: Die DirectShow-Basisklassen stellen Hilfsfunktionen zum Verarbeiten der am- \_ \_ Medientyp Struktur bereit.
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: Medientyp Funktionen (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Media
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39fe9a9599a1d85c14a226106f5c8d7080b721f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367413"
---
# <a name="media-type-functions"></a><span data-ttu-id="3c9a7-103">Medientyp Funktionen</span><span class="sxs-lookup"><span data-stu-id="3c9a7-103">Media Type Functions</span></span>

<span data-ttu-id="3c9a7-104">Die DirectShow-Basisklassen stellen Hilfsfunktionen zum Verarbeiten der [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur bereit.</span><span class="sxs-lookup"><span data-stu-id="3c9a7-104">The DirectShow base classes provides helper functions for handling the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="3c9a7-105">Die **am \_ \_ Medientyp** -Struktur enthält einen Zeiger (den **pbformat** -Member) zu einem anderen Speicherblock, der als *Format Block* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3c9a7-105">The **AM\_MEDIA\_TYPE** structure contains a pointer (the **pbFormat** member) to another block of memory, which is called the *format block*.</span></span> <span data-ttu-id="3c9a7-106">Wenn Sie mit dieser Struktur arbeiten, müssen Sie daher vorsichtig bei der Speicher Belegung sein, um Speicher Verluste zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="3c9a7-106">When you work with this structure, therefore, you must be careful about memory allocation in order to avoid memory leaks.</span></span>

<span data-ttu-id="3c9a7-107">Die folgenden Funktionen weisen Speicher zu:</span><span class="sxs-lookup"><span data-stu-id="3c9a7-107">The following functions allocate memory:</span></span>

-   <span data-ttu-id="3c9a7-108">Mit " **kreatemediatype** " wird eine neue **am- \_ \_ Medientyp** Struktur und der Format Block zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3c9a7-108">**CreateMediaType** allocates a new **AM\_MEDIA\_TYPE** structure and the format block.</span></span>
-   <span data-ttu-id="3c9a7-109">**Copymediatype** kopiert in eine vorhandene **\_ \_ Medientyp** Struktur, aber weist den Format Block zu.</span><span class="sxs-lookup"><span data-stu-id="3c9a7-109">**CopyMediaType** copies to an existing **AM\_MEDIA\_TYPE** structure, but allocates the format block.</span></span>
-   <span data-ttu-id="3c9a7-110">" **Tinateaudiomediatype** " Initialisiert eine vorhandene **am- \_ \_ Medientyp** Struktur und weist optional den Format Block zu.</span><span class="sxs-lookup"><span data-stu-id="3c9a7-110">**CreateAudioMediaType** initializes an existing **AM\_MEDIA\_TYPE** structure, and optionally allocates the format block.</span></span>

<span data-ttu-id="3c9a7-111">Die folgenden Funktionen können Arbeitsspeicher freigeben:</span><span class="sxs-lookup"><span data-stu-id="3c9a7-111">The following functions free memory:</span></span>

-   <span data-ttu-id="3c9a7-112">" **Freimediatype** " gibt den Format Block frei.</span><span class="sxs-lookup"><span data-stu-id="3c9a7-112">**FreeMediaType** releases the format block.</span></span>
-   <span data-ttu-id="3c9a7-113">**Deletemediatype** gibt eine **am \_ \_ Medientyp** -Struktur frei, einschließlich des Format Blocks.</span><span class="sxs-lookup"><span data-stu-id="3c9a7-113">**DeleteMediaType** frees an **AM\_MEDIA\_TYPE** structure, including the format block.</span></span>



| <span data-ttu-id="3c9a7-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="3c9a7-114">Function</span></span>                                             | <span data-ttu-id="3c9a7-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c9a7-115">Description</span></span>                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c9a7-116">**Copymediatype**</span><span class="sxs-lookup"><span data-stu-id="3c9a7-116">**CopyMediaType**</span></span>](copymediatype.md)               | <span data-ttu-id="3c9a7-117">Kopiert eine Aufgabe zugewiesene **am \_ \_ Medientyp** Struktur.</span><span class="sxs-lookup"><span data-stu-id="3c9a7-117">Copies a task-allocated **AM\_MEDIA\_TYPE** structure.</span></span>                                                      |
| [<span data-ttu-id="3c9a7-118">**"Kreateaudiomediatype"**</span><span class="sxs-lookup"><span data-stu-id="3c9a7-118">**CreateAudioMediaType**</span></span>](createaudiomediatype.md) | <span data-ttu-id="3c9a7-119">Initialisiert eine Medientyp Struktur, wenn eine Wave-Format-Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3c9a7-119">Initializes a media type structure given a wave format structure.</span></span>                                           |
| [<span data-ttu-id="3c9a7-120">**"Kreatemediatype"**</span><span class="sxs-lookup"><span data-stu-id="3c9a7-120">**CreateMediaType**</span></span>](createmediatype.md)           | <span data-ttu-id="3c9a7-121">Ordnet eine **am- \_ \_ Medientyp** Struktur zu und initialisiert sie aus einer vorhandenen **am- \_ \_ Medientyp** Struktur.</span><span class="sxs-lookup"><span data-stu-id="3c9a7-121">Allocates and initializes an **AM\_MEDIA\_TYPE** structure, from an existing **AM\_MEDIA\_TYPE** structure.</span></span> |
| [<span data-ttu-id="3c9a7-122">**Deletemediatype**</span><span class="sxs-lookup"><span data-stu-id="3c9a7-122">**DeleteMediaType**</span></span>](deletemediatype.md)           | <span data-ttu-id="3c9a7-123">Löscht eine Aufgabe zugewiesene **am \_ \_ Medientyp** Struktur.</span><span class="sxs-lookup"><span data-stu-id="3c9a7-123">Deletes a task-allocated **AM\_MEDIA\_TYPE** structure.</span></span>                                                     |
| [<span data-ttu-id="3c9a7-124">**Freimediatype**</span><span class="sxs-lookup"><span data-stu-id="3c9a7-124">**FreeMediaType**</span></span>](freemediatype.md)               | <span data-ttu-id="3c9a7-125">Gibt eine Aufgaben zugewiesene **am \_ \_ Medientyp** -Struktur aus dem Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="3c9a7-125">Frees a task-allocated **AM\_MEDIA\_TYPE** structure from memory.</span></span>                                           |



 

## <a name="requirements"></a><span data-ttu-id="3c9a7-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c9a7-126">Requirements</span></span>



| <span data-ttu-id="3c9a7-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c9a7-127">Requirement</span></span> | <span data-ttu-id="3c9a7-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3c9a7-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c9a7-129">Header</span><span class="sxs-lookup"><span data-stu-id="3c9a7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3c9a7-130"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c9a7-130"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="3c9a7-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3c9a7-131">Library</span></span><br/> | <dl> <span data-ttu-id="3c9a7-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3c9a7-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




