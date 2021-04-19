---
description: Beendet Ereignisse für das Ereignis des öffentlichen Adress Berichts.
ms.assetid: 6efe26bc-842d-49fc-aec2-e0dfa7f1eb0a
title: LocationDisp. civicaddressreportfactory. stoplisteningforreports-Methode (locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.StopListeningForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 36c58e9db0edb66735dcbd58c8e1968cfa8b1fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353985"
---
# <a name="locationdispcivicaddressreportfactorystoplisteningforreports-method"></a><span data-ttu-id="e369c-103">LocationDisp. civicaddressreportfactory. stoplisteningforreports-Methode</span><span class="sxs-lookup"><span data-stu-id="e369c-103">LocationDisp.CivicAddressReportFactory.StopListeningForReports method</span></span>

<span data-ttu-id="e369c-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e369c-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e369c-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e369c-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e369c-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e369c-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="e369c-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="e369c-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="e369c-108">Beendet Ereignisse für das Ereignis des öffentlichen Adress Berichts.</span><span class="sxs-lookup"><span data-stu-id="e369c-108">Stops civic address report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="e369c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e369c-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.StopListeningForReports()
```



## <a name="parameters"></a><span data-ttu-id="e369c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e369c-110">Parameters</span></span>

<span data-ttu-id="e369c-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e369c-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e369c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e369c-112">Return value</span></span>

<span data-ttu-id="e369c-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e369c-113">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="e369c-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e369c-114">Examples</span></span>

<span data-ttu-id="e369c-115">Ein Beispiel für die Verwendung dieser Methode finden Sie unter Überwachen von [Ereignissen zu öffentlichen Adress Berichten](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="e369c-115">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="e369c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e369c-116">Requirements</span></span>



| <span data-ttu-id="e369c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e369c-117">Requirement</span></span> | <span data-ttu-id="e369c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e369c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e369c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e369c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e369c-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e369c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e369c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e369c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e369c-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e369c-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e369c-123">Header</span><span class="sxs-lookup"><span data-stu-id="e369c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e369c-124"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e369c-124"><dt>Locationapi.h</dt></span></span> </dl> |



 

