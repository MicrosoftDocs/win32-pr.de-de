---
title: WINBIO_POOL Konstanten (winbio \_ types. h)
description: Geben Sie den Typ des biometrischen Einheiten Pools an, der in der Sitzung verwendet werden soll.
ms.assetid: e6e49b95-981a-477d-9889-ea132db5b387
topic_type:
- apiref
api_name:
- WINBIO_POOL_UNKNOWN
- WINBIO_POOL_SYSTEM
- WINBIO_POOL_PRIVATE
- WINBIO_POOL_UNASSIGNED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7af1ec8d5692a390bb91ecb63736bd94efb2e85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519025"
---
# <a name="winbio_pool-constants"></a><span data-ttu-id="caa4b-103">Winbio- \_ Pool Konstanten</span><span class="sxs-lookup"><span data-stu-id="caa4b-103">WINBIO\_POOL Constants</span></span>

<span data-ttu-id="caa4b-104">Die folgenden Konstanten können in der [**winbioopensession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) -Funktion verwendet werden, um den Typ des biometrischen Einheiten Pools anzugeben, der in der Sitzung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="caa4b-104">The following constants can be used in the [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) function to specify the type of biometric unit pool to be used in the session.</span></span>



| <span data-ttu-id="caa4b-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="caa4b-105">Constant</span></span>                                                                                                                                                                                  | <span data-ttu-id="caa4b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="caa4b-106">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <span data-ttu-id="caa4b-107"><dt>**winbio- \_ Pool \_ unbekannt**</dt></span><span class="sxs-lookup"><span data-stu-id="caa4b-107"><dt>**WINBIO\_POOL\_UNKNOWN**</dt></span></span> </dl>          | <span data-ttu-id="caa4b-108">Der Pooltyp ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="caa4b-108">The pool type is unknown.</span></span><br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <span data-ttu-id="caa4b-109"><dt>**winbio- \_ Pool \_ System**</dt></span><span class="sxs-lookup"><span data-stu-id="caa4b-109"><dt>**WINBIO\_POOL\_SYSTEM**</dt></span></span> </dl>             | <span data-ttu-id="caa4b-110">Gibt eine freigegebene Auflistung biometrischer Einheiten an, die vom Dienstanbieter verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="caa4b-110">Specifies a shared collection of biometric units managed by the service provider.</span></span><br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <span data-ttu-id="caa4b-111"><dt>**privater winbio- \_ Pool \_**</dt></span><span class="sxs-lookup"><span data-stu-id="caa4b-111"><dt>**WINBIO\_POOL\_PRIVATE**</dt></span></span> </dl>          | <span data-ttu-id="caa4b-112">Gibt eine Sammlung von biometrischen Einheiten an, die vom Aufrufer verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="caa4b-112">Specifies a collection of biometric units that are managed by the caller.</span></span><br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <span data-ttu-id="caa4b-113"><dt>**winbio- \_ Pool \_ nicht zugewiesen**</dt></span><span class="sxs-lookup"><span data-stu-id="caa4b-113"><dt>**WINBIO\_POOL\_UNASSIGNED**</dt></span></span> </dl> | <span data-ttu-id="caa4b-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="caa4b-114">Reserved.</span></span><br/>                                                                         |



## <a name="requirements"></a><span data-ttu-id="caa4b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="caa4b-115">Requirements</span></span>



| <span data-ttu-id="caa4b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="caa4b-116">Requirement</span></span> | <span data-ttu-id="caa4b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="caa4b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caa4b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="caa4b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="caa4b-119">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="caa4b-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="caa4b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="caa4b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="caa4b-121">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="caa4b-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="caa4b-122">Header</span><span class="sxs-lookup"><span data-stu-id="caa4b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="caa4b-123"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="caa4b-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caa4b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="caa4b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caa4b-125">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="caa4b-125">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





