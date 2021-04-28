---
description: 'CPL_NEWINQUIRE: Wird an die CPlApplet-Funktion einer Systemsteuerung-Anwendung gesendet, um Informationen zu einem Dialogfeld an fordern, das von der Anwendung unterstützt wird.'
title: CPL_NEWINQUIRE (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: af52889c-7180-4690-8ed1-a0eb0a9dff35
api_name:
- CPL_NEWINQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 90c5adf31c01fbab1b62aafd0714d165092f4e23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104438"
---
# <a name="cpl_newinquire-message"></a><span data-ttu-id="1d07e-103">CPL \_ NEWINQUIRE-Nachricht</span><span class="sxs-lookup"><span data-stu-id="1d07e-103">CPL\_NEWINQUIRE message</span></span>

<span data-ttu-id="1d07e-104">Wird an die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) einer Systemsteuerung, um Informationen zu einem Von der Anwendung unterstützten Dialogfeld an fordern.</span><span class="sxs-lookup"><span data-stu-id="1d07e-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d07e-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d07e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d07e-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="1d07e-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="1d07e-107">Die Nummer des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="1d07e-107">The dialog box number.</span></span> <span data-ttu-id="1d07e-108">Diese Zahl muss im Bereich 0 bis 1 kleiner als der Wert liegen, der als Antwort auf die [**CPL \_ GETCOUNT-Nachricht**](cpl-getcount.md) (CPL \_ GETCOUNT – 1) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1d07e-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="1d07e-109">*lpncpli*</span><span class="sxs-lookup"><span data-stu-id="1d07e-109">*lpncpli*</span></span> 
</dt> <dd>

<span data-ttu-id="1d07e-110">Die Adresse einer [**NEWCPLINFO-Struktur.**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)</span><span class="sxs-lookup"><span data-stu-id="1d07e-110">The address of a [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure.</span></span> <span data-ttu-id="1d07e-111">Die Systemsteuerung-Anwendung sollte diese Struktur mit Informationen zum Dialogfeld füllen.</span><span class="sxs-lookup"><span data-stu-id="1d07e-111">The Control Panel application should fill this structure with information about the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d07e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d07e-112">Return value</span></span>

<span data-ttu-id="1d07e-113">Wenn die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) diese Nachricht erfolgreich verarbeitet, sollte sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1d07e-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d07e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d07e-114">Remarks</span></span>

<span data-ttu-id="1d07e-115">Um eine bessere Leistung zu erzielen, sollten die meisten Anwendungen **CPL \_ NEWINQUIRE** ignorieren und stattdessen die [**\_ CPL-Nachricht FÜR DEN VORGANG VERARBEITEN.**](cpl-inquire.md)</span><span class="sxs-lookup"><span data-stu-id="1d07e-115">For better performance, most applications should ignore **CPL\_NEWINQUIRE** and process the [**CPL\_INQUIRE**](cpl-inquire.md) message instead.</span></span>

