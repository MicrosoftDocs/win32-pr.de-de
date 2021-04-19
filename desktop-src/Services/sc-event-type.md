---
description: Gibt einen Typ von Dienststatus Änderungen für die Überwachung und Berichterstellung an.
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: SC_EVENT_TYPE-Enumeration (winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SC_EVENT_TYPE
api_type:
- HeaderDef
api_location:
- Winsvcp.h
ms.openlocfilehash: 55853d13844d3bb255ab0e84a50e8cbbea2d76ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360834"
---
# <a name="sc_event_type-enumeration"></a><span data-ttu-id="e4ac2-103">SC \_ - \_ Ereignistyp-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e4ac2-103">SC\_EVENT\_TYPE enumeration</span></span>

<span data-ttu-id="e4ac2-104">Gibt einen Typ von Dienststatus Änderungen für die Überwachung und Berichterstellung an.</span><span class="sxs-lookup"><span data-stu-id="e4ac2-104">Indicates a type of service status change for monitoring and reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ac2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4ac2-105">Syntax</span></span>


```C++
typedef enum _SC_EVENT_TYPE { 
  SC_EVENT_DATABASE_CHANGE  = 0,
  SC_EVENT_PROPERTY_CHANGE  = 1,
  SC_EVENT_STATUS_CHANGE    = 2
} SC_EVENT_TYPE, *PSC_EVENT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="e4ac2-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e4ac2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e4ac2-107"><span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**Änderung der SC- \_ Ereignis \_ Datenbank \_**</span><span class="sxs-lookup"><span data-stu-id="e4ac2-107"><span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**SC\_EVENT\_DATABASE\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="e4ac2-108">Es wurde ein Dienst hinzugefügt oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e4ac2-108">A service has been added or deleted.</span></span> <span data-ttu-id="e4ac2-109">Der *hservice* -Parameter der Funktion " [**abonnebeservicechangenotifications**](subscribeservicechangenotifications.md) " muss ein Handle für den SCM sein.</span><span class="sxs-lookup"><span data-stu-id="e4ac2-109">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the SCM.</span></span>

</dd> <dt>

<span data-ttu-id="e4ac2-110"><span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**SC- \_ Ereignis \_ Eigenschafts \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="e4ac2-110"><span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**SC\_EVENT\_PROPERTY\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="e4ac2-111">Mindestens eine der Dienst Eigenschaften wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e4ac2-111">One or more of service properties have been updated.</span></span> <span data-ttu-id="e4ac2-112">Der *hservice* -Parameter der Funktion " [**abonnebeservicechangenotifications**](subscribeservicechangenotifications.md) " muss ein Handle für den Dienst sein.</span><span class="sxs-lookup"><span data-stu-id="e4ac2-112">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e4ac2-113"><span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**SC- \_ Ereignis \_ Status \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="e4ac2-113"><span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**SC\_EVENT\_STATUS\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="e4ac2-114">Der Status eines Dienstanbieter hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="e4ac2-114">The status of a service has changed.</span></span> <span data-ttu-id="e4ac2-115">Der *hservice* -Parameter der Funktion " [**abonnebeservicechangenotifications**](subscribeservicechangenotifications.md) " muss ein Handle für den Dienst sein.</span><span class="sxs-lookup"><span data-stu-id="e4ac2-115">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4ac2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4ac2-116">Requirements</span></span>



| <span data-ttu-id="e4ac2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4ac2-117">Requirement</span></span> | <span data-ttu-id="e4ac2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e4ac2-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ac2-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4ac2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e4ac2-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e4ac2-120">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="e4ac2-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4ac2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e4ac2-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4ac2-122">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="e4ac2-123">Header</span><span class="sxs-lookup"><span data-stu-id="e4ac2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4ac2-124"><dt>Winsvcp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4ac2-124"><dt>Winsvcp.h</dt></span></span> </dl> |



 

 




