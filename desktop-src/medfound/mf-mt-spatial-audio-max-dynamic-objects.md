---
description: Gibt die maximale Anzahl dynamischer Audioobjekte an, die vom audioendpunkt simuliert werden können.
ms.assetid: 6B6D73C1-C2E6-4C23-BBAD-7B51E8441C71
title: MF_MT_SPATIAL_AUDIO_MAX_DYNAMIC_OBJECTS-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358045079fb9cf52ad1fd0c8969f54723c7f02d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349884"
---
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a><span data-ttu-id="0c401-103">Das \_ MF \_ MT \_ - \_ Attribut für räumliche \_ \_ Objekte mit räumlichen Daten</span><span class="sxs-lookup"><span data-stu-id="0c401-103">MF\_MT\_SPATIAL\_AUDIO\_MAX\_DYNAMIC\_OBJECTS attribute</span></span>

<span data-ttu-id="0c401-104">Gibt die maximale Anzahl dynamischer Audioobjekte an, die vom audioendpunkt simuliert werden können.</span><span class="sxs-lookup"><span data-stu-id="0c401-104">Specifies the maximum number of dynamic audio objects that can be rendered by the audio endpoint simulataneously.</span></span>

## <a name="data-type"></a><span data-ttu-id="0c401-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0c401-105">Data type</span></span>

<span data-ttu-id="0c401-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0c401-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0c401-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c401-107">Remarks</span></span>

<span data-ttu-id="0c401-108">Ein [**imsspatialaudiosample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) -Wert kann weniger Stichproben enthalten als die Zahl, die von diesem Attribut angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0c401-108">An [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) may contain fewer samples than the number specified by this attribute.</span></span> <span data-ttu-id="0c401-109">Wenn ein Beispiel mehr Audioobjekte enthält, als durch dieses Attribut angegeben sind, ist das Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="0c401-109">If a sample contains more audio objects than specified by this attribute, the behavior is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c401-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c401-110">Requirements</span></span>



| <span data-ttu-id="0c401-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c401-111">Requirement</span></span> | <span data-ttu-id="0c401-112">Wert</span><span class="sxs-lookup"><span data-stu-id="0c401-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0c401-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c401-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0c401-114">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c401-114">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0c401-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c401-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0c401-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0c401-116">None supported</span></span><br/>                                                          |
| <span data-ttu-id="0c401-117">Header</span><span class="sxs-lookup"><span data-stu-id="0c401-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c401-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c401-118"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




