---
description: Ein-Wert, der die Größe des Datentyps für räumliche audiometadaten angibt, der vom Decoder ausgegeben wird.
ms.assetid: C133693D-A8D5-4520-B561-57BF11074257
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_LENGTH-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2cd0b3cab788dbc724ab896d2cbfeb0d42f633f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216271"
---
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a><span data-ttu-id="f9d01-103">MF \_ \_ \_ - \_ Objekt \_ metadatenlängen-Attribut für räumliche Audioobjekte \_</span><span class="sxs-lookup"><span data-stu-id="f9d01-103">MF\_MT\_SPATIAL\_AUDIO\_OBJECT\_METADATA\_LENGTH attribute</span></span>

<span data-ttu-id="f9d01-104">Ein-Wert, der die Größe des Datentyps für räumliche audiometadaten angibt, der vom Decoder ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f9d01-104">A value specifying the size, in bytes, of the spatial audio metadata object type that the decoder will output.</span></span>

## <a name="data-type"></a><span data-ttu-id="f9d01-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f9d01-105">Data type</span></span>

<span data-ttu-id="f9d01-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f9d01-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f9d01-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9d01-107">Remarks</span></span>

<span data-ttu-id="f9d01-108">Das metadatenblob mit dem angegebenen Format wird mithilfe der [**ispatialaudiometadatawriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) -Schnittstelle geschrieben und mithilfe der [**ispatialaudiometadatareader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) -Schnittstelle gelesen.</span><span class="sxs-lookup"><span data-stu-id="f9d01-108">The metadata blob with the specified format is written using the [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) interface and read using the [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) interface.</span></span> <span data-ttu-id="f9d01-109">Das metadatenblob ist für die Media Foundation Pipeline und die Komponenten nicht transparent.</span><span class="sxs-lookup"><span data-stu-id="f9d01-109">The metadata blob is opaque to the Media Foundation pipeline and components.</span></span> <span data-ttu-id="f9d01-110">Das-Attribut wird auf den Typ des räumlichen audiomediums angewendet.</span><span class="sxs-lookup"><span data-stu-id="f9d01-110">The attribute is applied to the spatial audio media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9d01-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9d01-111">Requirements</span></span>



| <span data-ttu-id="f9d01-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9d01-112">Requirement</span></span> | <span data-ttu-id="f9d01-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f9d01-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9d01-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9d01-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f9d01-115">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9d01-115">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f9d01-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9d01-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f9d01-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f9d01-117">None supported</span></span><br/>                                                          |
| <span data-ttu-id="f9d01-118">Header</span><span class="sxs-lookup"><span data-stu-id="f9d01-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9d01-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9d01-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
