---
title: WINBIO_BDB_ANSI_381_HEADER Struktur (winbio \_ types. h)
description: Gibt Informationen zu einer Reihe von Fingerabdruck-oder Palmen Beispielen an.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- WINBIO_BDB_ANSI_381_HEADER Struktur Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da04643bbdff273a2594394011ba46c16bfa29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345293"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a><span data-ttu-id="1946f-104">Winbio \_ BDB- \_ ANSI \_ 381- \_ Header Struktur</span><span class="sxs-lookup"><span data-stu-id="1946f-104">WINBIO\_BDB\_ANSI\_381\_HEADER structure</span></span>

<span data-ttu-id="1946f-105">Die **Header Struktur von winbio \_ BDB \_ ANSI \_ 381 \_** gibt Informationen zu einer Reihe von Fingerabdruck-oder Palmen Beispielen an.</span><span class="sxs-lookup"><span data-stu-id="1946f-105">The **WINBIO\_BDB\_ANSI\_381\_HEADER** structure specifies information about a series of fingerprint or palm samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="1946f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1946f-106">Syntax</span></span>


```C++
typedef struct _WINBIO_BDB_ANSI_381_HEADER {
  ULONG64                  RecordLength;
  ULONG                    FormatIdentifier;
  ULONG                    VersionNumber;
  WINBIO_REGISTERED_FORMAT ProductId;
  USHORT                   CaptureDeviceId;
  USHORT                   ImageAcquisitionLevel;
  USHORT                   HorizontalScanResolution;
  USHORT                   VerticalScanResolution;
  USHORT                   HorizontalImageResolution;
  USHORT                   VerticalImageResolution;
  UCHAR                    ElementCount;
  UCHAR                    ScaleUnits;
  UCHAR                    PixelDepth;
  UCHAR                    ImageCompressionAlg;
  USHORT                   Reserved;
} WINBIO_BDB_ANSI_381_HEADER;
```



## <a name="members"></a><span data-ttu-id="1946f-107">Member</span><span class="sxs-lookup"><span data-stu-id="1946f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1946f-108">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="1946f-108">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="1946f-109">Die Größe dieser Struktur in Bytes zuzüglich der Größe aller [**winbio \_ BDB- \_ ANSI \_ 381- \_ Daten Satz**](winbio-bdb-ansi-381-record.md) Strukturen für den Fingerabdruck oder die von einem Endbenutzer erfassten Palmen Beispiele.</span><span class="sxs-lookup"><span data-stu-id="1946f-109">The size, in bytes, of this structure plus the size of all [**WINBIO\_BDB\_ANSI\_381\_RECORD**](winbio-bdb-ansi-381-record.md) structures for the fingerprint or palm samples captured from an end user.</span></span> <span data-ttu-id="1946f-110">Nur die unteren sechs Bytes sind gültig.</span><span class="sxs-lookup"><span data-stu-id="1946f-110">Only the low six bytes are valid.</span></span>

</dd> <dt>

<span data-ttu-id="1946f-111">**Formatiertifier**</span><span class="sxs-lookup"><span data-stu-id="1946f-111">**FormatIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="1946f-112">Gibt das Format an.</span><span class="sxs-lookup"><span data-stu-id="1946f-112">Specifies the format.</span></span> <span data-ttu-id="1946f-113">Derzeit muss dies 0x46495200 sein.</span><span class="sxs-lookup"><span data-stu-id="1946f-113">Currently, this must be 0x46495200.</span></span>

</dd> <dt>

<span data-ttu-id="1946f-114">**VersionNumber**</span><span class="sxs-lookup"><span data-stu-id="1946f-114">**VersionNumber**</span></span>
</dt> <dd>

<span data-ttu-id="1946f-115">Gibt die Versionsnummer an.</span><span class="sxs-lookup"><span data-stu-id="1946f-115">Specifies the version number.</span></span> <span data-ttu-id="1946f-116">Derzeit muss dies 0x30313000 sein, das intern 0.1.0.0 entspricht.</span><span class="sxs-lookup"><span data-stu-id="1946f-116">Currently this must be 0x30313000 which corresponds internally to 0.1.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="1946f-117">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="1946f-117">**ProductId**</span></span>
</dt> <dd>

<span data-ttu-id="1946f-118">Eine [**winbio- \_ registrierte \_ Format**](winbio-registered-format.md) Struktur, die das registrierte Datenformat als Besitzer-/typpaar enthält.</span><span class="sxs-lookup"><span data-stu-id="1946f-118">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that contains the registered data format as an owner/type pair.</span></span>

</dd> <dt>

<span data-ttu-id="1946f-119">**Capturede viceid**</span><span class="sxs-lookup"><span data-stu-id="1946f-119">**CaptureDeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="1946f-120">Enthält die Einheiten-ID des Geräts, das zum Erfassen des Beispiels verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1946f-120">Contains the unit ID of the device used to capture the sample.</span></span>

