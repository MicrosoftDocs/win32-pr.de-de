---
description: Wird an die CPlApplet-Funktion einer System Steuerungsanwendung gesendet, um Informationen zu einem von der Anwendung unterstützten Dialogfeld anzufordern.
title: CPL_NEWINQUIRE Meldung (cpl. h)
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
ms.openlocfilehash: 72992d4ea867bc091c29feaa99cc1a22c2a02b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977345"
---
# <a name="cpl_newinquire-message"></a><span data-ttu-id="f7265-103">CPL- \_ netwinquire-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f7265-103">CPL\_NEWINQUIRE message</span></span>

<span data-ttu-id="f7265-104">Wird an die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion einer System Steuerungsanwendung gesendet, um Informationen zu einem von der Anwendung unterstützten Dialogfeld anzufordern.</span><span class="sxs-lookup"><span data-stu-id="f7265-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7265-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7265-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7265-106">*uappnum*</span><span class="sxs-lookup"><span data-stu-id="f7265-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="f7265-107">Die Dialogfeld Nummer.</span><span class="sxs-lookup"><span data-stu-id="f7265-107">The dialog box number.</span></span> <span data-ttu-id="f7265-108">Diese Zahl muss zwischen null und einem Wert liegen, der als Antwort auf die [**cpl- \_ GetCount**](cpl-getcount.md) -Nachricht (CPL \_ GetCount – 1) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f7265-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="f7265-109">*lpncpli*</span><span class="sxs-lookup"><span data-stu-id="f7265-109">*lpncpli*</span></span> 
</dt> <dd>

<span data-ttu-id="f7265-110">Die Adresse einer [**newcplinfo**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f7265-110">The address of a [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure.</span></span> <span data-ttu-id="f7265-111">In der System Steuerungsanwendung sollte diese Struktur mit Informationen zum Dialogfeld aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="f7265-111">The Control Panel application should fill this structure with information about the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7265-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7265-112">Return value</span></span>

<span data-ttu-id="f7265-113">Wenn die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion diese Nachricht erfolgreich verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f7265-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7265-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7265-114">Remarks</span></span>

<span data-ttu-id="f7265-115">Um eine bessere Leistung zu erzielen, sollten die meisten Anwendungen **cpl \_ newinquire** ignorieren und stattdessen die [**cpl- \_ Anfrage**](cpl-inquire.md) Nachricht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f7265-115">For better performance, most applications should ignore **CPL\_NEWINQUIRE** and process the [**CPL\_INQUIRE**](cpl-inquire.md) message instead.</span></span>

<span data-ttu-id="f7265-116">Die Systemsteuerung sendet für jedes von der Anwendung unterstützte Dialogfeld eine einmalige **cpl \_** -Meldung.</span><span class="sxs-lookup"><span data-stu-id="f7265-116">The Control Panel sends the **CPL\_NEWINQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="f7265-117">In der Systemsteuerung wird auch eine [**cpl- \_ Anfrage**](cpl-inquire.md) Nachricht für jedes Dialogfeld gesendet.</span><span class="sxs-lookup"><span data-stu-id="f7265-117">The Control Panel also sends a [**CPL\_INQUIRE**](cpl-inquire.md) message for each dialog box.</span></span> <span data-ttu-id="f7265-118">Diese Nachrichten werden unmittelbar nach der [**cpl- \_ GetCount**](cpl-getcount.md) -Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="f7265-118">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="f7265-119">Das System garantiert jedoch nicht die Reihenfolge, in der die **cpl \_** -Anforderungen und die **cpl- \_ Netzwerkmeldungs** -Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7265-119">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="f7265-120">Sie können für das Dialogfeld eine Initialisierung durchführen, wenn Sie eine [**cpl- \_ Anfrage**](cpl-inquire.md)erhalten.</span><span class="sxs-lookup"><span data-stu-id="f7265-120">You can perform initialization for the dialog box when you receive [**CPL\_INQUIRE**](cpl-inquire.md).</span></span> <span data-ttu-id="f7265-121">Wenn Sie Speicher zuweisen müssen, tun Sie dies als Reaktion auf die [**cpl- \_ Init**](cpl-init.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f7265-121">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="f7265-122">[**Cpl \_ "Erkundigen**](cpl-inquire.md) " ist die bevorzugte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f7265-122">[**CPL\_INQUIRE**](cpl-inquire.md) is the preferred message.</span></span> <span data-ttu-id="f7265-123">Der Grund hierfür ist, dass **cpl- \_ Netzteil** Informationen in einem Format zurückgibt, das vom System nicht zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f7265-123">This is because **CPL\_NEWINQUIRE** returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="f7265-124">Folglich müssen Anwendungen, die **cpl- \_ netzwinquire** verarbeiten, jedes Mal geladen werden, wenn die Systemsteuerung die Informationen benötigt, was zu einer deutlichen Verringerung der Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="f7265-124">Consequently, applications that process **CPL\_NEWINQUIRE** must be loaded each time the Control Panel needs the information, resulting in a significant reduction in performance.</span></span>

<span data-ttu-id="f7265-125">Die einzigen Anwendungen, die **cpl- \_ Netzteil** verwenden sollten, sind diejenigen, die Ihr Symbol ändern oder Zeichen folgen auf der Grundlage des Status des Computers anzeigen müssen.</span><span class="sxs-lookup"><span data-stu-id="f7265-125">The only applications that should use **CPL\_NEWINQUIRE** are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="f7265-126">In diesem Fall sollte der [**cpl \_**](cpl-inquire.md) - \_ erstellungshandler den dynamischen cpl- \_ Res-Wert für die Member " **idion**", " **IDName**" oder " **idinfo** " der [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -Struktur angeben, anstatt einen gültigen Ressourcen Bezeichner anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f7265-126">In this case, your [**CPL\_INQUIRE**](cpl-inquire.md) handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="f7265-127">Dies bewirkt, dass in der Systemsteuerung jedes Mal, wenn das Symbol und die Anzeige Zeichenfolgen benötigt werden, die **cpl- \_ Netzteil** Zeichenfolge gesendet wird, sodass Sie basierend auf dem aktuellen Status des Computers Informationen angeben können.</span><span class="sxs-lookup"><span data-stu-id="f7265-127">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="f7265-128">Dies ist natürlich deutlich langsamer als die Verwendung von zwischengespeicherten Informationen.</span><span class="sxs-lookup"><span data-stu-id="f7265-128">Of course, this is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7265-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f7265-129">Requirements</span></span>



| <span data-ttu-id="f7265-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7265-130">Requirement</span></span> | <span data-ttu-id="f7265-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f7265-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f7265-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f7265-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f7265-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7265-133">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f7265-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f7265-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f7265-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7265-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f7265-136">Header</span><span class="sxs-lookup"><span data-stu-id="f7265-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7265-137"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7265-137"><dt>Cpl.h</dt></span></span> </dl> |



 

 
