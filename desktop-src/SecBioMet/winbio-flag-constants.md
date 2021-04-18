---
title: WINBIO_FLAG Konstanten (winbio \_ types. h)
description: Geben Sie die Konfiguration für biometrische Einheiten und die Zugriffs Merkmale für die neue Sitzung an.
ms.assetid: 82b57023-6c27-433d-bf13-f136f501fc60
topic_type:
- apiref
api_name:
- WINBIO_FLAG_DEFAULT
- WINBIO_FLAG_BASIC
- WINBIO_FLAG_ADVANCED
- WINBIO_FLAG_RAW
- WINBIO_FLAG_MAINTENANCE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed632b5f15cc3d6a7ac6b0c6c70a2b3431b73db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391640"
---
# <a name="winbio_flag-constants"></a><span data-ttu-id="7c19c-103">Winbio- \_ Flag-Konstanten</span><span class="sxs-lookup"><span data-stu-id="7c19c-103">WINBIO\_FLAG Constants</span></span>

<span data-ttu-id="7c19c-104">Die folgenden Konstanten können in der [**winbioopensession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) -Funktion verwendet werden, um die Konfiguration und die Zugriffs Merkmale für biometrische Einheiten für die neue Sitzung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7c19c-104">The following constants can be used in the [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) function to specify biometric unit configuration and access characteristics for the new session.</span></span>



| <span data-ttu-id="7c19c-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="7c19c-105">Constant</span></span>                                                                                                                                                                                     | <span data-ttu-id="7c19c-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c19c-106">Description</span></span>                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <span data-ttu-id="7c19c-107"><dt>**winbio- \_ Flag ( \_ Standard)**</dt></span><span class="sxs-lookup"><span data-stu-id="7c19c-107"><dt>**WINBIO\_FLAG\_DEFAULT**</dt></span></span> </dl>             | <span data-ttu-id="7c19c-108">Sensorkonfigurationsflag.</span><span class="sxs-lookup"><span data-stu-id="7c19c-108">Sensor configuration flag.</span></span> <span data-ttu-id="7c19c-109">Die biometrischen Einheiten arbeiten in der während der Installation angegebenen Weise.</span><span class="sxs-lookup"><span data-stu-id="7c19c-109">The biometric units operate in the manner specified during installation.</span></span><br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <span data-ttu-id="7c19c-110"><dt>**winbio- \_ Flag \_ Basic**</dt></span><span class="sxs-lookup"><span data-stu-id="7c19c-110"><dt>**WINBIO\_FLAG\_BASIC**</dt></span></span> </dl>                   | <span data-ttu-id="7c19c-111">Sensorkonfigurationsflag.</span><span class="sxs-lookup"><span data-stu-id="7c19c-111">Sensor configuration flag.</span></span> <span data-ttu-id="7c19c-112">Die biometrischen Einheiten werden nur als einfache Erfassungsgeräte betrieben.</span><span class="sxs-lookup"><span data-stu-id="7c19c-112">The biometric units operate only as basic capture devices.</span></span><br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <span data-ttu-id="7c19c-113"><dt>**winbio- \_ Flag \_ erweitert**</dt></span><span class="sxs-lookup"><span data-stu-id="7c19c-113"><dt>**WINBIO\_FLAG\_ADVANCED**</dt></span></span> </dl>          | <span data-ttu-id="7c19c-114">Sensorkonfigurationsflag.</span><span class="sxs-lookup"><span data-stu-id="7c19c-114">Sensor configuration flag.</span></span> <span data-ttu-id="7c19c-115">Die biometrischen Einheiten verwenden interne Verarbeitungs-und Speicherfunktionen.</span><span class="sxs-lookup"><span data-stu-id="7c19c-115">The biometric units use internal processing and storage capabilities.</span></span><br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <span data-ttu-id="7c19c-116"><dt>**winbio- \_ Flag \_ RAW**</dt></span><span class="sxs-lookup"><span data-stu-id="7c19c-116"><dt>**WINBIO\_FLAG\_RAW**</dt></span></span> </dl>                         | <span data-ttu-id="7c19c-117">Gewünschtes Zugriffsflag.</span><span class="sxs-lookup"><span data-stu-id="7c19c-117">Desired access flag.</span></span> <span data-ttu-id="7c19c-118">Die Client Anwendung erfasst biometrische Rohdaten mithilfe von [**winbiocapturesample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span><span class="sxs-lookup"><span data-stu-id="7c19c-118">The client application captures raw biometric data using [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span></span><br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <span data-ttu-id="7c19c-119"><dt>**winbio- \_ Flag- \_ Wartung**</dt></span><span class="sxs-lookup"><span data-stu-id="7c19c-119"><dt>**WINBIO\_FLAG\_MAINTENANCE**</dt></span></span> </dl> | <span data-ttu-id="7c19c-120">Gewünschtes Zugriffsflag.</span><span class="sxs-lookup"><span data-stu-id="7c19c-120">Desired access flag.</span></span> <span data-ttu-id="7c19c-121">Der Client führt vom Hersteller definierte Steuerungs Vorgänge für eine biometrische Einheit durch Aufrufen von [**winbiocontrolunitprivilegierte**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged)durch.</span><span class="sxs-lookup"><span data-stu-id="7c19c-121">The client performs vendor-defined control operations on a biometric unit by calling [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7c19c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c19c-122">Requirements</span></span>



| <span data-ttu-id="7c19c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c19c-123">Requirement</span></span> | <span data-ttu-id="7c19c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="7c19c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c19c-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c19c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7c19c-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c19c-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="7c19c-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c19c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7c19c-128">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c19c-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7c19c-129">Header</span><span class="sxs-lookup"><span data-stu-id="7c19c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c19c-130"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c19c-130"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c19c-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c19c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c19c-132">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="7c19c-132">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





