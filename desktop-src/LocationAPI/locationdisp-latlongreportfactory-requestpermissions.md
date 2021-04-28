---
description: 'LocationDisp.LatLongReportFactory.RequestPermissions-Methode: Öffnet ein Systemdialogfeld zum Anfordern der Benutzerberechtigung für standortfähige Geräte.'
ms.assetid: 25b4368d-ff9d-4806-a22e-4ae0760d6f0f
title: LocationDisp.LatLongReportFactory.RequestPermissions-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b2d21a032a2e4c08c6f80e4f0ae79349a49ce21
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088928"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a><span data-ttu-id="4737a-103">LocationDisp.LatLongReportFactory.RequestPermissions-Methode</span><span class="sxs-lookup"><span data-stu-id="4737a-103">LocationDisp.LatLongReportFactory.RequestPermissions method</span></span>

<span data-ttu-id="4737a-104">\[Das Location-API-Objektmodell steht für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="4737a-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4737a-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="4737a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="4737a-106">Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="4737a-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="4737a-107">Verwenden Sie die [**Windows.Devices.Geolocation-API,**](/uwp/api/Windows.Devices.Geolocation) um über eine Desktopanwendung auf den Standort zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="4737a-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="4737a-108">Öffnet ein Systemdialogfeld, in dem Benutzerberechtigungen für standortfähige Geräte anfordern werden.</span><span class="sxs-lookup"><span data-stu-id="4737a-108">Opens a system dialog box to request user permission for location-enabled devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="4737a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4737a-109">Syntax</span></span>


```JScript
LocationDisp.LatLongReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a><span data-ttu-id="4737a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4737a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4737a-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="4737a-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="4737a-112">Dieser Parameter wird nicht verwendet und sollte auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4737a-112">This parameter is not used and should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4737a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4737a-113">Return value</span></span>

<span data-ttu-id="4737a-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4737a-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4737a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4737a-115">Remarks</span></span>

<span data-ttu-id="4737a-116">Der Aufruf ist synchron, und der Aufrufer wartet darauf, dass das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="4737a-116">The call is synchronous and the caller waits for the dialog box to be closed.</span></span>

> [!Note]  
> <span data-ttu-id="4737a-117">Wenn eine Anwendung, die im geschützten Modus ausgeführt wird, z. B. ein Browser-Hilfsobjekt (Browser  Helper Object, BHO) für Internet Explorer, **RequestPermissions** aufruft und der Benutzer die Option Diesen Standortsensor nicht aktivieren im Dialogfeld auswählt, wird der Standortanbieter nicht aktiviert, aber Windows zeigt das Dialogfeld erneut an, wenn **RequestPermissions** erneut vom gleichen Benutzer aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4737a-117">If an application running in protected mode, such as a Browser Helper Object (BHO) for Internet Explorer, calls **RequestPermissions**, and the user chooses the **Don't enable this location sensor** option in the dialog box, the location provider will not be enabled, but Windows will display the dialog box again if **RequestPermissions** is called again by the same user.</span></span> <span data-ttu-id="4737a-118">Anwendungen, die im geschützten Modus ausgeführt werden, können **requestPermissions** beim Start nicht aufrufen, damit dem Benutzer nicht bei jedem Start der Anwendung ein möglicherweise unerwünschtes Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4737a-118">Applications that run in protected mode may choose to not call **RequestPermissions** on startup so that the user does not see a possibly unwanted dialog box each time the application starts.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4737a-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4737a-119">Examples</span></span>

<span data-ttu-id="4737a-120">Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Lauschen auf LatLong-Berichtsereignisse.](/uwp/api/Windows.Devices.Geolocation)</span><span class="sxs-lookup"><span data-stu-id="4737a-120">For an example of how to use this method, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="4737a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4737a-121">Requirements</span></span>



| <span data-ttu-id="4737a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4737a-122">Requirement</span></span> | <span data-ttu-id="4737a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4737a-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="4737a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4737a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4737a-125">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4737a-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4737a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4737a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4737a-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4737a-127">None supported</span></span><br/>                  |



 

