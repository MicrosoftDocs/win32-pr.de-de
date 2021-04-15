---
title: WINBIO_PROPERTY_TYPE Konstanten (winbio. h)
description: Geben Sie die Quelle der Eigenschafts Informationen in der winbiogetproperty-Funktion an.
ms.assetid: 82C54092-032B-4F32-820E-A1D4BB81ECCE
topic_type:
- apiref
api_name:
- WINBIO_PROPERTY_TYPE_SESSION
- WINBIO_PROPERTY_TYPE_TEMPLATE
- WINBIO_PROPERTY_TYPE_UNIT
- WINBIO_PROPERTY_TYPE_ACCOUNT
api_location:
- Winbio.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4a1420af18bfa4d2ba5d0457b22cd5f77e7b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479251"
---
# <a name="winbio_property_type-constants"></a><span data-ttu-id="81b85-103">Winbio \_ - \_ Eigenschaftentyp Konstanten</span><span class="sxs-lookup"><span data-stu-id="81b85-103">WINBIO\_PROPERTY\_TYPE Constants</span></span>

<span data-ttu-id="81b85-104">Die folgenden **winbio \_ - \_ Eigenschaftentyp** Konstanten können verwendet werden, um die Quelle der Eigenschafts Informationen in der [**winbiogetproperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) -Funktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="81b85-104">The following **WINBIO\_PROPERTY\_TYPE** constants can be used to specify the source of the property information in the [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) function.</span></span>

<dl> <dt>

<span data-ttu-id="81b85-105"><span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**winbio \_ - \_ Eigenschaftentyp \_ Sitzung**</span><span class="sxs-lookup"><span data-stu-id="81b85-105"><span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**WINBIO\_PROPERTY\_TYPE\_SESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81b85-106">Die-Eigenschaft gilt für eine bestimmte biometrische Sitzung.</span><span class="sxs-lookup"><span data-stu-id="81b85-106">The property applies to a specific biometric session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81b85-107"><span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**winbio \_ - \_ Eigenschaftentyp \_ Vorlage**</span><span class="sxs-lookup"><span data-stu-id="81b85-107"><span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**WINBIO\_PROPERTY\_TYPE\_TEMPLATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81b85-108">Die-Eigenschaft gilt für eine bestimmte biometrische Vorlage.</span><span class="sxs-lookup"><span data-stu-id="81b85-108">The property applies to a specific biometric template.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81b85-109"><span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**winbio \_ - \_ Eigenschaftentyp \_ Einheit**</span><span class="sxs-lookup"><span data-stu-id="81b85-109"><span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**WINBIO\_PROPERTY\_TYPE\_UNIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81b85-110">Die-Eigenschaft gilt für eine bestimmte biometrische Einheit.</span><span class="sxs-lookup"><span data-stu-id="81b85-110">The property applies to a specific biometric unit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81b85-111"><span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**winbio \_ - \_ Eigenschaftentyp \_ Konto**</span><span class="sxs-lookup"><span data-stu-id="81b85-111"><span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**WINBIO\_PROPERTY\_TYPE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="81b85-112">Die-Eigenschaft gilt für ein bestimmtes Benutzerkonto, das über eine biometrische Registrierung verfügt.</span><span class="sxs-lookup"><span data-stu-id="81b85-112">The property applies to a specific user account that has a biometric enrollment.</span></span> <span data-ttu-id="81b85-113">Dieser Wert wird ab Windows 10 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81b85-113">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81b85-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81b85-114">Requirements</span></span>



| <span data-ttu-id="81b85-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81b85-115">Requirement</span></span> | <span data-ttu-id="81b85-116">Wert</span><span class="sxs-lookup"><span data-stu-id="81b85-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b85-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81b85-117">Minimum supported client</span></span><br/> | <span data-ttu-id="81b85-118">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81b85-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="81b85-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81b85-119">Minimum supported server</span></span><br/> | <span data-ttu-id="81b85-120">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81b85-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="81b85-121">Header</span><span class="sxs-lookup"><span data-stu-id="81b85-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="81b85-122"><dt>Winbio. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81b85-122"><dt>Winbio.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81b85-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81b85-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81b85-124">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="81b85-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="81b85-125">**Winbiogetproperty**</span><span class="sxs-lookup"><span data-stu-id="81b85-125">**WinBioGetProperty**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> </dl>

 

 





