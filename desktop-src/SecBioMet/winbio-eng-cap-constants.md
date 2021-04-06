---
title: WINBIO_ENG_CAP Konstanten (winbio \_ types. h)
description: Geben Sie generische Engine-Funktionen an.
ms.assetid: 31C4E8AF-6EF8-43FF-A944-D7363A26BB1A
topic_type:
- apiref
api_name:
- WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT
- WINBIO_ENG_CAP_SPOOF_DETECTION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d69db9f0e15ca0d50aa5ca134fdc74904dec85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743673"
---
# <a name="winbio_eng_cap-constants"></a><span data-ttu-id="773f9-103">Winbio \_ eng \_ Cap-Konstanten</span><span class="sxs-lookup"><span data-stu-id="773f9-103">WINBIO\_ENG\_CAP Constants</span></span>

<span data-ttu-id="773f9-104">Die folgenden Konstanten sind **winbio \_** -Funktions Werte, die verwendet werden können, um generische Funktionen der Engine-Komponente anzugeben, die mit einer bestimmten biometrischen Einheit verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="773f9-104">The following constants are **WINBIO\_CAPABILITIES** values that can be used to specify generic capabilities of the engine component that is connected to a specific biometric unit.</span></span> <span data-ttu-id="773f9-105">Diese Funktionen geben Sie in **genericenginecapabili-** Member der Struktur [**\_ \_ \_ Info**](winbio-extended-engine-info.md) -Struktur von winbio an.</span><span class="sxs-lookup"><span data-stu-id="773f9-105">You specify these capabilities in **GenericEngineCapabilities** member of the [**WINBIO\_EXTENDED\_ENGINE\_INFO**](winbio-extended-engine-info.md) structure.</span></span>



| <span data-ttu-id="773f9-106">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="773f9-106">Constant/value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="773f9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="773f9-107">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span id="WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT"></span><span id="winbio_eng_cap_iterative_improvement"></span><dl> <span data-ttu-id="773f9-108"><dt>**Winbio \_ ENG \_ Cap \_ iterative \_ Verbesserung**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="773f9-108"><dt>**WINBIO\_ENG\_CAP\_ITERATIVE\_IMPROVEMENT**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="773f9-109">Die Komponente für biometrische Module kann iterative Verbesserung durchführen.</span><span class="sxs-lookup"><span data-stu-id="773f9-109">The biometric engine component can perform iterative improvement.</span></span><br/> |
| <span id="WINBIO_ENG_CAP_SPOOF_DETECTION"></span><span id="winbio_eng_cap_spoof_detection"></span><dl> <span data-ttu-id="773f9-110"><dt>**Winbio \_ ENG \_ Cap- \_ Spoof- \_ Erkennung**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="773f9-110"><dt>**WINBIO\_ENG\_CAP\_SPOOF\_DETECTION**</dt> <dt>0x00000002</dt></span></span> </dl>                   | <span data-ttu-id="773f9-111">Die Komponente für biometrische Module kann eine spoofen-Erkennung ausführen.</span><span class="sxs-lookup"><span data-stu-id="773f9-111">The biometric engine component can perform spoof detection.</span></span><br/>       |



## <a name="requirements"></a><span data-ttu-id="773f9-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="773f9-112">Requirements</span></span>



| <span data-ttu-id="773f9-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="773f9-113">Requirement</span></span> | <span data-ttu-id="773f9-114">Wert</span><span class="sxs-lookup"><span data-stu-id="773f9-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="773f9-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="773f9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="773f9-116">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="773f9-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="773f9-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="773f9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="773f9-118">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="773f9-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="773f9-119">Header</span><span class="sxs-lookup"><span data-stu-id="773f9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="773f9-120"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="773f9-120"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





