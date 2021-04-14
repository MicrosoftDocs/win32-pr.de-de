---
title: IWMDRMDeviceApp2-Schnittstelle
description: Die IWMDRMDeviceApp2-Schnittstelle erweitert iwmdrmdeviceapp durch Bereitstellen einer neuen Version der querydevicestatus-Methode.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- IWMDRMDeviceApp2 Interface Windows Media Device Manager
- IWMDRMDeviceApp2 Interface Windows Media Device Manager, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4bfdb023198631b16ffa0e511488fa52423c5e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313134"
---
# <a name="iwmdrmdeviceapp2-interface"></a><span data-ttu-id="929dd-105">IWMDRMDeviceApp2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="929dd-105">IWMDRMDeviceApp2 interface</span></span>

<span data-ttu-id="929dd-106">Die **IWMDRMDeviceApp2** -Schnittstelle erweitert [**iwmdrmdeviceapp**](iwmdrmdeviceapp.md) durch Bereitstellen einer neuen Version der [**querydevicestatus**](iwmdrmdeviceapp-querydevicestatus.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="929dd-106">The **IWMDRMDeviceApp2** interface extends [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) by providing a new version of the [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) method.</span></span> <span data-ttu-id="929dd-107">**QueryDeviceStatus2** ermöglicht dem Aufrufer, eine bestimmte DRM-Anforderung abzufragen.</span><span class="sxs-lookup"><span data-stu-id="929dd-107">**QueryDeviceStatus2** enables the caller to query for a specific DRM requirement.</span></span>

<span data-ttu-id="929dd-108">Um diese Schnittstelle zu erhalten, müssen Sie **cokreateinstance** aufrufen und CLSID \_ wmdrmdeviceapp übergeben.</span><span class="sxs-lookup"><span data-stu-id="929dd-108">To get this interface, call **CoCreateInstance** and pass in CLSID\_WMDRMDeviceApp.</span></span>

> [!Note]  
> <span data-ttu-id="929dd-109">Diese Schnittstelle ist in der Header Datei definiert, die aus wmdrmdeviceapp. idl erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="929dd-109">This interface is defined in the header file built from WMDRMDeviceApp.idl.</span></span> <span data-ttu-id="929dd-110">Dieser Header **\# enthält** "WMDM. h".</span><span class="sxs-lookup"><span data-stu-id="929dd-110">This header **\#includes** "wmdm.h".</span></span> <span data-ttu-id="929dd-111">Möglicherweise müssen Sie diesen Dateinamen ändern, damit er mit dem aus WMDM. idl erstellten Header identisch ist.</span><span class="sxs-lookup"><span data-stu-id="929dd-111">You might need to change this file name to match the header built from WMDM.idl.</span></span>

 

## <a name="members"></a><span data-ttu-id="929dd-112">Member</span><span class="sxs-lookup"><span data-stu-id="929dd-112">Members</span></span>

<span data-ttu-id="929dd-113">Die **IWMDRMDeviceApp2** -Schnittstelle erbt von [**iwmdrmdeviceapp**](iwmdrmdeviceapp.md).</span><span class="sxs-lookup"><span data-stu-id="929dd-113">The **IWMDRMDeviceApp2** interface inherits from [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md).</span></span> <span data-ttu-id="929dd-114">**IWMDRMDeviceApp2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="929dd-114">**IWMDRMDeviceApp2** also has these types of members:</span></span>

-   [<span data-ttu-id="929dd-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="929dd-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="929dd-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="929dd-116">Methods</span></span>

<span data-ttu-id="929dd-117">Die **IWMDRMDeviceApp2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="929dd-117">The **IWMDRMDeviceApp2** interface has these methods.</span></span>



| <span data-ttu-id="929dd-118">Methode</span><span class="sxs-lookup"><span data-stu-id="929dd-118">Method</span></span>                                                            | <span data-ttu-id="929dd-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="929dd-119">Description</span></span>                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="929dd-120">**QueryDeviceStatus2**</span><span class="sxs-lookup"><span data-stu-id="929dd-120">**QueryDeviceStatus2**</span></span>](iwmdrmdeviceapp2-querydevicestatus2.md) | <span data-ttu-id="929dd-121">Fragt ein Gerät nach einem bestimmten DRM-Status oder einer bestimmten Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="929dd-121">Queries a device for a specific DRM status or capability.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="929dd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="929dd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="929dd-123">**Iwmdrmdeviceapp**</span><span class="sxs-lookup"><span data-stu-id="929dd-123">**IWMDRMDeviceApp**</span></span>](iwmdrmdeviceapp.md)
</dt> <dt>

[<span data-ttu-id="929dd-124">**Behandeln geschützter Inhalte in der Anwendung**</span><span class="sxs-lookup"><span data-stu-id="929dd-124">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="929dd-125">**Schnittstellen für Anwendungen**</span><span class="sxs-lookup"><span data-stu-id="929dd-125">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> <dt>

[<span data-ttu-id="929dd-126">**Verwendung von Messungs Inhalten**</span><span class="sxs-lookup"><span data-stu-id="929dd-126">**Metering Content Usage**</span></span>](metering-content-usage.md)
</dt> </dl>

 

 





