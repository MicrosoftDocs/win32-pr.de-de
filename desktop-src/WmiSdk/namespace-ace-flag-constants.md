---
description: In der folgenden Liste sind die möglichen Werte des Felds Flags in einem WMI-Access Control Entry (ACE) aufgelistet.
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Namespace-ACE-Flag-Konstanten (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OBJECT_INHERIT_ACE
- CONTAINER_INHERIT_ACE
- NO_PROPAGATE_INHERIT_ACE
- INHERIT_ONLY_ACE
- INHERITED_ACE
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 053d4166882b6254dec313cb10fbf10588ba0071
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370771"
---
# <a name="namespace-ace-flag-constants"></a><span data-ttu-id="dd55b-103">Namespace-ACE-Flag-Konstanten</span><span class="sxs-lookup"><span data-stu-id="dd55b-103">Namespace ACE Flag Constants</span></span>

<span data-ttu-id="dd55b-104">In der folgenden Liste sind die möglichen Werte des Felds **Flags** in einem WMI-Access Control Entry (ACE) aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dd55b-104">The following list lists the possible values of the **Flags** field in a WMI Access Control Entry (ACE).</span></span>

<dl> <dt>

<span data-ttu-id="dd55b-105"><span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**Objekt \_ erben ( \_ ACE)**</span><span class="sxs-lookup"><span data-stu-id="dd55b-105"><span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**OBJECT\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd55b-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="dd55b-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="dd55b-107">Untergeordnete Objekte, die nicht Container sind, erben den ACE als effektiven ACE.</span><span class="sxs-lookup"><span data-stu-id="dd55b-107">Non-container child objects inherit the ACE as an effective ACE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dd55b-108"><span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**Container \_ erben ( \_ ACE)**</span><span class="sxs-lookup"><span data-stu-id="dd55b-108"><span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**CONTAINER\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd55b-109">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="dd55b-109">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="dd55b-110">Der ACE wirkt sich auf untergeordnete Namespaces und den aktuellen Namespace aus.</span><span class="sxs-lookup"><span data-stu-id="dd55b-110">The ACE has an effect on child namespaces as well as the current namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dd55b-111"><span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**kein \_ propagieren- \_ \_ ACE erben**</span><span class="sxs-lookup"><span data-stu-id="dd55b-111"><span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**NO\_PROPAGATE\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd55b-112">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="dd55b-112">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="dd55b-113">Der ACE gilt nur für den aktuellen Namespace und die unmittelbar untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="dd55b-113">The ACE applies only to the current namespace and immediate children .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dd55b-114"><span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**\_nur \_ ACE erben**</span><span class="sxs-lookup"><span data-stu-id="dd55b-114"><span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**INHERIT\_ONLY\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd55b-115">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="dd55b-115">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="dd55b-116">Der ACE gilt nur für untergeordnete Namespaces.</span><span class="sxs-lookup"><span data-stu-id="dd55b-116">The ACE applies only to child namespaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dd55b-117"><span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**geerbte \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="dd55b-117"><span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**INHERITED\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd55b-118">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="dd55b-118">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="dd55b-119">Dies wird nicht von Clients festgelegt, sondern an Clients gemeldet, wenn die Quelle eines ACE ein übergeordneter Namespace ist.</span><span class="sxs-lookup"><span data-stu-id="dd55b-119">This is not set by clients, but is reported to clients when the source of an ACE is a parent namespace.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd55b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd55b-120">Requirements</span></span>



| <span data-ttu-id="dd55b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd55b-121">Requirement</span></span> | <span data-ttu-id="dd55b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="dd55b-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dd55b-123">Header</span><span class="sxs-lookup"><span data-stu-id="dd55b-123">Header</span></span><br/> | <dl> <span data-ttu-id="dd55b-124"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd55b-124"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd55b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd55b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd55b-126">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="dd55b-126">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="dd55b-127">Festlegen von namepace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="dd55b-127">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="dd55b-128">Einrichten der Vererbung der Namespace Sicherheit</span><span class="sxs-lookup"><span data-stu-id="dd55b-128">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="dd55b-129">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="dd55b-129">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 




