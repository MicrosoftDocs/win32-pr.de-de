---
title: Fehler Codes (uiautomationcoreapi. h)
description: In diesem Thema werden die von der Microsoft-Benutzeroberflächen Automatisierung verfügbar gemachten Fehlercodes beschrieben.
ms.assetid: f7820aa3-908e-426e-851c-84397019d735
topic_type:
- apiref
api_name:
- UIA_E_ELEMENTNOTAVAILABLE
- UIA_E_ELEMENTNOTENABLED
- UIA_E_INVALIDOPERATION
- UIA_E_NOCLICKABLEPOINT
- UIA_E_NOTSUPPORTED
- UIA_E_PROXYASSEMBLYNOTLOADED
- UIA_E_TIMEOUT
api_location:
- UIAutomationCoreApi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaa03746bfb1a5e56fcac8b39d326581159f459
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040032"
---
# <a name="error-codes-uiautomationcoreapih"></a><span data-ttu-id="2365c-103">Fehler Codes (uiautomationcoreapi. h)</span><span class="sxs-lookup"><span data-stu-id="2365c-103">Error Codes (UIAutomationCoreApi.h)</span></span>

<span data-ttu-id="2365c-104">In diesem Thema werden die von der Microsoft-Benutzeroberflächen Automatisierung verfügbar gemachten Fehlercodes beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2365c-104">This topic describes the error codes exposed by Microsoft UI Automation.</span></span> <span data-ttu-id="2365c-105">Die Liste wird alphabetisch nach dem Namen sortiert.</span><span class="sxs-lookup"><span data-stu-id="2365c-105">The list is sorted alphabetically by name.</span></span>



| <span data-ttu-id="2365c-106">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="2365c-106">Constant/value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="2365c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2365c-107">Description</span></span>                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <span data-ttu-id="2365c-108"><dt>**UIA \_ E \_ elementnotavailable**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="2365c-108"><dt>**UIA\_E\_ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt></span></span> </dl>          | <span data-ttu-id="2365c-109">Gibt an, dass eine Methode für ein virtualisiertes Element oder für ein Element aufgerufen wurde, das nicht mehr vorhanden ist. Dies ist normalerweise darauf zurückzuführen, dass es zerstört wurde.</span><span class="sxs-lookup"><span data-stu-id="2365c-109">Indicates that a method was called on a virtualized element, or on an element that no longer exists, usually because it has been destroyed.</span></span> <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <span data-ttu-id="2365c-110"><dt>**UIA \_ E \_ elementnotenabled**</dt> <dt>0x80040200</dt></span><span class="sxs-lookup"><span data-stu-id="2365c-110"><dt>**UIA\_E\_ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt></span></span> </dl>                | <span data-ttu-id="2365c-111">Gibt an, dass eine Methode, die ein aktiviertes Element benötigt (z. b. [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) oder [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)), für ein Element aufgerufen wurde, das deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="2365c-111">Indicates that a method that requires an enabled element, such as [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) or [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), was called on an element that was disabled.</span></span> <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <span data-ttu-id="2365c-112"><dt>**UIA \_ E \_ InvalidOperation**</dt> <dt>0x80131509</dt></span><span class="sxs-lookup"><span data-stu-id="2365c-112"><dt>**UIA\_E\_INVALIDOPERATION**</dt> <dt>0x80131509</dt></span></span> </dl>                   | <span data-ttu-id="2365c-113">Gibt an, dass die Methode einen ungültigen Vorgang versucht hat.</span><span class="sxs-lookup"><span data-stu-id="2365c-113">Indicates that the method attempted an operation that was not valid.</span></span><br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <span data-ttu-id="2365c-114"><dt>**UIA \_ E \_ noclickablepoint**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="2365c-114"><dt>**UIA\_E\_NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt></span></span> </dl>                   | <span data-ttu-id="2365c-115">Gibt an, dass die [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) -Methode für ein Element aufgerufen wurde, das über keinen durch Klicken aktivierbaren Punkt verfügt.</span><span class="sxs-lookup"><span data-stu-id="2365c-115">Indicates that the [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) method was called on an element that has no clickable point.</span></span><br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <span data-ttu-id="2365c-116"><dt>**UIA \_ E \_ NotSupported**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="2365c-116"><dt>**UIA\_E\_NOTSUPPORTED**</dt> <dt>0x80040204</dt></span></span> </dl>                               | <span data-ttu-id="2365c-117">Gibt an, dass der Anbieter die angegebene Eigenschaft oder das angegebene Steuerelement Muster explizit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2365c-117">Indicates that the provider explicitly does not support the specified property or control pattern.</span></span> <span data-ttu-id="2365c-118">Die Benutzeroberflächen Automatisierung gibt diesen Fehlercode an den Aufrufer zurück, ohne zu versuchen, einen Standardwert anzugeben oder auf einen anderen Anbieter zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="2365c-118">UI Automation will return this error code to the caller without attempting to provide a default value or falling back to another provider.</span></span><br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <span data-ttu-id="2365c-119"><dt>**UIA \_ E \_ proxyassemblynotloaded**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="2365c-119"><dt>**UIA\_E\_PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt></span></span> </dl> | <span data-ttu-id="2365c-120">Gibt an, dass beim Laden einer Assembly, die einen Client seitigen (Proxy-) Anbieter enthält, ein Problem aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2365c-120">Indicates that a problem occurred when loading an assembly that contains a client-side (proxy) provider.</span></span><br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <span data-ttu-id="2365c-121"><dt>**UIA \_ E \_ Timeout**</dt> <dt>0x80131505</dt></span><span class="sxs-lookup"><span data-stu-id="2365c-121"><dt>**UIA\_E\_TIMEOUT**</dt> <dt>0x80131505</dt></span></span> </dl>                                                      | <span data-ttu-id="2365c-122">Gibt an, dass die für einen Prozess oder einen Vorgang vorgesehene Zeit abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="2365c-122">Indicates that the time allotted for a process or operation has expired.</span></span><br/>                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="2365c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2365c-123">Requirements</span></span>



| <span data-ttu-id="2365c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2365c-124">Requirement</span></span> | <span data-ttu-id="2365c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2365c-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2365c-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2365c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2365c-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2365c-127">Windows XP \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2365c-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2365c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2365c-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2365c-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2365c-130">Header</span><span class="sxs-lookup"><span data-stu-id="2365c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2365c-131"><dt>Uiautomationcoreapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2365c-131"><dt>UIAutomationCoreApi.h</dt></span></span> </dl> |



 

 





