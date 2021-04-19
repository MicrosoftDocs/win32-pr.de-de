---
description: Öffnet ein System Dialogfeld zum Anfordern von Benutzerberechtigungen für Geräte, die für den Standort aktiviert sind.
ms.assetid: 25b4368d-ff9d-4806-a22e-4ae0760d6f0f
title: LocationDisp. latlongreportfactory. requestberechtigungs Methode
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
ms.openlocfilehash: ed789aca4b6c9d0db50a3e7b6cae33d55d22920c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358542"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a><span data-ttu-id="36a69-103">LocationDisp. latlongreportfactory. requestberechtigungs Methode</span><span class="sxs-lookup"><span data-stu-id="36a69-103">LocationDisp.LatLongReportFactory.RequestPermissions method</span></span>

<span data-ttu-id="36a69-104">\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="36a69-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="36a69-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="36a69-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="36a69-106">Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="36a69-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="36a69-107">Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="36a69-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="36a69-108">Öffnet ein System Dialogfeld zum Anfordern von Benutzerberechtigungen für Geräte, die für den Standort aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="36a69-108">Opens a system dialog box to request user permission for location-enabled devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="36a69-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="36a69-109">Syntax</span></span>


```JScript
LocationDisp.LatLongReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a><span data-ttu-id="36a69-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="36a69-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36a69-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="36a69-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="36a69-112">Dieser Parameter wird nicht verwendet und sollte auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="36a69-112">This parameter is not used and should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36a69-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36a69-113">Return value</span></span>

<span data-ttu-id="36a69-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="36a69-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36a69-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36a69-115">Remarks</span></span>

<span data-ttu-id="36a69-116">Der Aufruf erfolgt synchron, und der Aufrufer wartet darauf, dass das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="36a69-116">The call is synchronous and the caller waits for the dialog box to be closed.</span></span>

> [!Note]  
> <span data-ttu-id="36a69-117">Wenn eine Anwendung, die im geschützten Modus ausgeführt wird, z. b. ein Browserhilfsobjekt (BHO) für Internet Explorer, **requestberechtigungen** aufruft und der Benutzer die Option **diesen Speicherort nicht aktivieren** im Dialogfeld aktiviert, wird der Speicherort Anbieter nicht aktiviert, aber Windows zeigt das Dialogfeld erneut an, wenn **requestberechtigungs Berechtigungen** vom gleichen Benutzer erneut aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="36a69-117">If an application running in protected mode, such as a Browser Helper Object (BHO) for Internet Explorer, calls **RequestPermissions**, and the user chooses the **Don't enable this location sensor** option in the dialog box, the location provider will not be enabled, but Windows will display the dialog box again if **RequestPermissions** is called again by the same user.</span></span> <span data-ttu-id="36a69-118">Anwendungen, die im geschützten Modus ausgeführt werden, können **anfordererberechtigungen** beim Start nicht aufrufen, damit dem Benutzer bei jedem Start der Anwendung kein möglicherweise unerwünschtes Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="36a69-118">Applications that run in protected mode may choose to not call **RequestPermissions** on startup so that the user does not see a possibly unwanted dialog box each time the application starts.</span></span>

 

## <a name="examples"></a><span data-ttu-id="36a69-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36a69-119">Examples</span></span>

<span data-ttu-id="36a69-120">Ein Beispiel für die Verwendung dieser Methode finden Sie unter [lauschen auf latlong-Bericht Ereignisse](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="36a69-120">For an example of how to use this method, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="36a69-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36a69-121">Requirements</span></span>



| <span data-ttu-id="36a69-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36a69-122">Requirement</span></span> | <span data-ttu-id="36a69-123">Wert</span><span class="sxs-lookup"><span data-stu-id="36a69-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="36a69-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36a69-124">Minimum supported client</span></span><br/> | <span data-ttu-id="36a69-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36a69-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="36a69-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36a69-126">Minimum supported server</span></span><br/> | <span data-ttu-id="36a69-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="36a69-127">None supported</span></span><br/>                  |



 