</dd> <dt>

<span data-ttu-id="1946f-121">**Imageacquisitionlevel**</span><span class="sxs-lookup"><span data-stu-id="1946f-121">**ImageAcquisitionLevel**</span></span>
</dt> <dd>

<span data-ttu-id="1946f-122">Gibt die Auflösungsebene an, bei der das Beispiel aufgezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1946f-122">Specifies the resolution level at which the sample is captured.</span></span>

</dd> <dt>

<span data-ttu-id="1946f-123">**Horizontalscanresolution**</span><span class="sxs-lookup"><span data-stu-id="1946f-123">**HorizontalScanResolution**</span></span>
</dt> <dd>

<span data-ttu-id="1946f-124">Gibt die horizontale Auflösung der Überprüfung an.</span><span class="sxs-lookup"><span data-stu-id="1946f-124">Specifies the horizontal resolution of the scan.</span></span>

</dd> <dt>

<span data-ttu-id="1946f-125">**Verticalscanresolution**</span><span class="sxs-lookup"><span data-stu-id="1946f-125">**VerticalScanResolution**</span></span>
</dt> <dd>

<span data-ttu-id="1946f-126">Gibt die vertikale Auflösung der Überprüfung an.</span><span class="sxs-lookup"><span data-stu-id="1946f-126">Specifies the vertical resolution of the scan.</span></span>

</dd> <dt>

<span data-ttu-id="1946f-127">**Horizontalimageresolution**</span><span class="sxs-lookup"><span data-stu-id="1946f-127">**HorizontalImageResolution**</span></span>
</dt> <dd>

<span data-ttu-id="1946f-128">Gibt die horizontale Auflösung des aufgezeichneten Finger Abbilds oder des Palm Bilds an.</span><span class="sxs-lookup"><span data-stu-id="1946f-128">Specifies the horizontal resolution of the captured fingerprint or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="1946f-129">**Verticalimageresolution**</span><span class="sxs-lookup"><span data-stu-id="1946f-129">**VerticalImageResolution**</span></span>
</dt> <dd>

<span data-ttu-id="1946f-130">Gibt die vertikale Auflösung des aufgezeichneten Finger Abbilds oder des Palm Bilds an.</span><span class="sxs-lookup"><span data-stu-id="1946f-130">Specifies the vertical resolution of the captured fingerprint or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="1946f-131">**Element count**</span><span class="sxs-lookup"><span data-stu-id="1946f-131">**ElementCount**</span></span>
</dt> <dd>

<span data-ttu-id="1946f-132">Anzahl der Finger-oder Palmen Datensätze in dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="1946f-132">Number of finger or palm records in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="1946f-133">**ScaleUnits**</span><span class="sxs-lookup"><span data-stu-id="1946f-133">**ScaleUnits**</span></span>
</dt> <dd>

<span data-ttu-id="1946f-134">Enthält die Maßeinheit 1 für Zoll und 2 für Zentimeter.</span><span class="sxs-lookup"><span data-stu-id="1946f-134">Contains the unit of measure, 1 for inches and 2 for centimeters.</span></span>

</dd> <dt>

<span data-ttu-id="1946f-135">**Pixeltiefe**</span><span class="sxs-lookup"><span data-stu-id="1946f-135">**PixelDepth**</span></span>
</dt> <dd>

<span data-ttu-id="1946f-136">Gibt die Anzahl der Bits in einem Pixel an.</span><span class="sxs-lookup"><span data-stu-id="1946f-136">Specifies the number of bits in a pixel.</span></span> <span data-ttu-id="1946f-137">Der Wert kann zwischen 1 und 16 Bits pro Pixel liegen.</span><span class="sxs-lookup"><span data-stu-id="1946f-137">This can be 1 to 16 bits per pixel for color.</span></span>

</dd> <dt>

<span data-ttu-id="1946f-138">**Imagecompressionalg**</span><span class="sxs-lookup"><span data-stu-id="1946f-138">**ImageCompressionAlg**</span></span>
</dt> <dd>

<span data-ttu-id="1946f-139">Gibt den Algorithmus an, der zum Komprimieren des Fingers oder des Palmen Bilds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1946f-139">Specifies the algorithm used to compress the finger or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="1946f-140">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="1946f-140">**Reserved**</span></span>
<span data-ttu-id="1946f-141"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1946f-141"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1946f-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1946f-142">Requirements</span></span>



| <span data-ttu-id="1946f-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1946f-143">Requirement</span></span> | <span data-ttu-id="1946f-144">Wert</span><span class="sxs-lookup"><span data-stu-id="1946f-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1946f-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1946f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1946f-146">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1946f-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="1946f-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1946f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1946f-148">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1946f-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1946f-149">Header</span><span class="sxs-lookup"><span data-stu-id="1946f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="1946f-150"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1946f-150"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1946f-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1946f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1946f-152">Client Anwendungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="1946f-152">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





