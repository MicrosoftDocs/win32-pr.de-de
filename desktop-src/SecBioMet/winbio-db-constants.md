---
title: WINBIO_DB Konstanten (winbio \_ types. h)
description: Geben Sie die Datenbank an, die für einen System Pool verwendet werden soll.
ms.assetid: 2cffa455-5834-4a35-b8d8-f9d1feddcaa1
topic_type:
- apiref
api_name:
- WINBIO_DB_DEFAULT
- WINBIO_DB_BOOTSTRAP
- WINBIO_DB_ONCHIP
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20503e1dc3cd7b5e47651889dd9c67777614593c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104367"
---
# <a name="winbio_db-constants"></a><span data-ttu-id="370fa-103">Winbio \_ DB-Konstanten</span><span class="sxs-lookup"><span data-stu-id="370fa-103">WINBIO\_DB Constants</span></span>

<span data-ttu-id="370fa-104">Die folgenden Konstanten können beim Aufrufen von [**winbioopensession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) verwendet werden, um die Datenbank anzugeben, die für einen System Pool verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="370fa-104">The following constants can be used when calling [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) to specify the database to be used for a system pool.</span></span>



| <span data-ttu-id="370fa-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="370fa-105">Constant</span></span>                                                                                                                                                                         | <span data-ttu-id="370fa-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="370fa-106">Description</span></span>                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <span data-ttu-id="370fa-107"><dt>**winbio \_ DB- \_ Standard**</dt></span><span class="sxs-lookup"><span data-stu-id="370fa-107"><dt>**WINBIO\_DB\_DEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="370fa-108">Jede biometrische Einheit im Sensor Pool verwendet die Standarddatenbank, die in der Standardkonfiguration für biometrische Einheiten angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="370fa-108">Each biometric unit in the sensor pool uses the default database specified in the default biometric unit configuration.</span></span><br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <span data-ttu-id="370fa-109"><dt>**winbio- \_ DB- \_ Bootstrap**</dt></span><span class="sxs-lookup"><span data-stu-id="370fa-109"><dt>**WINBIO\_DB\_BOOTSTRAP**</dt></span></span> </dl> | <span data-ttu-id="370fa-110">Kann für Szenarien vor dem Starten von Windows verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="370fa-110">Can be used for scenarios prior to starting Windows.</span></span> <span data-ttu-id="370fa-111">In der Regel ist die Datenbank Teil des Sensorchips oder Bestandteil des BIOS und kann nur für die Vorlagen Registrierung und-Löschung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="370fa-111">Typically, the database is part of the sensor chip or is part of the BIOS and can only be used for template enrollment and deletion.</span></span><br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <span data-ttu-id="370fa-112"><dt>**winbio- \_ DB- \_ Onchip**</dt></span><span class="sxs-lookup"><span data-stu-id="370fa-112"><dt>**WINBIO\_DB\_ONCHIP**</dt></span></span> </dl>          | <span data-ttu-id="370fa-113">Die Datenbank befindet sich auf dem Sensorchip.</span><span class="sxs-lookup"><span data-stu-id="370fa-113">The database resides on the sensor chip.</span></span><br/>                                                                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="370fa-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="370fa-114">Requirements</span></span>



| <span data-ttu-id="370fa-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="370fa-115">Requirement</span></span> | <span data-ttu-id="370fa-116">Wert</span><span class="sxs-lookup"><span data-stu-id="370fa-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="370fa-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="370fa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="370fa-118">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="370fa-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="370fa-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="370fa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="370fa-120">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="370fa-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="370fa-121">Header</span><span class="sxs-lookup"><span data-stu-id="370fa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="370fa-122"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="370fa-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="370fa-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="370fa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="370fa-124">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="370fa-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





