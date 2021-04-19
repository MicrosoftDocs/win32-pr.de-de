---
title: _WAVEFORMATEX Struktur
description: Die \_WAVEFORMATEX-Struktur definiert das Format von Waveform-Audiodaten.
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- _WAVEFORMATEX Struktur von Windows-Medien Device Manager
topic_type:
- apiref
api_name:
- _WAVEFORMATEX
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d0ede83e22033aee8f18d11b6230e471e0dfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366956"
---
# <a name="_waveformatex-structure"></a><span data-ttu-id="66627-104">\_WaveFormatEx-Struktur</span><span class="sxs-lookup"><span data-stu-id="66627-104">\_WAVEFORMATEX structure</span></span>

<span data-ttu-id="66627-105">Die **\_ WaveFormatEx** -Struktur definiert das Format von Waveform-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="66627-105">The **\_WAVEFORMATEX** structure defines the format of waveform-audio data.</span></span>

## <a name="syntax"></a><span data-ttu-id="66627-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="66627-106">Syntax</span></span>


```C++
typedef struct _tWAVEFORMATEX {
  WORD  wFormatTag;
  WORD  nChannels;
  DWORD nSamplesPerSec;
  DWORD nAvgBytesPerSec;
  WORD  nBlockAlign;
  WORD  wBitsPerSample;
  WORD  cbSize;
} _WAVEFORMATEX;
```



## <a name="members"></a><span data-ttu-id="66627-107">Member</span><span class="sxs-lookup"><span data-stu-id="66627-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="66627-108">**wformattag**</span><span class="sxs-lookup"><span data-stu-id="66627-108">**wFormatTag**</span></span>
</dt> <dd>

