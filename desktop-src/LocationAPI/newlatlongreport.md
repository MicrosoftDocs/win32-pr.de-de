---
description: Tritt ein, wenn ein neuer Breiten-/Längengrad Bericht generiert wird.
ms.assetid: 2b1a25a1-ccd6-43f8-979b-c2d414d666a2
title: Newlatlongreport-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: ea305d17169b71d183a8d453e9885d8de878b026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106361089"
---
# <a name="newlatlongreport-event"></a><span data-ttu-id="27c92-103">Newlatlongreport-Ereignis</span><span class="sxs-lookup"><span data-stu-id="27c92-103">NewLatLongReport event</span></span>

<span data-ttu-id="27c92-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="27c92-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="27c92-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="27c92-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="27c92-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="27c92-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="27c92-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="27c92-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="27c92-108">Tritt ein, wenn ein neuer Breiten-/Längengrad Bericht generiert wird.</span><span class="sxs-lookup"><span data-stu-id="27c92-108">Occurs when a new latitude/longitude report is generated.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c92-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="27c92-109">Syntax</span></span>


```JScript
.NewLatLongReport(
  newReport
)
```



## <a name="parameters"></a><span data-ttu-id="27c92-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="27c92-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27c92-111">*newreport*</span><span class="sxs-lookup"><span data-stu-id="27c92-111">*newReport*</span></span> 
</dt> <dd>

<span data-ttu-id="27c92-112">Das neue [**LocationDisp. displatlongreport**](locationdisp-displatlongreport.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="27c92-112">The new [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27c92-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27c92-113">Return value</span></span>

<span data-ttu-id="27c92-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="27c92-114">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="27c92-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27c92-115">Examples</span></span>

<span data-ttu-id="27c92-116">Ein Beispiel für die Verwendung dieses Ereignisses finden Sie unter [lauschen auf latlong-Bericht Ereignisse](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="27c92-116">For an example of how to use this event, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="27c92-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27c92-117">Requirements</span></span>



| <span data-ttu-id="27c92-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27c92-118">Requirement</span></span> | <span data-ttu-id="27c92-119">Wert</span><span class="sxs-lookup"><span data-stu-id="27c92-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="27c92-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27c92-120">Minimum supported client</span></span><br/> | <span data-ttu-id="27c92-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27c92-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="27c92-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27c92-122">Minimum supported server</span></span><br/> | <span data-ttu-id="27c92-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="27c92-123">None supported</span></span><br/>                  |



 

