---
description: Stellt die übergeordnete Klasse dar, von der alle Objekt-Manager-Ereignis Ablauf Verfolgungs Klassen abgeleitet werden.
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: Obtrace-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTrace
api_type:
- NA
api_location: ''
ms.openlocfilehash: ca89f58df9f5dd741da5b1fb8572b153c956cd43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757662"
---
# <a name="obtrace-class"></a><span data-ttu-id="a9e25-103">Obtrace-Klasse</span><span class="sxs-lookup"><span data-stu-id="a9e25-103">ObTrace class</span></span>

<span data-ttu-id="a9e25-104">Stellt die übergeordnete Klasse dar, von der alle Objekt-Manager-Ereignis Ablauf Verfolgungs Klassen abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="a9e25-104">Represents the parent class from which all object manager event trace classes are derived.</span></span>

<span data-ttu-id="a9e25-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a9e25-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9e25-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9e25-106">Syntax</span></span>

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="a9e25-107">Member</span><span class="sxs-lookup"><span data-stu-id="a9e25-107">Members</span></span>

<span data-ttu-id="a9e25-108">Die **obtrace** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="a9e25-108">The **ObTrace** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9e25-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9e25-109">Remarks</span></span>

<span data-ttu-id="a9e25-110">Um die Objekt-Manager-Ereignis Ablauf Verfolgung zu aktivieren, müssen Sie die [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) -Funktion mit dem *informationclass* -Parameter aufrufen, der gleich dem Enumerationswert der [**Trace \_ Info- \_ Klasse**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) , **tracesystemtraceenableflagsinfo** , und dem **enableflags** -Member der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) gleich dem **perf-ob- \_ \_ handle** (0x</span><span class="sxs-lookup"><span data-stu-id="a9e25-110">To enable object manager event tracing, call the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function with the *InformationClass* parameter equal to the [**TRACE\_INFO\_CLASS**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) enumeration value **TraceSystemTraceEnableFlagsInfo** and the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure's **EnableFlags** member equal to **PERF\_OB\_HANDLE** (0x80000040).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9e25-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a9e25-111">Requirements</span></span>



| <span data-ttu-id="a9e25-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9e25-112">Requirement</span></span> | <span data-ttu-id="a9e25-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a9e25-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9e25-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9e25-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a9e25-115">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9e25-115">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a9e25-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9e25-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a9e25-117">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9e25-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a9e25-118">MOF</span><span class="sxs-lookup"><span data-stu-id="a9e25-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9e25-119"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a9e25-119"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 
