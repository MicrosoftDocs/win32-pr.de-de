---
description: Das Datum und die Uhrzeit, zu der der Bericht generiert wurde.
ms.assetid: b9435384-72e0-42c4-a948-df52621a5ec2
title: LocationDisp. dispcivicaddressreport. Timestamp (Eigenschaft)
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
ms.openlocfilehash: 7b805454a6c2d62a58ba5a2a3de8f5b5095e1db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363389"
---
# <a name="locationdispdispcivicaddressreporttimestamp-property"></a><span data-ttu-id="7af9c-103">LocationDisp. dispcivicaddressreport. Timestamp (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7af9c-103">LocationDisp.DispCivicAddressReport.Timestamp property</span></span>

<span data-ttu-id="7af9c-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7af9c-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7af9c-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7af9c-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7af9c-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="7af9c-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="7af9c-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="7af9c-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="7af9c-108">Das Datum und die Uhrzeit, zu der der Bericht generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7af9c-108">The date and time when the report was generated.</span></span>

<span data-ttu-id="7af9c-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7af9c-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7af9c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7af9c-110">Syntax</span></span>


```JScript
Timestamp = LocationDisp.DispCivicAddressReport.Timestamp
```



## <a name="property-value"></a><span data-ttu-id="7af9c-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7af9c-111">Property value</span></span>

<span data-ttu-id="7af9c-112">Diese Eigenschaft ist ein Schreib geschütztes **Datum**.</span><span class="sxs-lookup"><span data-stu-id="7af9c-112">This property is a read-only **Date**.</span></span> <span data-ttu-id="7af9c-113">Zeitstempel werden als koordinierte Weltzeit (UTC) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7af9c-113">Time stamps are provided as Coordinated Universal Time (UTC).</span></span>

## <a name="remarks"></a><span data-ttu-id="7af9c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7af9c-114">Remarks</span></span>

<span data-ttu-id="7af9c-115">Beachten Sie, dass es für Skriptsprachen wie z. b. Microsoft JScript erforderlich ist, Konvertierungen in andere Zeitformate auszuführen, wenn Sie Zeitstempel als Zeichen folgen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7af9c-115">Note that scripting languages, such as Microsoft JScript, might require you to perform conversions to other time formats when you display time stamps as strings.</span></span>

## <a name="examples"></a><span data-ttu-id="7af9c-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7af9c-116">Examples</span></span>

<span data-ttu-id="7af9c-117">Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie in [einem einfachen Beispiel für einen Bericht über den öffentlichen Adress Bericht](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="7af9c-117">For an example of how to use this property, see [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="7af9c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7af9c-118">Requirements</span></span>



| <span data-ttu-id="7af9c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7af9c-119">Requirement</span></span> | <span data-ttu-id="7af9c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7af9c-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="7af9c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7af9c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7af9c-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7af9c-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7af9c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7af9c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7af9c-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7af9c-124">None supported</span></span><br/>                  |



 

