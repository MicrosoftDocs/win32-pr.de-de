---
title: WINBIO_BIOMETRIC_SENSOR_SUBTYPE Konstanten (winbio \_ types. h)
description: Geben Sie eine Bitmaske zum Integrieren von Sensor Funktionen an.
ms.assetid: ED2A26BC-AED4-4304-9A17-A9BA126B0AFC
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_SUBTYPE_UNKNOWN
- WINBIO_FP_SENSOR_SUBTYPE_SWIPE
- WINBIO_FP_SENSOR_SUBTYPE_TOUCH
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26229634f3d404921f877bb65d83f7d75634ecbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391772"
---
# <a name="winbio_biometric_sensor_subtype-constants"></a><span data-ttu-id="0662f-103">\_ \_ \_ Subtypkonstanten für den Subtyp "winbio-biometrische</span><span class="sxs-lookup"><span data-stu-id="0662f-103">WINBIO\_BIOMETRIC\_SENSOR\_SUBTYPE Constants</span></span>

<span data-ttu-id="0662f-104">Die folgenden Konstanten können als Bitmaske für den *Funktionsparameter der* [**winbio- \_ Einheiten \_ Schema**](winbio-unit-schema.md) Struktur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0662f-104">The following constants can be used as a bitmask for the *Capabilities* parameter of the [**WINBIO\_UNIT\_SCHEMA**](winbio-unit-schema.md) structure.</span></span> <span data-ttu-id="0662f-105">Diese Informationen beziehen sich auf die Funktionen des integrierten Sensors.</span><span class="sxs-lookup"><span data-stu-id="0662f-105">These refer to the onboard sensor capabilities.</span></span>



| <span data-ttu-id="0662f-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="0662f-106">Constant</span></span>                                                                                                                                                                                                            | <span data-ttu-id="0662f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0662f-107">Description</span></span>                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="WINBIO_SENSOR_SUBTYPE_UNKNOWN"></span><span id="winbio_sensor_subtype_unknown"></span><dl> <span data-ttu-id="0662f-108"><dt>**der winbio- \_ Sensor \_ Untertyp ist \_ unbekannt.**</dt></span><span class="sxs-lookup"><span data-stu-id="0662f-108"><dt>**WINBIO\_SENSOR\_SUBTYPE\_UNKNOWN**</dt></span></span> </dl>     | <span data-ttu-id="0662f-109">Die Sensor Untertypen sind nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="0662f-109">The sensor sub types is not known.</span></span><br/>      |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_SWIPE"></span><span id="winbio_fp_sensor_subtype_swipe"></span><dl> <span data-ttu-id="0662f-110"><dt>**winbio- \_ FP- \_ \_ unter Typ \_ schwenken**</dt></span><span class="sxs-lookup"><span data-stu-id="0662f-110"><dt>**WINBIO\_FP\_SENSOR\_SUBTYPE\_SWIPE**</dt></span></span> </dl> | <span data-ttu-id="0662f-111">Der Sensor unterstützt Fingerabdruck.</span><span class="sxs-lookup"><span data-stu-id="0662f-111">The sensor supports fingerprint swipes.</span></span><br/> |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_TOUCH"></span><span id="winbio_fp_sensor_subtype_touch"></span><dl> <span data-ttu-id="0662f-112"><dt>**Fingereingabe von winbio \_ FP- \_ Sensor \_ unter Typ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0662f-112"><dt>**WINBIO\_FP\_SENSOR\_SUBTYPE\_TOUCH**</dt></span></span> </dl> | <span data-ttu-id="0662f-113">Der Sensor unterstützt Finger Berührungen.</span><span class="sxs-lookup"><span data-stu-id="0662f-113">The sensor supports finger touches.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="0662f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0662f-114">Requirements</span></span>



| <span data-ttu-id="0662f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0662f-115">Requirement</span></span> | <span data-ttu-id="0662f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0662f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0662f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0662f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0662f-118">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0662f-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="0662f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0662f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0662f-120">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0662f-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0662f-121">Header</span><span class="sxs-lookup"><span data-stu-id="0662f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0662f-122"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0662f-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0662f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0662f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0662f-124">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="0662f-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="0662f-125">**winbio- \_ Einheits \_ Schema**</span><span class="sxs-lookup"><span data-stu-id="0662f-125">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





