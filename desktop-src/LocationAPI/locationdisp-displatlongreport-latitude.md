---
description: Aktueller Breitengrad in Grad.
ms.assetid: 24a4e75c-5162-406a-bf34-471387bff5d9
title: LocationDisp. displatlongreport. Latitude (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Latitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7f1bb6e7441b4e007c972f43bb45f59236ebe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359488"
---
# <a name="locationdispdisplatlongreportlatitude-property"></a><span data-ttu-id="b1692-103">LocationDisp. displatlongreport. Latitude (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b1692-103">LocationDisp.DispLatLongReport.Latitude property</span></span>

<span data-ttu-id="b1692-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b1692-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b1692-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b1692-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b1692-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b1692-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="b1692-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="b1692-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="b1692-108">Aktueller Breitengrad in Grad.</span><span class="sxs-lookup"><span data-stu-id="b1692-108">Current latitude, in degrees.</span></span> <span data-ttu-id="b1692-109">Der Breitengrad liegt zwischen-90 und 90, wobei North positiv ist.</span><span class="sxs-lookup"><span data-stu-id="b1692-109">The latitude is between -90 and 90, where north is positive.</span></span>

<span data-ttu-id="b1692-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b1692-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1692-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1692-111">Syntax</span></span>


```JScript
Latitude = LocationDisp.DispLatLongReport.Latitude
```



## <a name="property-value"></a><span data-ttu-id="b1692-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b1692-112">Property value</span></span>

<span data-ttu-id="b1692-113">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (Gleit Komma Wert mit doppelter Genauigkeit).</span><span class="sxs-lookup"><span data-stu-id="b1692-113">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="b1692-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1692-114">Examples</span></span>

<span data-ttu-id="b1692-115">Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [Beispiel für einen einfachen latlong-Bericht](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="b1692-115">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1692-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1692-116">Requirements</span></span>



| <span data-ttu-id="b1692-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1692-117">Requirement</span></span> | <span data-ttu-id="b1692-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b1692-118">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="b1692-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1692-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b1692-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1692-120">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b1692-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1692-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b1692-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b1692-122">None supported</span></span><br/>                  |



 

