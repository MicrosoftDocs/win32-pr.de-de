---
title: WINBIO_BDB_ANSI_381_RECORD Struktur (winbio \_ types. h)
description: Enthält Informationen zu einem einzelnen Fingerabdruck oder einem Palmen Beispiel von einem Endbenutzer.
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- WINBIO_BDB_ANSI_381_RECORD Struktur Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_RECORD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30af31d88349dbe02066f231cdff21293aebe90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391570"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a><span data-ttu-id="11f72-104">Struktur von winbio \_ BDB \_ ANSI \_ 381- \_ Datensätzen</span><span class="sxs-lookup"><span data-stu-id="11f72-104">WINBIO\_BDB\_ANSI\_381\_RECORD structure</span></span>

<span data-ttu-id="11f72-105">Die Struktur von **winbio \_ BDB \_ ANSI \_ 381 \_** -Datensätzen enthält Informationen zu einem einzelnen Fingerabdruck oder einem Palmen Beispiel von einem Endbenutzer.</span><span class="sxs-lookup"><span data-stu-id="11f72-105">The **WINBIO\_BDB\_ANSI\_381\_RECORD** structure contains information about a single fingerprint or palm sample from an end user.</span></span> <span data-ttu-id="11f72-106">Eine Auflistung dieser Strukturen ist in jeder [**winbio \_ BDB- \_ ANSI \_ 381- \_ Header**](winbio-bdb-ansi-381-header.md) Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="11f72-106">A collection of these structures is included in each [**WINBIO\_BDB\_ANSI\_381\_HEADER**](winbio-bdb-ansi-381-header.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f72-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="11f72-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BDB_ANSI_381_RECORD {
  ULONG                    BlockLength;
  USHORT                   HorizontalLineLength;
  USHORT                   VerticalLineLength;
  WINBIO_BIOMETRIC_SUBTYPE Position;
  UCHAR                    CountOfViews;
  UCHAR                    ViewNumber;
  UCHAR                    ImageQuality;
  UCHAR                    ImpressionType;
  UCHAR                    Reserved;
} WINBIO_BDB_ANSI_381_RECORD;
```



## <a name="members"></a><span data-ttu-id="11f72-108">Member</span><span class="sxs-lookup"><span data-stu-id="11f72-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="11f72-109">**Blocklength**</span><span class="sxs-lookup"><span data-stu-id="11f72-109">**BlockLength**</span></span>
</dt> <dd>

<span data-ttu-id="11f72-110">Enthält die Anzahl der Bytes in dieser Struktur zuzüglich der Anzahl von Bytes von Beispiel Bilddaten.</span><span class="sxs-lookup"><span data-stu-id="11f72-110">Contains the number of bytes in this structure plus the number of bytes of sample image data.</span></span>

</dd> <dt>

<span data-ttu-id="11f72-111">**Horizontallinelength**</span><span class="sxs-lookup"><span data-stu-id="11f72-111">**HorizontalLineLength**</span></span>
</dt> <dd>

<span data-ttu-id="11f72-112">Gibt die Anzahl der Pixel in einer horizontalen Zeile des Beispiels an.</span><span class="sxs-lookup"><span data-stu-id="11f72-112">Specifies the number of pixels in a horizontal line of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="11f72-113">**Verticallinelength**</span><span class="sxs-lookup"><span data-stu-id="11f72-113">**VerticalLineLength**</span></span>
</dt> <dd>

<span data-ttu-id="11f72-114">Gibt die Anzahl der Pixel in einer vertikalen Zeile des Beispiels an.</span><span class="sxs-lookup"><span data-stu-id="11f72-114">Specifies the number of pixels in a vertical line of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="11f72-115">**Position**</span><span class="sxs-lookup"><span data-stu-id="11f72-115">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="11f72-116">Ein Wert des **Typs "winbio \_ biometrische \_ SubType** ", der den Finger oder die Palme angibt, mit dem das biometrische Beispiel generiert wird.</span><span class="sxs-lookup"><span data-stu-id="11f72-116">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that specifies the finger or palm used to generate the biometric sample.</span></span> <span data-ttu-id="11f72-117">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="11f72-117">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="11f72-118">**Ansichts Ansichten**</span><span class="sxs-lookup"><span data-stu-id="11f72-118">**CountOfViews**</span></span>
</dt> <dd>

<span data-ttu-id="11f72-119">Diese muss auf 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="11f72-119">This must be set to one (1);</span></span>

</dd> <dt>

<span data-ttu-id="11f72-120">**Viewnumber**</span><span class="sxs-lookup"><span data-stu-id="11f72-120">**ViewNumber**</span></span>
</dt> <dd>

<span data-ttu-id="11f72-121">Diese muss auf 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="11f72-121">This must be set to one (1);</span></span>

</dd> <dt>

<span data-ttu-id="11f72-122">**ImageQuality**</span><span class="sxs-lookup"><span data-stu-id="11f72-122">**ImageQuality**</span></span>
</dt> <dd>

<span data-ttu-id="11f72-123">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="11f72-123">Reserved.</span></span> <span data-ttu-id="11f72-124">Dies muss 254 (0xFE) sein.</span><span class="sxs-lookup"><span data-stu-id="11f72-124">This must be 254 (0xFE).</span></span>

</dd> <dt>

<span data-ttu-id="11f72-125">**Impressiontype**</span><span class="sxs-lookup"><span data-stu-id="11f72-125">**ImpressionType**</span></span>
</dt> <dd>

<span data-ttu-id="11f72-126">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="11f72-126">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="11f72-127">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="11f72-127">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="11f72-128">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="11f72-128">Reserved.</span></span> <span data-ttu-id="11f72-129">Muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="11f72-129">Must be set to zero (0).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11f72-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11f72-130">Remarks</span></span>

<span data-ttu-id="11f72-131">Der *Positions* Member gibt den Bereich der Hand oder der Palme an, der zum Erstellen des biometrischen Beispiels verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="11f72-131">The *Position* member specifies the area of the hand or palm used to make the biometric sample.</span></span> <span data-ttu-id="11f72-132">Der Windows-Biometrieframework (WBF) unterstützt derzeit nur die Fingerabdruck Erfassung und verwendet die folgenden Konstanten, um Positionsinformationen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="11f72-132">The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent position information.</span></span>

-   <span data-ttu-id="11f72-133">Winbio \_ ANSI \_ 381 Torys \_ \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="11f72-133">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="11f72-134">Winbio \_ ANSI \_ 381 \_ POS, \_ RH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="11f72-134">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="11f72-135">Winbio \_ ANSI \_ 381 POS-Zeige- \_ \_ \_ \_ Finger</span><span class="sxs-lookup"><span data-stu-id="11f72-135">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="11f72-136">Winbio \_ ANSI \_ 381 \_ Torpo- \_ \_ \_ Mittelfinger</span><span class="sxs-lookup"><span data-stu-id="11f72-136">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="11f72-137">Winbio \_ ANSI \_ 381 \_ POS, \_ RH- \_ Klingel \_ Finger</span><span class="sxs-lookup"><span data-stu-id="11f72-137">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="11f72-138">Winbio \_ ANSI \_ 381 Torys \_ \_ RH \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="11f72-138">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="11f72-139">Winbio \_ ANSI \_ 381 \_ POS \_ LH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="11f72-139">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="11f72-140">Winbio \_ ANSI \_ 381 Torys \_ \_ LH \_ Index \_ Finger</span><span class="sxs-lookup"><span data-stu-id="11f72-140">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="11f72-141">Winbio \_ ANSI \_ 381 \_ POS \_ - \_ Mittel \_ Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="11f72-141">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="11f72-142">Winbio \_ ANSI \_ 381 Torys LH- \_ \_ \_ Klingel \_ Finger</span><span class="sxs-lookup"><span data-stu-id="11f72-142">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="11f72-143">Winbio \_ ANSI \_ 381 Torys \_ \_ LH \_ wenig \_ Finger</span><span class="sxs-lookup"><span data-stu-id="11f72-143">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="11f72-144">Winbio \_ ANSI 381 Torys mit \_ \_ \_ \_ vier \_ Fingern</span><span class="sxs-lookup"><span data-stu-id="11f72-144">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="11f72-145">Winbio \_ ANSI 381 Torys mit \_ \_ \_ \_ vier \_ Fingern</span><span class="sxs-lookup"><span data-stu-id="11f72-145">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="11f72-146">Winbio \_ ANSI \_ 381 \_ POS \_ zwei \_ Daumen</span><span class="sxs-lookup"><span data-stu-id="11f72-146">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="11f72-147">Versuchen Sie nicht, den für den *Positions* Wert angegebenen Wert zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="11f72-147">Do not attempt to validate the value supplied for the *Position* value.</span></span> <span data-ttu-id="11f72-148">Der Windows-Biometrie-Dienst überprüft den angegebenen Wert vor der Übergabe an Ihre Implementierung.</span><span class="sxs-lookup"><span data-stu-id="11f72-148">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="11f72-149">Wenn der Wert " **winbio \_ SubType \_ No \_ Information** " oder " **winbio \_ SubType \_ any**" lautet, überprüfen Sie ggf. ggf.</span><span class="sxs-lookup"><span data-stu-id="11f72-149">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11f72-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11f72-150">Requirements</span></span>



| <span data-ttu-id="11f72-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11f72-151">Requirement</span></span> | <span data-ttu-id="11f72-152">Wert</span><span class="sxs-lookup"><span data-stu-id="11f72-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f72-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11f72-153">Minimum supported client</span></span><br/> | <span data-ttu-id="11f72-154">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11f72-154">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="11f72-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11f72-155">Minimum supported server</span></span><br/> | <span data-ttu-id="11f72-156">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11f72-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="11f72-157">Header</span><span class="sxs-lookup"><span data-stu-id="11f72-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="11f72-158"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11f72-158"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11f72-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11f72-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f72-160">Client Anwendungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="11f72-160">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





