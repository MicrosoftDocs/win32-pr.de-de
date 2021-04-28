---
description: 'LocationDisp.DispCivicAddressReport.Timestamp-Eigenschaft: Datum und Uhrzeit der Berichtgenerieren.'
ms.assetid: b9435384-72e0-42c4-a948-df52621a5ec2
title: LocationDisp.DispCivicAddressReport.Timestamp (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: d2ed39956bb542aa4e150bf9afa3e59a472a4d91
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110878"
---
# <a name="locationdispdispcivicaddressreporttimestamp-property"></a><span data-ttu-id="6edb8-103">LocationDisp.DispCivicAddressReport.Timestamp (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6edb8-103">LocationDisp.DispCivicAddressReport.Timestamp property</span></span>

<span data-ttu-id="6edb8-104">\[Das Location-API-Objektmodell steht für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="6edb8-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6edb8-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6edb8-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6edb8-106">Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="6edb8-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="6edb8-107">Verwenden Sie die [**Windows.Devices.Geolocation-API,**](/uwp/api/Windows.Devices.Geolocation) um über eine Desktopanwendung auf den Standort zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="6edb8-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="6edb8-108">Das Datum und die Uhrzeit, zu der der Bericht generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6edb8-108">The date and time when the report was generated.</span></span>

<span data-ttu-id="6edb8-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6edb8-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6edb8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6edb8-110">Syntax</span></span>


```JScript
Timestamp = LocationDisp.DispCivicAddressReport.Timestamp
```



## <a name="property-value"></a><span data-ttu-id="6edb8-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6edb8-111">Property value</span></span>

<span data-ttu-id="6edb8-112">Diese Eigenschaft ist ein schreibgeschütztes **Datum.**</span><span class="sxs-lookup"><span data-stu-id="6edb8-112">This property is a read-only **Date**.</span></span> <span data-ttu-id="6edb8-113">Zeitstempel werden als koordinierte Weltzeit (UTC) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6edb8-113">Time stamps are provided as Coordinated Universal Time (UTC).</span></span>

## <a name="remarks"></a><span data-ttu-id="6edb8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6edb8-114">Remarks</span></span>

<span data-ttu-id="6edb8-115">Beachten Sie, dass Skriptsprachen wie Microsoft JScript möglicherweise Konvertierungen in andere Zeitformate erfordern, wenn Sie Zeitstempel als Zeichenfolgen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6edb8-115">Note that scripting languages, such as Microsoft JScript, might require you to perform conversions to other time formats when you display time stamps as strings.</span></span>

## <a name="examples"></a><span data-ttu-id="6edb8-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6edb8-116">Examples</span></span>

<span data-ttu-id="6edb8-117">Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="6edb8-117">For an example of how to use this property, see [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="6edb8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6edb8-118">Requirements</span></span>



| <span data-ttu-id="6edb8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6edb8-119">Requirement</span></span> | <span data-ttu-id="6edb8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6edb8-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="6edb8-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6edb8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6edb8-122">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6edb8-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6edb8-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6edb8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6edb8-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6edb8-124">None supported</span></span><br/>                  |



 

