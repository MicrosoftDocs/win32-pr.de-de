---
description: Eine vom Decoder definierte GUID, die das räumliche audiometadatenformat identifiziert, wobei Downstreamkomponenten des metadatenobjekttyps benachrichtigt werden, die der Decoder ausgibt.
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed16188a24b4c61facf1e325867d093b9b5cc869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216272"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a><span data-ttu-id="34f3f-103">Das \_ MF \_ MT \_ - \_ Attribut für räumliche audioobjektmetadatenformat \_ \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="34f3f-103">MF\_MT\_SPATIAL\_AUDIO\_OBJECT\_METADATA\_FORMAT\_ID attribute</span></span>

<span data-ttu-id="34f3f-104">Eine vom Decoder definierte GUID, die das räumliche audiometadatenformat identifiziert, wobei Downstreamkomponenten des metadatenobjekttyps benachrichtigt werden, die der Decoder ausgibt.</span><span class="sxs-lookup"><span data-stu-id="34f3f-104">A decoder-defined GUID that identifies the spatial audio metadata format, notifying downstream components of the metadata object type that the decoder will output.</span></span>

## <a name="data-type"></a><span data-ttu-id="34f3f-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="34f3f-105">Data type</span></span>

<span data-ttu-id="34f3f-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="34f3f-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="34f3f-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34f3f-107">Remarks</span></span>

<span data-ttu-id="34f3f-108">Das metadatenblob mit dem angegebenen Format wird mithilfe der [**ispatialaudiometadatawriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) -Schnittstelle geschrieben und mithilfe der [**ispatialaudiometadatareader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) -Schnittstelle gelesen.</span><span class="sxs-lookup"><span data-stu-id="34f3f-108">The metadata blob with the specified format is written using the [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) interface and read using the [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) interface.</span></span> <span data-ttu-id="34f3f-109">Das metadatenblob ist für die Media Foundation Pipeline und die Komponenten nicht transparent.</span><span class="sxs-lookup"><span data-stu-id="34f3f-109">The metadata blob is opaque to the Media Foundation pipeline and components.</span></span> <span data-ttu-id="34f3f-110">Das-Attribut wird auf den Typ des räumlichen audiomediums angewendet.</span><span class="sxs-lookup"><span data-stu-id="34f3f-110">The attribute is applied to the spatial audio media type.</span></span> <span data-ttu-id="34f3f-111">Wenn eine Downstreamkomponente das durch die GUID angegebene Metadatenformat nicht unterstützt, sollte die Komponente den Eingabe Medientyp ablehnen.</span><span class="sxs-lookup"><span data-stu-id="34f3f-111">If a downstream component does not support the metadata format specified by the GUID, the component should reject the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="34f3f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34f3f-112">Requirements</span></span>



| <span data-ttu-id="34f3f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34f3f-113">Requirement</span></span> | <span data-ttu-id="34f3f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="34f3f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34f3f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34f3f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="34f3f-116">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34f3f-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="34f3f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34f3f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="34f3f-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="34f3f-118">None supported</span></span><br/>                                                          |
| <span data-ttu-id="34f3f-119">Header</span><span class="sxs-lookup"><span data-stu-id="34f3f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="34f3f-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="34f3f-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
