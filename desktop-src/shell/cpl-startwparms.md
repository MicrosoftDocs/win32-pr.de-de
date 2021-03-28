---
description: Wird gesendet, um das CPlApplet zu benachrichtigen, dass der Benutzer das Symbol ausgewählt hat, das einem bestimmten Dialogfeld zugeordnet ist. CPlApplet sollte das entsprechende Dialogfeld anzeigen und alle benutzerdefinierten Tasks ausführen.
title: CPL_STARTWPARMS Meldung (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 04ac5117-39c9-4d3f-b32d-8f8d2b515be1
api_name:
- CPL_STARTWPARMS
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 790779c1c45acbc211fe36e28b2e55d5ae2e60da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958771"
---
# <a name="cpl_startwparms-message"></a><span data-ttu-id="5d665-104">CPL- \_ startwparser-Meldung</span><span class="sxs-lookup"><span data-stu-id="5d665-104">CPL\_STARTWPARMS message</span></span>

<span data-ttu-id="5d665-105">Wird gesendet, um das [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) zu benachrichtigen, dass der Benutzer das Symbol ausgewählt hat, das einem bestimmten Dialogfeld zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5d665-105">Sent to notify [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) that the user has chosen the icon associated with a given dialog box.</span></span> <span data-ttu-id="5d665-106">**CPlApplet** sollte das entsprechende Dialogfeld anzeigen und alle benutzerdefinierten Tasks ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d665-106">**CPlApplet** should display the corresponding dialog box and carry out any user-specified tasks.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d665-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d665-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d665-108">*uappnum*</span><span class="sxs-lookup"><span data-stu-id="5d665-108">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="5d665-109">Die Dialogfeld Nummer.</span><span class="sxs-lookup"><span data-stu-id="5d665-109">The dialog box number.</span></span> <span data-ttu-id="5d665-110">Diese Zahl muss zwischen null und einem Wert liegen, der als Antwort auf die [**cpl- \_ GetCount**](cpl-getcount.md) -Nachricht (CPL \_ GetCount – 1) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5d665-110">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="5d665-111">*lpszextra*</span><span class="sxs-lookup"><span data-stu-id="5d665-111">*lpszExtra*</span></span> 
</dt> <dd>

<span data-ttu-id="5d665-112">Eine Zeichenfolge mit zusätzlichen Ausführungs Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="5d665-112">A string with additional directions for execution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d665-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d665-113">Return value</span></span>

<span data-ttu-id="5d665-114">Gibt **true** zurück, wenn die Meldung behandelt wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="5d665-114">Returns **TRUE** if the message was handled, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d665-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d665-115">Remarks</span></span>

<span data-ttu-id="5d665-116">**Cpl \_ Startwparamems** ähnelt [**cpl \_ dblclk**](cpl-dblclk.md) , ermöglicht Ihnen jedoch, eine Zeichenfolge an [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) anstatt an **int** zu übergeben. Sie können diese Zeichenfolge als flexible Möglichkeit zum Bereitstellen von detaillierten Ausführungs Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d665-116">**CPL\_STARTWPARMS** is similar to [**CPL\_DBLCLK**](cpl-dblclk.md) but allows you to pass a string to [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) instead of an **int**. You can use this string as a flexible way to provide detailed directions for execution.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d665-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5d665-117">Requirements</span></span>



| <span data-ttu-id="5d665-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d665-118">Requirement</span></span> | <span data-ttu-id="5d665-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5d665-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5d665-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d665-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5d665-121">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d665-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="5d665-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d665-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5d665-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d665-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5d665-124">Header</span><span class="sxs-lookup"><span data-stu-id="5d665-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d665-125"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d665-125"><dt>Cpl.h</dt></span></span> </dl> |



 

 