<span data-ttu-id="66627-109">Muss auf ein Format oder auf Formate festgelegt werden, die vom Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="66627-109">Must be set to a format or formats supported by the device.</span></span> <span data-ttu-id="66627-110">Beachten Sie, dass in früheren Versionen des Windows Media-Device Manager die Verwendung von WMDM \_ Wave \_ Format all empfohlen wird \_ , um die Unterstützung für alle Formate anzugeben.</span><span class="sxs-lookup"><span data-stu-id="66627-110">Note that previous versions of the Windows Media Device Manager recommended using WMDM\_WAVE\_FORMAT\_ALL to indicate support for all formats.</span></span> <span data-ttu-id="66627-111">Dies wird jedoch nicht mehr empfohlen, da verschiedene Medienspieler dies auf unterschiedliche Weise interpretieren und nur wenige Geräte das Dateiformat wirklich wiedergeben können.</span><span class="sxs-lookup"><span data-stu-id="66627-111">However, this is no longer recommended, as different media players will interpret this in different ways, and few devices can truly play any file format.</span></span> <span data-ttu-id="66627-112">Es wird nun empfohlen, die WMDM- \_ \_ Enumerationswerte \_ gültige \_ Werte \_ für einen beliebigen Wert der Enumeration für [**\_ \_ \_ gültige \_ Werte \_ des WMDM**](wmdm-enum-prop-valid-values-form.md) -Enumerationswerts zu verwenden, oder Sie sollten einen Bereich von Formaten mit der [**WMDM- \_ \_ Werte \_ Bereichs**](wmdm-prop-values-range.md) Struktur angeben.</span><span class="sxs-lookup"><span data-stu-id="66627-112">It is now recommended that you use the WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY value of the [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration, or better yet specify a range of formats with the [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="66627-113">**nchannels**</span><span class="sxs-lookup"><span data-stu-id="66627-113">**nChannels**</span></span>
</dt> <dd>

<span data-ttu-id="66627-114">Anzahl von Kanälen in den Waveform-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="66627-114">Number of channels in the waveform-audio data.</span></span> <span data-ttu-id="66627-115">Die Monale Daten verwenden einen Kanal, und Stereodaten verwenden zwei Kanäle.</span><span class="sxs-lookup"><span data-stu-id="66627-115">Monaural data uses one channel, and stereo data uses two channels.</span></span>

</dd> <dt>

<span data-ttu-id="66627-116">**nsamplespersec**</span><span class="sxs-lookup"><span data-stu-id="66627-116">**nSamplesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="66627-117">Die Stichprobenrate in Samplings pro Sekunde (Hertz), bei der jeder Kanal wiedergegeben oder aufgezeichnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="66627-117">Sample rate, in samples per second (Hertz), at which each channel must be played or recorded.</span></span> <span data-ttu-id="66627-118">Allgemeine Werte für **nsamplespersec** sind 8,0 Kilohertz (kHz), 11,025 kHz, 22,05 kHz und 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="66627-118">Common values for **nSamplesPerSec** are 8.0 kilohertz (kHz), 11.025 kHz, 22.05 kHz, and 44.1 kHz.</span></span>

</dd> <dt>

<span data-ttu-id="66627-119">**navgbytespersec**</span><span class="sxs-lookup"><span data-stu-id="66627-119">**nAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="66627-120">Erforderliche durchschnittliche Datenübertragungsrate für das Formattag (in Bytes pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="66627-120">Required average data-transfer rate for the format tag, in bytes per second.</span></span> <span data-ttu-id="66627-121">Wiedergabe-und Aufzeichnungssoftware kann die Puffergrößen mit dem **navgbytespersec** -Member schätzen.</span><span class="sxs-lookup"><span data-stu-id="66627-121">Playback and recording software can estimate buffer sizes by using the **nAvgBytesPerSec** member.</span></span>

</dd> <dt>

<span data-ttu-id="66627-122">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="66627-122">**nBlockAlign**</span></span>
</dt> <dd>

<span data-ttu-id="66627-123">Block Ausrichtung (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="66627-123">Block alignment, in bytes.</span></span> <span data-ttu-id="66627-124">Die Block Ausrichtung ist die minimale unteilbare Einheit von Daten für den Formattyp " **wformattag** ".</span><span class="sxs-lookup"><span data-stu-id="66627-124">The block alignment is the minimum atomic unit of data for the **wFormatTag** format type.</span></span> <span data-ttu-id="66627-125">Wiedergabe-und Aufzeichnungssoftware muss ein Vielfaches von **nBlockAlign** -Bytes an Daten gleichzeitig verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="66627-125">Playback and recording software must process a multiple of **nBlockAlign** bytes of data at a time.</span></span> <span data-ttu-id="66627-126">Von einem Gerät geschriebene und gelesene Daten müssen immer am Anfang eines-Blocks gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="66627-126">Data written and read from a device must always start at the beginning of a block.</span></span> <span data-ttu-id="66627-127">Beispielsweise ist es nicht möglich, in der Mitte eines Beispiels (d. h. an einer Grenze, die nicht Block bündig ist) die Wiedergabe von PCM-Daten zu starten.</span><span class="sxs-lookup"><span data-stu-id="66627-127">For example, it is not possible to correctly start playing PCM data in the middle of a sample (that is, on a boundary that is not block aligned).</span></span>

</dd> <dt>

<span data-ttu-id="66627-128">**wbitspersample**</span><span class="sxs-lookup"><span data-stu-id="66627-128">**wBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="66627-129">Bits pro Sample für den Formattyp " **wformattag** ".</span><span class="sxs-lookup"><span data-stu-id="66627-129">Bits per sample for the **wFormatTag** format type.</span></span>

</dd> <dt>

<span data-ttu-id="66627-130">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="66627-130">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="66627-131">Dieser Member wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="66627-131">This member is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66627-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66627-132">Requirements</span></span>



| <span data-ttu-id="66627-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66627-133">Requirement</span></span> | <span data-ttu-id="66627-134">Wert</span><span class="sxs-lookup"><span data-stu-id="66627-134">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="66627-135">Header</span><span class="sxs-lookup"><span data-stu-id="66627-135">Header</span></span><br/> | <dl> <span data-ttu-id="66627-136"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66627-136"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66627-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66627-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66627-138">**Imdspdevice:: getformatsupport**</span><span class="sxs-lookup"><span data-stu-id="66627-138">**IMDSPDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[<span data-ttu-id="66627-139">**Imdspstorage:: anatestorage**</span><span class="sxs-lookup"><span data-stu-id="66627-139">**IMDSPStorage::CreateStorage**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[<span data-ttu-id="66627-140">**Imdspstorage:: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="66627-140">**IMDSPStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[<span data-ttu-id="66627-141">**Iwmdmdevice:: getformatsupport**</span><span class="sxs-lookup"><span data-stu-id="66627-141">**IWMDMDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[<span data-ttu-id="66627-142">**Iwmdmoperation:: getobjectattributes**</span><span class="sxs-lookup"><span data-stu-id="66627-142">**IWMDMOperation::GetObjectAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[<span data-ttu-id="66627-143">**Iwmdmoperation:: "abtobjectattributes"**</span><span class="sxs-lookup"><span data-stu-id="66627-143">**IWMDMOperation::SetObjectAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[<span data-ttu-id="66627-144">**Iwmdmstorage:: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="66627-144">**IWMDMStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[<span data-ttu-id="66627-145">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="66627-145">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