<span data-ttu-id="1d07e-116">Der Systemsteuerung sendet die **CPL \_ NEWINQUIRE-Nachricht** einmal für jedes Dialogfeld, das von Ihrer Anwendung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1d07e-116">The Control Panel sends the **CPL\_NEWINQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="1d07e-117">Der Systemsteuerung sendet auch eine [**\_ CPL-NACHRICHT FÜR JEDES**](cpl-inquire.md) Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="1d07e-117">The Control Panel also sends a [**CPL\_INQUIRE**](cpl-inquire.md) message for each dialog box.</span></span> <span data-ttu-id="1d07e-118">Diese Nachrichten werden unmittelbar nach der [**CPL \_ GETCOUNT-Nachricht**](cpl-getcount.md) gesendet.</span><span class="sxs-lookup"><span data-stu-id="1d07e-118">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="1d07e-119">Das System garantiert jedoch nicht die Reihenfolge, in der **die \_ CPL-NACHRICHTEN FÜR DIE NACHRICHTEN ZU UND** **\_ NEWINQUIRE** gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d07e-119">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="1d07e-120">Sie können die Initialisierung für das Dialogfeld ausführen, wenn Sie [**\_ CPL-BENACHRICHTIGUNG erhalten.**](cpl-inquire.md)</span><span class="sxs-lookup"><span data-stu-id="1d07e-120">You can perform initialization for the dialog box when you receive [**CPL\_INQUIRE**](cpl-inquire.md).</span></span> <span data-ttu-id="1d07e-121">Wenn Sie Arbeitsspeicher zuordnen müssen, tun Sie dies als Reaktion auf die [**\_ CPL-INIT-Nachricht.**](cpl-init.md)</span><span class="sxs-lookup"><span data-stu-id="1d07e-121">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="1d07e-122">[**CPL \_ DIE**](cpl-inquire.md) VORZUGSMELDUNG ist die bevorzugte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1d07e-122">[**CPL\_INQUIRE**](cpl-inquire.md) is the preferred message.</span></span> <span data-ttu-id="1d07e-123">Dies liegt **daran, dass CPL \_ NEWINQUIRE** Informationen in einer Form zurückgibt, die das System nicht zwischenspeichern kann.</span><span class="sxs-lookup"><span data-stu-id="1d07e-123">This is because **CPL\_NEWINQUIRE** returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="1d07e-124">Folglich müssen Anwendungen, die **CPL \_ NEWINQUIRE** verarbeiten, jedes Mal geladen werden, wenn die Systemsteuerung die Informationen benötigt, was zu einer erheblichen Leistungsreduzierung führt.</span><span class="sxs-lookup"><span data-stu-id="1d07e-124">Consequently, applications that process **CPL\_NEWINQUIRE** must be loaded each time the Control Panel needs the information, resulting in a significant reduction in performance.</span></span>

<span data-ttu-id="1d07e-125">Die einzigen Anwendungen, die **CPL \_ NEWINQUIRE** verwenden sollten, sind anwendungen, die ihr Symbol ändern oder Zeichenfolgen basierend auf dem Zustand des Computers anzeigen müssen.</span><span class="sxs-lookup"><span data-stu-id="1d07e-125">The only applications that should use **CPL\_NEWINQUIRE** are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="1d07e-126">In diesem Fall sollte Ihr [**\_ CPL-HANDLER DEN**](cpl-inquire.md) \_ DYNAMISCHEN \_ RES-Wert für die Member **idIcon,** **idName** oder **idInfo** der [**CPLINFO-Struktur**](/windows/win32/api/cpl/ns-cpl-cplinfo) angeben, anstatt einen gültigen Ressourcenbezeichner anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1d07e-126">In this case, your [**CPL\_INQUIRE**](cpl-inquire.md) handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="1d07e-127">Dadurch sendet die Systemsteuerung die **CPL \_ NEWINQUIRE-Nachricht** jedes Mal, wenn sie das Symbol benötigt, und zeigt Zeichenfolgen an, sodass Sie Informationen basierend auf dem aktuellen Status des Computers angeben können.</span><span class="sxs-lookup"><span data-stu-id="1d07e-127">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="1d07e-128">Dies ist natürlich deutlich langsamer als die Verwendung zwischengespeicherter Informationen.</span><span class="sxs-lookup"><span data-stu-id="1d07e-128">Of course, this is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d07e-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d07e-129">Requirements</span></span>



| <span data-ttu-id="1d07e-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d07e-130">Requirement</span></span> | <span data-ttu-id="1d07e-131">Wert</span><span class="sxs-lookup"><span data-stu-id="1d07e-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1d07e-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d07e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1d07e-133">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d07e-133">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1d07e-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d07e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1d07e-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d07e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1d07e-136">Header</span><span class="sxs-lookup"><span data-stu-id="1d07e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d07e-137"><dt>Cpl.h</dt></span><span class="sxs-lookup"><span data-stu-id="1d07e-137"><dt>Cpl.h</dt></span></span> </dl> |



 

 
