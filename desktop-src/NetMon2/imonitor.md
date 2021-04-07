---
description: Die Imonitor-Schnittstelle stellt Methoden bereit, die den Monitor Vorgang steuern. Diese Methoden werden vom Überwachungs Steuerungs Dienst (Monitor Control Service, mcsvc) aufgerufen.
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: Imonitor-Schnittstelle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 1b6ba91860905010fd14a46cd4608eaee3da80fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863271"
---
# <a name="imonitor-interface"></a><span data-ttu-id="00e24-104">Imonitor-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="00e24-104">IMonitor interface</span></span>

<span data-ttu-id="00e24-105">Die **Imonitor** -Schnittstelle stellt Methoden bereit, die den Monitor Vorgang steuern.</span><span class="sxs-lookup"><span data-stu-id="00e24-105">The **IMonitor** interface provides methods that control monitor operation.</span></span> <span data-ttu-id="00e24-106">Diese Methoden werden vom [*Überwachungs Steuerungs Dienst (Monitor Control Service*](m.md) , mcsvc) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="00e24-106">These methods are called by the [*Monitor Control Service*](m.md) (MCSVC).</span></span>

## <a name="members"></a><span data-ttu-id="00e24-107">Member</span><span class="sxs-lookup"><span data-stu-id="00e24-107">Members</span></span>

<span data-ttu-id="00e24-108">Die **Imonitor** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="00e24-108">The **IMonitor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="00e24-109">**Imonitor** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="00e24-109">**IMonitor** also has these types of members:</span></span>

-   [<span data-ttu-id="00e24-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="00e24-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="00e24-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="00e24-111">Methods</span></span>

<span data-ttu-id="00e24-112">Die **Imonitor** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="00e24-112">The **IMonitor** interface has these methods.</span></span>



| <span data-ttu-id="00e24-113">Methode</span><span class="sxs-lookup"><span data-stu-id="00e24-113">Method</span></span>                                        | <span data-ttu-id="00e24-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00e24-114">Description</span></span>                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00e24-115">**Doconfigure**</span><span class="sxs-lookup"><span data-stu-id="00e24-115">**DoConfigure**</span></span>](imonitor-doconfigure.md)   | <span data-ttu-id="00e24-116">Update Monitor Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="00e24-116">Updates monitor configuration.</span></span><br/>                                                                           |
| [<span data-ttu-id="00e24-117">**Doinitialize**</span><span class="sxs-lookup"><span data-stu-id="00e24-117">**DoInitialize**</span></span>](imonitor-doinitialize.md) | <span data-ttu-id="00e24-118">Initialisiert einen Monitor.</span><span class="sxs-lookup"><span data-stu-id="00e24-118">Initializes a monitor.</span></span><br/>                                                                                   |
| [<span data-ttu-id="00e24-119">**Onframes**</span><span class="sxs-lookup"><span data-stu-id="00e24-119">**OnFrames**</span></span>](imonitor-onframes.md)         | <span data-ttu-id="00e24-120">Gibt den Status eines Frame Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="00e24-120">Indicates the status of a frame event.</span></span><br/>                                                                   |
| [<span data-ttu-id="00e24-121">**OnStart**</span><span class="sxs-lookup"><span data-stu-id="00e24-121">**OnStart**</span></span>](imonitor-onstart.md)           | <span data-ttu-id="00e24-122">Gibt an, dass der Monitor erfolgreich konfiguriert wurde und dass die Datenerfassung im Begriff ist.</span><span class="sxs-lookup"><span data-stu-id="00e24-122">Indicates that the monitor has been configured successfully and that the data capture is about to begin.</span></span><br/> |
| [<span data-ttu-id="00e24-123">**OnStatus**</span><span class="sxs-lookup"><span data-stu-id="00e24-123">**OnStatus**</span></span>](imonitor-onstatus.md)         | <span data-ttu-id="00e24-124">Gibt ein NPP-Status Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="00e24-124">Indicates an NPP status event.</span></span><br/>                                                                           |
| [<span data-ttu-id="00e24-125">**OnStop**</span><span class="sxs-lookup"><span data-stu-id="00e24-125">**OnStop**</span></span>](imonitor-onstop.md)             | <span data-ttu-id="00e24-126">Gibt den Abschluss der Datenerfassung an.</span><span class="sxs-lookup"><span data-stu-id="00e24-126">Indicates data capture completion.</span></span><br/>                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="00e24-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00e24-127">Requirements</span></span>



| <span data-ttu-id="00e24-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00e24-128">Requirement</span></span> | <span data-ttu-id="00e24-129">Wert</span><span class="sxs-lookup"><span data-stu-id="00e24-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="00e24-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00e24-130">Minimum supported client</span></span><br/> | <span data-ttu-id="00e24-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00e24-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="00e24-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00e24-132">Minimum supported server</span></span><br/> | <span data-ttu-id="00e24-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00e24-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="00e24-134">Header</span><span class="sxs-lookup"><span data-stu-id="00e24-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="00e24-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="00e24-135"><dt>Netmon.h</dt></span></span> </dl> |



 

