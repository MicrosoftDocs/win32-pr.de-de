---
title: Komplexer filterlisttype-Typ
description: Definiert eine Liste von Filtern, die von einem etw-Controller an Ihren Anbieter übergeben werden können, um die zu schreibenden Ereignisse weiter einzuschränken.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- Filterlisttype Complex-Typ EventLog
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1071fbbb9eba6bf6ebf0d74d4caaac50e1ccce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341217"
---
# <a name="filterlisttype-complex-type"></a><span data-ttu-id="76387-104">Komplexer filterlisttype-Typ</span><span class="sxs-lookup"><span data-stu-id="76387-104">FilterListType Complex Type</span></span>

<span data-ttu-id="76387-105">Definiert eine Liste von Filtern, die von einem etw-Controller an Ihren Anbieter übergeben werden können, um die zu schreibenden Ereignisse weiter einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="76387-105">Defines a list of filters that an ETW controller can pass to your provider to further limit the events that it writes.</span></span>

``` syntax
<xs:complexType name="FilterListType">
    <xs:sequence>
        <xs:element name="filter"
            type="FilterType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="76387-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76387-106">Child elements</span></span>



| <span data-ttu-id="76387-107">Element</span><span class="sxs-lookup"><span data-stu-id="76387-107">Element</span></span>    | <span data-ttu-id="76387-108">type</span><span class="sxs-lookup"><span data-stu-id="76387-108">Type</span></span>                                                             | <span data-ttu-id="76387-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76387-109">Description</span></span>                   |
|------------|------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="76387-110">**filter**</span><span class="sxs-lookup"><span data-stu-id="76387-110">**filter**</span></span> | [<span data-ttu-id="76387-111">**Filter Type**</span><span class="sxs-lookup"><span data-stu-id="76387-111">**FilterType**</span></span>](eventmanifestschema-filtertype-complextype.md) | <span data-ttu-id="76387-112">Eine Liste mit Filtern.</span><span class="sxs-lookup"><span data-stu-id="76387-112">A list of filters.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="76387-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76387-113">Remarks</span></span>

<span data-ttu-id="76387-114">Ein etw-Controller ist eine Anwendung, die die [**Start Trace**](/windows/desktop/ETW/starttrace) -Funktion aufruft, um eine ETW-Sitzung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="76387-114">An ETW controller is an application that calls the [**StartTrace**](/windows/desktop/ETW/starttrace) function to create an ETW session.</span></span> <span data-ttu-id="76387-115">Weitere Informationen finden Sie unter [Steuern von Ereignis Ablauf Verfolgungs Sitzungen](/windows/desktop/ETW/controlling-event-tracing-sessions).</span><span class="sxs-lookup"><span data-stu-id="76387-115">For details, see [Controlling Event Tracing Sessions](/windows/desktop/ETW/controlling-event-tracing-sessions).</span></span> <span data-ttu-id="76387-116">Der Controller kann die [**tdhenumerateproviderfilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) -Funktion verwenden, um die von Ihnen definierten Filter aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="76387-116">The controller can use the [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) function to enumerate the filters that you define.</span></span> <span data-ttu-id="76387-117">Der Controller kann dann einen oder mehrere der Filter übergeben, wenn die [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) -Funktion aufgerufen wird, um den Anbieter zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="76387-117">The controller can then pass one or more of the filters when it calls the [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) function to enable your provider.</span></span> <span data-ttu-id="76387-118">Der Anbieter empfängt die Filter zusammen mit den restlichen enable-Parametern in Ihrer [*enablecallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) -Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="76387-118">Your provider receives the filters, along with the rest of the enable parameters, in your [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) callback function.</span></span>

## <a name="requirements"></a><span data-ttu-id="76387-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76387-119">Requirements</span></span>



| <span data-ttu-id="76387-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76387-120">Requirement</span></span> | <span data-ttu-id="76387-121">Wert</span><span class="sxs-lookup"><span data-stu-id="76387-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="76387-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76387-122">Minimum supported client</span></span><br/> | <span data-ttu-id="76387-123">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76387-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="76387-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76387-124">Minimum supported server</span></span><br/> | <span data-ttu-id="76387-125">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76387-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

