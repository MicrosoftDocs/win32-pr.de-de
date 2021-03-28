---
description: Sfvm \_ GetPane kann geändert oder nicht verfügbar sein.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: SFVM_GETPANE Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2800be1b7b427e13014686e587b51fc4bf7d7617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960086"
---
# <a name="sfvm_getpane-message"></a><span data-ttu-id="03bad-103">Sfvm \_ GetPane-Nachricht</span><span class="sxs-lookup"><span data-stu-id="03bad-103">SFVM\_GETPANE message</span></span>

<span data-ttu-id="03bad-104">\[**Sfvm \_ "GetPane** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="03bad-104">\[**SFVM\_GETPANE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="03bad-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="03bad-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="03bad-106">Ermöglicht dem Rückruf Objekt, den Status Leistenbereich bereitzustellen, in dem die Internet Zonen Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="03bad-106">Allows the callback object to provide the status bar pane in which to display the Internet zone information.</span></span> <span data-ttu-id="03bad-107">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="03bad-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a><span data-ttu-id="03bad-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="03bad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03bad-109">*paneid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03bad-109">*paneID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03bad-110">ID des angeforderten Bereichs.</span><span class="sxs-lookup"><span data-stu-id="03bad-110">ID of the requested pane.</span></span> <span data-ttu-id="03bad-111">Dabei handelt es sich normalerweise um \_ eine Bereichs Zone, bei der es sich um einen der folgenden Werte handeln kann.</span><span class="sxs-lookup"><span data-stu-id="03bad-111">This is normally PANE\_ZONE, but can be any one of the following values.</span></span>

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span data-ttu-id="03bad-112"><span id="PANE_NONE"></span><span id="pane_none"></span>**Bereich " \_ None"**</span><span class="sxs-lookup"><span data-stu-id="03bad-112"><span id="PANE_NONE"></span><span id="pane_none"></span>**PANE\_NONE**</span></span>


</dt> <dd>

<span data-ttu-id="03bad-113">Kein Bereich.</span><span class="sxs-lookup"><span data-stu-id="03bad-113">No pane.</span></span>

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span data-ttu-id="03bad-114"><span id="PANE_ZONE"></span><span id="pane_zone"></span>**\_Bereichs Zone**</span><span class="sxs-lookup"><span data-stu-id="03bad-114"><span id="PANE_ZONE"></span><span id="pane_zone"></span>**PANE\_ZONE**</span></span>


</dt> <dd>

<span data-ttu-id="03bad-115">Der Bereich "Internet Zone".</span><span class="sxs-lookup"><span data-stu-id="03bad-115">The Internet zone pane.</span></span>

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span data-ttu-id="03bad-116"><span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**Bereich \_ Offline**</span><span class="sxs-lookup"><span data-stu-id="03bad-116"><span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**PANE\_OFFLINE**</span></span>


</dt> <dd>

<span data-ttu-id="03bad-117">Der Offline-Bereich.</span><span class="sxs-lookup"><span data-stu-id="03bad-117">The offline pane.</span></span>

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span data-ttu-id="03bad-118"><span id="PANE_PRINTER"></span><span id="pane_printer"></span>**Bereichs \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="03bad-118"><span id="PANE_PRINTER"></span><span id="pane_printer"></span>**PANE\_PRINTER**</span></span>


</dt> <dd>

<span data-ttu-id="03bad-119">Der Druckanzeige Bereich.</span><span class="sxs-lookup"><span data-stu-id="03bad-119">The print indication pane.</span></span>

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span data-ttu-id="03bad-120"><span id="PANE_SSL"></span><span id="pane_ssl"></span>**Bereich- \_ SSL**</span><span class="sxs-lookup"><span data-stu-id="03bad-120"><span id="PANE_SSL"></span><span id="pane_ssl"></span>**PANE\_SSL**</span></span>


</dt> <dd>

<span data-ttu-id="03bad-121">Der SSL-Bereich.</span><span class="sxs-lookup"><span data-stu-id="03bad-121">The SSL pane.</span></span>

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span data-ttu-id="03bad-122"><span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**Bereichs \_ Navigation**</span><span class="sxs-lookup"><span data-stu-id="03bad-122"><span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**PANE\_NAVIGATION**</span></span>


</dt> <dd>

<span data-ttu-id="03bad-123">Der Navigationsbereich.</span><span class="sxs-lookup"><span data-stu-id="03bad-123">The navigation pane.</span></span>

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span data-ttu-id="03bad-124"><span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**Bereichs Status \_**</span><span class="sxs-lookup"><span data-stu-id="03bad-124"><span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**PANE\_PROGRESS**</span></span>


</dt> <dd>

<span data-ttu-id="03bad-125">Der Bereich der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="03bad-125">The progress bar pane.</span></span>

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span data-ttu-id="03bad-126"><span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**\_Datenschutz im Bereich**</span><span class="sxs-lookup"><span data-stu-id="03bad-126"><span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**PANE\_PRIVACY**</span></span>


</dt> <dd>

<span data-ttu-id="03bad-127">Der Datenschutz Indikator Bereich.</span><span class="sxs-lookup"><span data-stu-id="03bad-127">The privacy indicator pane.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="03bad-128"> Bereich \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="03bad-128">*pane* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03bad-129">Zeiger auf ein **DWORD** , das die Bereichs Nummer enthält.</span><span class="sxs-lookup"><span data-stu-id="03bad-129">Pointer to a **DWORD** containing the pane number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03bad-130">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="03bad-130">Requirements</span></span>



| <span data-ttu-id="03bad-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03bad-131">Requirement</span></span> | <span data-ttu-id="03bad-132">Wert</span><span class="sxs-lookup"><span data-stu-id="03bad-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="03bad-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03bad-133">Minimum supported client</span></span><br/> | <span data-ttu-id="03bad-134">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03bad-134">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="03bad-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03bad-135">Minimum supported server</span></span><br/> | <span data-ttu-id="03bad-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03bad-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="03bad-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="03bad-137">End of client support</span></span><br/>    | <span data-ttu-id="03bad-138">Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="03bad-138">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="03bad-139">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="03bad-139">End of server support</span></span><br/>    | <span data-ttu-id="03bad-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="03bad-140">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="03bad-141">Header</span><span class="sxs-lookup"><span data-stu-id="03bad-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="03bad-142"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="03bad-142"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
