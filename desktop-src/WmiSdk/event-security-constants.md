---
description: Im folgenden werden die WMI-Sicherheits Konstanten angezeigt, die für-Ereignisse verwendet werden. Sie werden verwendet, um Zugriffs Steuerungs Einträge (Access Control Entries, ACEs) in Sicherheits Beschreibungen festzulegen, die für Ereignisse oder senken verwendet werden.
ms.assetid: 18318262-d948-4329-8d48-23664798fc58
ms.tgt_platform: multiple
title: Ereignis Sicherheits Konstanten (wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3009b16e468a647ee96b9be365286caba2c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131156"
---
# <a name="event-security-constants"></a><span data-ttu-id="da9eb-104">Ereignis Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="da9eb-104">Event Security Constants</span></span>

<span data-ttu-id="da9eb-105">Im folgenden werden die WMI-Sicherheits Konstanten angezeigt, die für-Ereignisse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da9eb-105">The following shows the WMI security constants used for events.</span></span> <span data-ttu-id="da9eb-106">Sie werden verwendet, um Zugriffs Steuerungs Einträge (Access Control Entries, ACEs) in Sicherheits Beschreibungen festzulegen, die für Ereignisse oder senken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da9eb-106">They are used to set access control entries (ACEs) in security descriptors used for events or sinks.</span></span>

<dl> <dt>

<span data-ttu-id="da9eb-107"><span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**WBEM \_ right \_ Publish**</span><span class="sxs-lookup"><span data-stu-id="da9eb-107"><span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**WBEM\_RIGHT\_PUBLISH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9eb-108">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="da9eb-108">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="da9eb-109">Gibt an, dass das Konto Ereignisse in der Instanz von [**\_ \_ EventFilter**](--eventfilter.md) veröffentlichen kann, die den Ereignis Filter für einen permanenten Consumer definiert.</span><span class="sxs-lookup"><span data-stu-id="da9eb-109">Specifies that the account can publish events to the instance of [**\_\_EventFilter**](--eventfilter.md) that defines the event filter for a permanent consumer.</span></span> <span data-ttu-id="da9eb-110">Verfügbar in wbemcli. h.</span><span class="sxs-lookup"><span data-stu-id="da9eb-110">Available in wbemcli.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da9eb-111"><span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**WBEM \_ right \_ Subscribe**</span><span class="sxs-lookup"><span data-stu-id="da9eb-111"><span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**WBEM\_RIGHT\_SUBSCRIBE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9eb-112">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="da9eb-112">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="da9eb-113">Gibt an, dass ein Consumer die an eine Senke übermittelten Ereignisse abonnieren kann.</span><span class="sxs-lookup"><span data-stu-id="da9eb-113">Specifies that a consumer can subscribe to the events delivered to a sink.</span></span> <span data-ttu-id="da9eb-114">Wird in [**iwbemeventsink:: setsink Security**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)verwendet.</span><span class="sxs-lookup"><span data-stu-id="da9eb-114">Used in [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity).</span></span> <span data-ttu-id="da9eb-115">Verfügbar in wbemcli. h.</span><span class="sxs-lookup"><span data-stu-id="da9eb-115">Available in wbemcli.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da9eb-116"><span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM \_ S \_ unter \_ liegt \_ SDS**</span><span class="sxs-lookup"><span data-stu-id="da9eb-116"><span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM\_S\_SUBJECT\_TO\_SDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9eb-117">274435 (0x43003)</span><span class="sxs-lookup"><span data-stu-id="da9eb-117">274435 (0x43003)</span></span>
</dt> <dt>



<span data-ttu-id="da9eb-118">Der Ereignis Anbieter zeigt an, dass WMI die **\_ sicherheitsbeschreibungenschaft** in jedem Ereignis überprüft (von [**\_ \_ Ereignis**](--event.md)geerbt) und nur Ereignisse an Consumer mit den entsprechenden Zugriffsberechtigungen sendet.</span><span class="sxs-lookup"><span data-stu-id="da9eb-118">Event provider indicates that WMI checks the **SECURITY\_DESCRIPTOR** property in each event (inherited from [**\_\_Event**](--event.md)), and only sends events to consumers with the appropriate access permissions.</span></span> <span data-ttu-id="da9eb-119">Verfügbar in "wbemprov. h".</span><span class="sxs-lookup"><span data-stu-id="da9eb-119">Available in wbemprov.h.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da9eb-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da9eb-120">Requirements</span></span>



| <span data-ttu-id="da9eb-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da9eb-121">Requirement</span></span> | <span data-ttu-id="da9eb-122">Wert</span><span class="sxs-lookup"><span data-stu-id="da9eb-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da9eb-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da9eb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="da9eb-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da9eb-124">Windows Vista</span></span><br/>                                                                                                                               |
| <span data-ttu-id="da9eb-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da9eb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="da9eb-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da9eb-126">Windows Server 2008</span></span><br/>                                                                                                                         |
| <span data-ttu-id="da9eb-127">Header</span><span class="sxs-lookup"><span data-stu-id="da9eb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="da9eb-128"><dt>Wbemcli. h; </dt> <dt>Wbemprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="da9eb-128"><dt>Wbemcli.h; </dt> <dt>Wbemprov.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da9eb-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da9eb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da9eb-130">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="da9eb-130">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="da9eb-131">Verwalten der WMI-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="da9eb-131">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="da9eb-132">Sichern von WMI-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="da9eb-132">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 




