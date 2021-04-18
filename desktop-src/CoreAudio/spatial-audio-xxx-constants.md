---
description: Die \_ \_ Konstanten für räumliche Audio xxx definieren Werte, die sich auf räumliche Audiofunktionen beziehen.
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: SPATIAL_AUDIO_XXX Konstanten (spatialaudiometadata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2c92b970f69cf84e0744f21a41932a8851efed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360974"
---
# <a name="spatial_audio_xxx-constants"></a><span data-ttu-id="40a16-103">Räumliche \_ Audiodateien \_ xxx-Konstanten</span><span class="sxs-lookup"><span data-stu-id="40a16-103">SPATIAL\_AUDIO\_XXX Constants</span></span>

<span data-ttu-id="40a16-104">Die \_ \_ Konstanten für räumliche Audio xxx definieren Werte, die sich auf räumliche Audiofunktionen beziehen.</span><span class="sxs-lookup"><span data-stu-id="40a16-104">The SPATIAL\_AUDIO\_XXX constants define values related to spatial sound features.</span></span>



| <span data-ttu-id="40a16-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="40a16-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="40a16-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40a16-106">Description</span></span>                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <span data-ttu-id="40a16-107"><dt>**Räumlich \_ \_AudioPosition**</dt> <dt>200</dt></span><span class="sxs-lookup"><span data-stu-id="40a16-107"><dt>**SPATIAL\_AUDIO\_POSITION**</dt> <dt>200</dt></span></span> </dl>                                                   | <span data-ttu-id="40a16-108">Ein von Microsoft definierter standardmäßiger audiometadatenbefehl, der die listenerposition im Standardmodell darstellt, das von [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) verwendet wird, wobei der Listener an der Position an Koordinaten (0, 0, 0) liegt und in Meter definiert ist.</span><span class="sxs-lookup"><span data-stu-id="40a16-108">A standard Microsoft-defined spatial audio metadata command which represents the listener position in the standard model used by [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) where the listener's head is position at coordinates (0,0,0), defined in meters.</span></span><br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <span data-ttu-id="40a16-109"><dt>**Räumlich \_ \_ \_ Byte \_ Anzahl der AudioPosition**</dt> <dt>sizeof (float) \* 3</dt></span><span class="sxs-lookup"><span data-stu-id="40a16-109"><dt>**SPATIAL\_AUDIO\_POSITION\_BYTE\_COUNT**</dt> <dt>sizeof(float) \* 3</dt></span></span> </dl> | <span data-ttu-id="40a16-110">Gibt die Größe des Werts **der \_ räumlichen \_ AudioPosition** an.</span><span class="sxs-lookup"><span data-stu-id="40a16-110">Specifies the size of the **SPATIAL\_AUDIO\_POSITION** value.</span></span><br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <span data-ttu-id="40a16-111"><dt>**Räumlich \_ \_ \_ Audiostandardbefehle \_ starten**</dt> <dt>200</dt></span><span class="sxs-lookup"><span data-stu-id="40a16-111"><dt>**SPATIAL\_AUDIO\_STANDARD\_COMMANDS\_START**</dt> <dt>200</dt></span></span> </dl>    | <span data-ttu-id="40a16-112">Gibt den Anfang des Bereichs der von Microsoft reservierten räumlichen audiometadatenbefehle an.</span><span class="sxs-lookup"><span data-stu-id="40a16-112">Specifies the start of the range of Microsoft-reserved spatial audio metadata commands.</span></span> <span data-ttu-id="40a16-113">Benutzerdefinierte metadatenbefehle sind auf Befehls-IDs 0-199 beschränkt.</span><span class="sxs-lookup"><span data-stu-id="40a16-113">Custom metadata commands are restricted to command IDs 0 - 199.</span></span> <span data-ttu-id="40a16-114">Die Befehle 200-255 sind für die Verwendung durch Microsoft reserviert.</span><span class="sxs-lookup"><span data-stu-id="40a16-114">Commands 200 - 255 are reserved for Microsoft use.</span></span><br/>                                                           |



## <a name="requirements"></a><span data-ttu-id="40a16-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40a16-115">Requirements</span></span>



| <span data-ttu-id="40a16-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40a16-116">Requirement</span></span> | <span data-ttu-id="40a16-117">Wert</span><span class="sxs-lookup"><span data-stu-id="40a16-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40a16-118">Header</span><span class="sxs-lookup"><span data-stu-id="40a16-118">Header</span></span><br/> | <dl> <span data-ttu-id="40a16-119"><dt>Spatialaudiometadata. h</dt></span><span class="sxs-lookup"><span data-stu-id="40a16-119"><dt>SpatialAudioMetadata.h</dt></span></span> </dl> |



 

 




