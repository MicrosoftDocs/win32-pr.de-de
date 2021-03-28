---
description: Wird an die CPlApplet-Funktion einer System Steuerungsanwendung gesendet, um die von der Anwendung unterstützte Anzahl von Dialogfeldern abzurufen.
title: CPL_GETCOUNT Meldung (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6b88b56c-aad7-4144-ab95-15d7eef21861
api_name:
- CPL_GETCOUNT
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3bf8980fa29841d3c5341daeeccf26cea05db80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525391"
---
# <a name="cpl_getcount-message"></a><span data-ttu-id="2a498-103">CPL- \_ GetCount-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2a498-103">CPL\_GETCOUNT message</span></span>

<span data-ttu-id="2a498-104">Wird an die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion einer System Steuerungsanwendung gesendet, um die von der Anwendung unterstützte Anzahl von Dialogfeldern abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2a498-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to retrieve the number of dialog boxes supported by the application.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a498-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a498-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a498-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a498-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2a498-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2a498-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2a498-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a498-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2a498-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2a498-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a498-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a498-110">Return value</span></span>

<span data-ttu-id="2a498-111">Die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion gibt die Anzahl der Dialogfelder zurück, die von der System Steuerungsanwendung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2a498-111">The [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function returns the number of dialog boxes that the Control Panel application supports.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a498-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a498-112">Remarks</span></span>

<span data-ttu-id="2a498-113">Diese Nachricht wird unmittelbar nach der [**cpl- \_ Init**](cpl-init.md) -Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="2a498-113">This message is sent immediately after the [**CPL\_INIT**](cpl-init.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a498-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2a498-114">Requirements</span></span>



| <span data-ttu-id="2a498-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a498-115">Requirement</span></span> | <span data-ttu-id="2a498-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2a498-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2a498-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a498-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2a498-118">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a498-118">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2a498-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a498-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2a498-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a498-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2a498-121">Header</span><span class="sxs-lookup"><span data-stu-id="2a498-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a498-122"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a498-122"><dt>Cpl.h</dt></span></span> </dl> |



 

 
