---
description: Tritt auf, wenn ein neuer Bericht über die Berichterstellung generiert wird.
ms.assetid: a8df870e-6744-4e8a-a103-56b446da135f
title: Newcivicaddressreport-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: fa786ecee4ce4223cdb7ec0c8400c5c11bf6e192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868891"
---
# <a name="newcivicaddressreport-event"></a><span data-ttu-id="2e9b0-103">Newcivicaddressreport-Ereignis</span><span class="sxs-lookup"><span data-stu-id="2e9b0-103">NewCivicAddressReport event</span></span>

<span data-ttu-id="2e9b0-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2e9b0-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2e9b0-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="2e9b0-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="2e9b0-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="2e9b0-108">Tritt auf, wenn ein neuer Bericht über die Berichterstellung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-108">Occurs when a new civic address report is generated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e9b0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e9b0-109">Syntax</span></span>


```JScript
.NewCivicAddressReport(
  newReport
)
```



## <a name="parameters"></a><span data-ttu-id="2e9b0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e9b0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e9b0-111">*newreport*</span><span class="sxs-lookup"><span data-stu-id="2e9b0-111">*newReport*</span></span> 
</dt> <dd>

<span data-ttu-id="2e9b0-112">Das neue [**LocationDisp. dispcivicaddressreport**](locationdisp-dispcivicaddressreport.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-112">The new [**LocationDisp.DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e9b0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e9b0-113">Return value</span></span>

<span data-ttu-id="2e9b0-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2e9b0-114">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="2e9b0-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e9b0-115">Examples</span></span>

<span data-ttu-id="2e9b0-116">Ein Beispiel für die Verwendung dieses Ereignisses finden Sie unter Überwachen von [Ereignissen für den öffentlichen Adress Bericht](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="2e9b0-116">For an example of how to use this event, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e9b0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e9b0-117">Requirements</span></span>



| <span data-ttu-id="2e9b0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e9b0-118">Requirement</span></span> | <span data-ttu-id="2e9b0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2e9b0-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="2e9b0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e9b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e9b0-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e9b0-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2e9b0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e9b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e9b0-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2e9b0-123">None supported</span></span><br/>                  |



 

