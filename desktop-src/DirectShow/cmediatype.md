---
description: Die cmediatype-Klasse verwaltet Medientypen. Diese Klasse erbt die am \_ \_ Medientyp-Struktur. Sie kann in eine Variable vom Typ "am Medientyp" umgewandelt werden \_ \_ .
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: Cmediatype-Klasse (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f91578f91840c316347c6266e678357e31c8a284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364930"
---
# <a name="cmediatype-class"></a><span data-ttu-id="a695b-105">Cmediatype-Klasse</span><span class="sxs-lookup"><span data-stu-id="a695b-105">CMediaType class</span></span>

![cmediatype-Klassenhierarchie](images/mtype01.png)

<span data-ttu-id="a695b-107">Die- `CMediaType` Klasse verwaltet Medientypen.</span><span class="sxs-lookup"><span data-stu-id="a695b-107">The `CMediaType` class manages media types.</span></span> <span data-ttu-id="a695b-108">Diese Klasse erbt die [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a695b-108">This class inherits the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="a695b-109">Sie kann in eine Variable vom Typ " **am \_ \_ Medientyp**" umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="a695b-109">It can be cast to a variable of type **AM\_MEDIA\_TYPE**.</span></span>



| <span data-ttu-id="a695b-110">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="a695b-110">Public Methods</span></span>                                                      | <span data-ttu-id="a695b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a695b-111">Description</span></span>                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="a695b-112">**Cmediatype**</span><span class="sxs-lookup"><span data-stu-id="a695b-112">**CMediaType**</span></span>](cmediatype-cmediatype.md)                         | <span data-ttu-id="a695b-113">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="a695b-113">Constructor method.</span></span>                                                            |
| [<span data-ttu-id="a695b-114">**~ Cmediatype**</span><span class="sxs-lookup"><span data-stu-id="a695b-114">**~CMediaType**</span></span>](cmediatype--cmediatype.md)                       | <span data-ttu-id="a695b-115">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="a695b-115">Destructor method.</span></span>                                                             |
| [<span data-ttu-id="a695b-116">**Set**</span><span class="sxs-lookup"><span data-stu-id="a695b-116">**Set**</span></span>](cmediatype-set.md)                                       | <span data-ttu-id="a695b-117">Legt den Medientyp von einem anderen Medientyp fest.</span><span class="sxs-lookup"><span data-stu-id="a695b-117">Sets the media type from another media type.</span></span>                                   |
| [<span data-ttu-id="a695b-118">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="a695b-118">**IsValid**</span></span>](cmediatype-isvalid.md)                               | <span data-ttu-id="a695b-119">Bestimmt, ob diesem-Objekt ein Haupttyp zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="a695b-119">Determines whether a major type has been assigned to this object.</span></span>              |
| [<span data-ttu-id="a695b-120">**type**</span><span class="sxs-lookup"><span data-stu-id="a695b-120">**Type**</span></span>](cmediatype-type.md)                                     | <span data-ttu-id="a695b-121">Ruft den Haupttyp ab.</span><span class="sxs-lookup"><span data-stu-id="a695b-121">Retrieves the major type.</span></span>                                                      |
| [<span data-ttu-id="a695b-122">**Settype**</span><span class="sxs-lookup"><span data-stu-id="a695b-122">**SetType**</span></span>](cmediatype-settype.md)                               | <span data-ttu-id="a695b-123">Gibt den Haupttyp an.</span><span class="sxs-lookup"><span data-stu-id="a695b-123">Specifies the major type.</span></span>                                                      |
| [<span data-ttu-id="a695b-124">**Untertyp**</span><span class="sxs-lookup"><span data-stu-id="a695b-124">**Subtype**</span></span>](cmediatype-subtype.md)                               | <span data-ttu-id="a695b-125">Ruft den Untertyp ab.</span><span class="sxs-lookup"><span data-stu-id="a695b-125">Retrieves the subtype.</span></span>                                                         |
| [<span data-ttu-id="a695b-126">**Setsubtype**</span><span class="sxs-lookup"><span data-stu-id="a695b-126">**SetSubtype**</span></span>](cmediatype-setsubtype.md)                         | <span data-ttu-id="a695b-127">Gibt den Untertyp an.</span><span class="sxs-lookup"><span data-stu-id="a695b-127">Specifies the subtype.</span></span>                                                         |
| [<span data-ttu-id="a695b-128">**IsFixedSize**</span><span class="sxs-lookup"><span data-stu-id="a695b-128">**IsFixedSize**</span></span>](cmediatype-isfixedsize.md)                       | <span data-ttu-id="a695b-129">Bestimmt, ob die Stichproben eine festgelegte Größe oder eine Variable Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a695b-129">Determines if the samples have a fixed size or a variable size.</span></span>                |
| [<span data-ttu-id="a695b-130">**Istemporalcompressed**</span><span class="sxs-lookup"><span data-stu-id="a695b-130">**IsTemporalCompressed**</span></span>](cmediatype-istemporalcompressed.md)     | <span data-ttu-id="a695b-131">Bestimmt, ob der Stream Temporale Komprimierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a695b-131">Determines if the stream uses temporal compression.</span></span>                            |
| [<span data-ttu-id="a695b-132">**GetSampleSize**</span><span class="sxs-lookup"><span data-stu-id="a695b-132">**GetSampleSize**</span></span>](cmediatype-getsamplesize.md)                   | <span data-ttu-id="a695b-133">Ruft die Stichprobengröße ab.</span><span class="sxs-lookup"><span data-stu-id="a695b-133">Retrieves the sample size.</span></span>                                                     |
| [<span data-ttu-id="a695b-134">**Setsamplesize**</span><span class="sxs-lookup"><span data-stu-id="a695b-134">**SetSampleSize**</span></span>](cmediatype-setsamplesize.md)                   | <span data-ttu-id="a695b-135">Gibt eine festgelegte Stichprobengröße an oder gibt an, dass Beispiele eine Variable Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a695b-135">Specifies a fixed sample size, or specifies that samples have a variable size.</span></span> |
| [<span data-ttu-id="a695b-136">**Setvariablesize**</span><span class="sxs-lookup"><span data-stu-id="a695b-136">**SetVariableSize**</span></span>](cmediatype-setvariablesize.md)               | <span data-ttu-id="a695b-137">Gibt an, dass die Stichproben keine festgelegte Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a695b-137">Specifies that samples do not have a fixed size.</span></span>                               |
| [<span data-ttu-id="a695b-138">**Settemporalcompression**</span><span class="sxs-lookup"><span data-stu-id="a695b-138">**SetTemporalCompression**</span></span>](cmediatype-settemporalcompression.md) | <span data-ttu-id="a695b-139">Gibt an, ob Samples mithilfe der temporalen Komprimierung komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="a695b-139">Specifies whether samples are compressed using temporal compression.</span></span>           |
| [<span data-ttu-id="a695b-140">**Ges**</span><span class="sxs-lookup"><span data-stu-id="a695b-140">**Format**</span></span>](cmediatype-format.md)                                 | <span data-ttu-id="a695b-141">Ruft einen Zeiger auf den Format Block ab.</span><span class="sxs-lookup"><span data-stu-id="a695b-141">Retrieves a pointer to the format block.</span></span>                                       |
| [<span data-ttu-id="a695b-142">**Formatlength**</span><span class="sxs-lookup"><span data-stu-id="a695b-142">**FormatLength**</span></span>](cmediatype-formatlength.md)                     | <span data-ttu-id="a695b-143">Ruft die Länge des Format Blocks ab.</span><span class="sxs-lookup"><span data-stu-id="a695b-143">Retrieves the length of the format block.</span></span>                                      |
| [<span data-ttu-id="a695b-144">**Setformattype**</span><span class="sxs-lookup"><span data-stu-id="a695b-144">**SetFormatType**</span></span>](cmediatype-setformattype.md)                   | <span data-ttu-id="a695b-145">Gibt den Formattyp an</span><span class="sxs-lookup"><span data-stu-id="a695b-145">Specifies the format type.</span></span>                                                     |
| [<span data-ttu-id="a695b-146">**Format Type**</span><span class="sxs-lookup"><span data-stu-id="a695b-146">**FormatType**</span></span>](cmediatype-formattype.md)                         | <span data-ttu-id="a695b-147">Ruft den Formattyp ab.</span><span class="sxs-lookup"><span data-stu-id="a695b-147">Retrieves the format type.</span></span>                                                     |
| [<span data-ttu-id="a695b-148">**SetFormat**</span><span class="sxs-lookup"><span data-stu-id="a695b-148">**SetFormat**</span></span>](cmediatype-setformat.md)                           | <span data-ttu-id="a695b-149">Gibt den Format Block an.</span><span class="sxs-lookup"><span data-stu-id="a695b-149">Specifies the format block.</span></span>                                                    |
| [<span data-ttu-id="a695b-150">**Resetformatbuffer**</span><span class="sxs-lookup"><span data-stu-id="a695b-150">**ResetFormatBuffer**</span></span>](cmediatype-resetformatbuffer.md)           | <span data-ttu-id="a695b-151">Löscht den Format Block.</span><span class="sxs-lookup"><span data-stu-id="a695b-151">Deletes the format block.</span></span>                                                      |
| [<span data-ttu-id="a695b-152">**"Zuweisung"**</span><span class="sxs-lookup"><span data-stu-id="a695b-152">**AllocFormatBuffer**</span></span>](cmediatype-allocformatbuffer.md)           | <span data-ttu-id="a695b-153">Weist Speicher für den Format Block zu.</span><span class="sxs-lookup"><span data-stu-id="a695b-153">Allocates memory for the format block.</span></span>                                         |
| [<span data-ttu-id="a695b-154">**Rezuweisung von formatbuffer**</span><span class="sxs-lookup"><span data-stu-id="a695b-154">**ReallocFormatBuffer**</span></span>](cmediatype-reallocformatbuffer.md)       | <span data-ttu-id="a695b-155">Ordnet den Format Block neu einer neuen Größe zu.</span><span class="sxs-lookup"><span data-stu-id="a695b-155">Reallocates the format block to a new size.</span></span>                                    |
| [<span data-ttu-id="a695b-156">**Initmediatype**</span><span class="sxs-lookup"><span data-stu-id="a695b-156">**InitMediaType**</span></span>](cmediatype-initmediatype.md)                   | <span data-ttu-id="a695b-157">Initialisiert den Medientyp.</span><span class="sxs-lookup"><span data-stu-id="a695b-157">Initializes the media type.</span></span>                                                    |
| [<span data-ttu-id="a695b-158">**Matchespartial**</span><span class="sxs-lookup"><span data-stu-id="a695b-158">**MatchesPartial**</span></span>](cmediatype-matchespartial.md)                 | <span data-ttu-id="a695b-159">Bestimmt, ob dieser Medientyp mit einem teilweise angegebenen Medientyp übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="a695b-159">Determines if this media type matches a partially specified media type.</span></span>        |
| [<span data-ttu-id="a695b-160">**Ispartiallyspezifiziert**</span><span class="sxs-lookup"><span data-stu-id="a695b-160">**IsPartiallySpecified**</span></span>](cmediatype-ispartiallyspecified.md)     | <span data-ttu-id="a695b-161">Bestimmt, ob der Medientyp teilweise definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a695b-161">Determines if the media type is partially defined.</span></span>                             |
| <span data-ttu-id="a695b-162">Operatoren</span><span class="sxs-lookup"><span data-stu-id="a695b-162">Operators</span></span>                                                           | <span data-ttu-id="a695b-163">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a695b-163">Description</span></span>                                                                    |
| [<span data-ttu-id="a695b-164">**Operator =**</span><span class="sxs-lookup"><span data-stu-id="a695b-164">**operator =**</span></span>](cmediatype-operator-.md)                          | <span data-ttu-id="a695b-165">Über lädt den Zuweisungs Operator zum Kopieren eines Medientyps.</span><span class="sxs-lookup"><span data-stu-id="a695b-165">Overloads the assignment operator to copy a media type.</span></span>                        |
| [<span data-ttu-id="a695b-166">**Operator = =**</span><span class="sxs-lookup"><span data-stu-id="a695b-166">**operator ==**</span></span>](cmediatype-operator--.md)                        | <span data-ttu-id="a695b-167">Prüft auf Gleichheit zwischen `CMediaType`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="a695b-167">Tests for equality between `CMediaType` objects.</span></span>                               |
| [<span data-ttu-id="a695b-168">**Operator! =**</span><span class="sxs-lookup"><span data-stu-id="a695b-168">**operator !=**</span></span>](cmediatype-operator-neq.md)                      | <span data-ttu-id="a695b-169">Prüft auf Ungleichheit zwischen `CMediaType`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="a695b-169">Tests for inequality between `CMediaType` objects.</span></span>                             |



 

## <a name="requirements"></a><span data-ttu-id="a695b-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a695b-170">Requirements</span></span>



| <span data-ttu-id="a695b-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a695b-171">Requirement</span></span> | <span data-ttu-id="a695b-172">Wert</span><span class="sxs-lookup"><span data-stu-id="a695b-172">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a695b-173">Header</span><span class="sxs-lookup"><span data-stu-id="a695b-173">Header</span></span><br/>  | <dl> <span data-ttu-id="a695b-174"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a695b-174"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="a695b-175">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a695b-175">Library</span></span><br/> | <dl> <span data-ttu-id="a695b-176">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a695b-176"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




