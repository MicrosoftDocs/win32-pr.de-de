---
description: 'LocationDisp.CivicAddressReportFactory.RequestPermissions-Methode: Öffnet ein Systemdialogfeld, in dem Benutzerberechtigungen für standortfähige Geräte angefordert werden.'
ms.assetid: b213591a-2830-4979-b532-e71cdef1b994
title: LocationDisp.CivicAddressReportFactory.RequestPermissions-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: cab163585fa23839eb894f7ad83f29ed7975e589
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110908"
---
# <a name="locationdispcivicaddressreportfactoryrequestpermissions-method"></a><span data-ttu-id="f1b30-103">LocationDisp.CivicAddressReportFactory.RequestPermissions-Methode</span><span class="sxs-lookup"><span data-stu-id="f1b30-103">LocationDisp.CivicAddressReportFactory.RequestPermissions method</span></span>

<span data-ttu-id="f1b30-104">\[Das Standort-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f1b30-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f1b30-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f1b30-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f1b30-106">Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f1b30-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="f1b30-107">Verwenden Sie die [**Windows.Devices.Geolocation-API,**](/uwp/api/Windows.Devices.Geolocation) um von einer Desktopanwendung aus auf den Standort zuzugreifen.\]</span><span class="sxs-lookup"><span data-stu-id="f1b30-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="f1b30-108">Öffnet ein Systemdialogfeld, in dem Benutzerberechtigungen für standortfähige Geräte angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f1b30-108">Opens a system dialog box to request user permission for location-enabled devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b30-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1b30-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a><span data-ttu-id="f1b30-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1b30-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1b30-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="f1b30-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f1b30-112">Dieser Parameter wird nicht verwendet und sollte auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f1b30-112">This parameter is not used and should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1b30-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1b30-113">Return value</span></span>

<span data-ttu-id="f1b30-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f1b30-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1b30-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1b30-115">Remarks</span></span>

<span data-ttu-id="f1b30-116">Der Aufruf ist synchron, und der Aufrufer wartet, bis das Dialogfeld geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="f1b30-116">The call is synchronous and the caller waits for the dialog box to be closed.</span></span>

> [!Note]  
> <span data-ttu-id="f1b30-117">Wenn eine Anwendung, die im geschützten Modus ausgeführt wird, z. B. ein Browserhilfsobjekt (Browser Helper Object, BHO) für Internet Explorer, **RequestPermissions** aufruft und der Benutzer die Option **Diesen Standortsensor nicht aktivieren** im Dialogfeld aus wählt, wird der Standortanbieter nicht aktiviert, aber Windows zeigt das Dialogfeld erneut an, wenn **RequestPermissions** erneut vom gleichen Benutzer aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f1b30-117">If an application running in protected mode, such as a Browser Helper Object (BHO) for Internet Explorer, calls **RequestPermissions**, and the user chooses the **Don't enable this location sensor** option in the dialog box, the location provider will not be enabled, but Windows will display the dialog box again if **RequestPermissions** is called again by the same user.</span></span> <span data-ttu-id="f1b30-118">Anwendungen, die im geschützten Modus ausgeführt werden, können [**requestPermissions**](/windows/win32/api/locationapi/nf-locationapi-ilocation-requestpermissions) beim Start nicht aufrufen, sodass dem Benutzer bei jedem Start der Anwendung kein möglicherweise unerwünschtes Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f1b30-118">Applications that run in protected mode may choose to not call [**RequestPermissions**](/windows/win32/api/locationapi/nf-locationapi-ilocation-requestpermissions) on startup so that the user does not see a possibly unwanted dialog box each time the application starts.</span></span>

 

## <a name="examples"></a><span data-ttu-id="f1b30-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1b30-119">Examples</span></span>

<span data-ttu-id="f1b30-120">Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="f1b30-120">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1b30-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1b30-121">Requirements</span></span>



| <span data-ttu-id="f1b30-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1b30-122">Requirement</span></span> | <span data-ttu-id="f1b30-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f1b30-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="f1b30-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1b30-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f1b30-125">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1b30-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f1b30-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1b30-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f1b30-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f1b30-127">None supported</span></span><br/>                  |



 

