---
description: Legt den Zustand "automatisch ausblenden" und "Always on-Top" der Windows-Taskleiste fest.
title: ABM_SETSTATE Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a60e156d-19ef-49b9-83fc-138d1a2169f2
api_name:
- ABM_SETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cd21ca49d1a57d870c26e010420f978f1d9b88a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977441"
---
# <a name="abm_setstate-message"></a><span data-ttu-id="00e54-103">ABM- \_ SetState-Meldung</span><span class="sxs-lookup"><span data-stu-id="00e54-103">ABM\_SETSTATE message</span></span>

<span data-ttu-id="00e54-104">Legt den Zustand "automatisch ausblenden" und "Always on-Top" der Windows-Taskleiste fest.</span><span class="sxs-lookup"><span data-stu-id="00e54-104">Sets the autohide and always-on-top states of the Windows taskbar.</span></span>


```C++
SHAppBarMessage(ABM_SETSTATE, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="00e54-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="00e54-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00e54-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="00e54-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="00e54-107">Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="00e54-107">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="00e54-108">Beim Senden dieser Nachricht müssen Sie die **CBSIZE** -und **HWND** -Elemente angeben.</span><span class="sxs-lookup"><span data-stu-id="00e54-108">You must specify the **cbSize** and **hWnd** members when sending this message.</span></span> <span data-ttu-id="00e54-109">Die Daten für den gewünschten Zustand werden im **LPARAM** -Member mit einem der folgenden Werte gesendet.</span><span class="sxs-lookup"><span data-stu-id="00e54-109">Data for the desired state is sent in the **lParam** member using one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="00e54-110"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="00e54-110"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="00e54-111">Automatisch ausblenden und immer am oberen Rand</span><span class="sxs-lookup"><span data-stu-id="00e54-111">Autohide and always-on-top both off</span></span>

</dd> <dt>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>

<span data-ttu-id="00e54-112"><span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ABS \_ AlwaysOnTop**</span><span class="sxs-lookup"><span data-stu-id="00e54-112"><span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ABS\_ALWAYSONTOP**</span></span>


</dt> <dd>

<span data-ttu-id="00e54-113">Always on-Top on, Automatisches Ausblenden Off</span><span class="sxs-lookup"><span data-stu-id="00e54-113">Always-on-top on, autohide off</span></span>

</dd> <dt>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>

<span data-ttu-id="00e54-114"><span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**ABS \_ automatisch ausblenden**</span><span class="sxs-lookup"><span data-stu-id="00e54-114"><span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**ABS\_AUTOHIDE**</span></span>


</dt> <dd>

<span data-ttu-id="00e54-115">Automatisch ausblenden bei, immer am Anfang</span><span class="sxs-lookup"><span data-stu-id="00e54-115">Autohide on, always-on-top off</span></span>

</dd> <dt>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>

<span data-ttu-id="00e54-116"><span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS \_ Autohide \| ABS \_ AlwaysOnTop**</span><span class="sxs-lookup"><span data-stu-id="00e54-116"><span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS\_AUTOHIDE \| ABS\_ALWAYSONTOP**</span></span>


</dt> <dd>

<span data-ttu-id="00e54-117">Automatisch ausblenden und immer am oberen Rand</span><span class="sxs-lookup"><span data-stu-id="00e54-117">Autohide and always-on-top both on</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00e54-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00e54-118">Return value</span></span>

<span data-ttu-id="00e54-119">Gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="00e54-119">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="00e54-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="00e54-120">Requirements</span></span>



| <span data-ttu-id="00e54-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00e54-121">Requirement</span></span> | <span data-ttu-id="00e54-122">Wert</span><span class="sxs-lookup"><span data-stu-id="00e54-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00e54-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00e54-123">Minimum supported client</span></span><br/> | <span data-ttu-id="00e54-124">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00e54-124">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="00e54-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00e54-125">Minimum supported server</span></span><br/> | <span data-ttu-id="00e54-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00e54-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00e54-127">Header</span><span class="sxs-lookup"><span data-stu-id="00e54-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="00e54-128"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="00e54-128"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




