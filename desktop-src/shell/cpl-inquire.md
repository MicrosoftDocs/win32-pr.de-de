---
description: 'CPL_INQUIRE: Wird an die CPlApplet-Funktion einer Systemsteuerung-Anwendung gesendet, um Informationen zu einem dialogfeld an anforderungsbasierten Dialog zu erhalten, das von der Anwendung unterstützt wird.'
title: CPL_INQUIRE (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: daca87b7-f1ee-40f4-95d2-3150b595151e
api_name:
- CPL_INQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f9962ff94e8bf80041d7b61ecf97220d573131fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104468"
---
# <a name="cpl_inquire-message"></a><span data-ttu-id="f92e9-103">\_CPL-NACHRICHT ZU 10000000</span><span class="sxs-lookup"><span data-stu-id="f92e9-103">CPL\_INQUIRE message</span></span>

<span data-ttu-id="f92e9-104">Wird an die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) einer Systemsteuerung, um Informationen zu einem Von der Anwendung unterstützten Dialogfeld an fordern.</span><span class="sxs-lookup"><span data-stu-id="f92e9-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="f92e9-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f92e9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f92e9-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="f92e9-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="f92e9-107">Die Nummer des Dialogfelds.</span><span class="sxs-lookup"><span data-stu-id="f92e9-107">The dialog box number.</span></span> <span data-ttu-id="f92e9-108">Diese Zahl muss im Bereich 0 bis 1 kleiner als der Wert liegen, der als Antwort auf die [**CPL \_ GETCOUNT-Nachricht**](cpl-getcount.md) (CPL \_ GETCOUNT – 1) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f92e9-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="f92e9-109">*lpcpli*</span><span class="sxs-lookup"><span data-stu-id="f92e9-109">*lpcpli*</span></span> 
</dt> <dd>

<span data-ttu-id="f92e9-110">Die Adresse einer [**CPLINFO-Struktur.**](/windows/win32/api/cpl/ns-cpl-cplinfo)</span><span class="sxs-lookup"><span data-stu-id="f92e9-110">The address of a [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure.</span></span> <span data-ttu-id="f92e9-111">Die Anwendung muss diese Struktur mit Ressourcenbezeichnern für das Symbol, den Kurznamen, die Beschreibung und alle benutzerdefinierten Werte füllen, die dem Dialogfeld zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f92e9-111">The application must fill this structure with resource identifiers for the icon, short name, description, and any user-defined value associated with the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f92e9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f92e9-112">Return value</span></span>

<span data-ttu-id="f92e9-113">Wenn die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) diese Nachricht erfolgreich verarbeitet, sollte sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f92e9-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f92e9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f92e9-114">Remarks</span></span>

<span data-ttu-id="f92e9-115">Der Systemsteuerung sendet die **\_ CPL-NACHRICHT FÜR ALLE** Dialogfelder, die von Ihrer Anwendung unterstützt werden, einmal.</span><span class="sxs-lookup"><span data-stu-id="f92e9-115">The Control Panel sends the **CPL\_INQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="f92e9-116">Der Systemsteuerung sendet auch eine [**CPL \_ NEWINQUIRE-Nachricht**](cpl-newinquire.md) für jedes Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="f92e9-116">The Control Panel also sends a [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message for each dialog box.</span></span> <span data-ttu-id="f92e9-117">Diese Nachrichten werden unmittelbar nach der [**CPL \_ GETCOUNT-Nachricht**](cpl-getcount.md) gesendet.</span><span class="sxs-lookup"><span data-stu-id="f92e9-117">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="f92e9-118">Das System garantiert jedoch nicht die Reihenfolge, in der **die \_ CPL-NACHRICHTEN FÜR DIE NACHRICHTEN ZU UND** **\_ NEWINQUIRE** gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="f92e9-118">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="f92e9-119">Sie können die Initialisierung für das Dialogfeld ausführen, wenn Sie **\_ CPL-BENACHRICHTIGUNG erhalten.**</span><span class="sxs-lookup"><span data-stu-id="f92e9-119">You can perform initialization for the dialog box when you receive **CPL\_INQUIRE**.</span></span> <span data-ttu-id="f92e9-120">Wenn Sie Arbeitsspeicher zuordnen müssen, tun Sie dies als Reaktion auf die [**\_ CPL-INIT-Nachricht.**](cpl-init.md)</span><span class="sxs-lookup"><span data-stu-id="f92e9-120">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="f92e9-121">Die [**\_ CPL-Nachricht NEWINQUIRE**](cpl-newinquire.md) gibt Informationen in einer Form zurück, die das System nicht zwischenspeichern kann.</span><span class="sxs-lookup"><span data-stu-id="f92e9-121">The [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="f92e9-122">Aus diesem Grund sollten die [**meisten CPlApplet-Funktionen**](/windows/win32/api/cpl/nc-cpl-applet_proc) **\_ CPL-11000000111888888CPL- UND CPL** **\_ NEWINQUIRE-Funktionen ignorieren.**</span><span class="sxs-lookup"><span data-stu-id="f92e9-122">For this reason, most [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) functions should process **CPL\_INQUIRE** and ignore **CPL\_NEWINQUIRE**.</span></span>

<span data-ttu-id="f92e9-123">Die einzigen Anwendungen, die [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) verwenden sollten, sind diejenigen, die ihr Symbol ändern oder Zeichenfolgen basierend auf dem Zustand des Computers anzeigen müssen.</span><span class="sxs-lookup"><span data-stu-id="f92e9-123">The only applications that should use [**CPL\_NEWINQUIRE**](cpl-newinquire.md) are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="f92e9-124">In diesem Fall sollte Ihr **\_ CPL-HANDLER DEN** \_ DYNAMISCHEN \_ RES-Wert für die Member **idIcon,** **idName** oder **idInfo** der [**CPLINFO-Struktur**](/windows/win32/api/cpl/ns-cpl-cplinfo) angeben, anstatt einen gültigen Ressourcenbezeichner anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f92e9-124">In this case, your **CPL\_INQUIRE** handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="f92e9-125">Dadurch sendet die Systemsteuerung die **CPL \_ NEWINQUIRE-Nachricht** jedes Mal, wenn sie das Symbol benötigt, und zeigt Zeichenfolgen an, sodass Sie Informationen basierend auf dem aktuellen Status des Computers angeben können.</span><span class="sxs-lookup"><span data-stu-id="f92e9-125">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="f92e9-126">Dies ist erheblich langsamer als die Verwendung zwischengespeicherter Informationen.</span><span class="sxs-lookup"><span data-stu-id="f92e9-126">This is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f92e9-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f92e9-127">Requirements</span></span>



| <span data-ttu-id="f92e9-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f92e9-128">Requirement</span></span> | <span data-ttu-id="f92e9-129">Wert</span><span class="sxs-lookup"><span data-stu-id="f92e9-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f92e9-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f92e9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f92e9-131">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f92e9-131">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f92e9-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f92e9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f92e9-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f92e9-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f92e9-134">Header</span><span class="sxs-lookup"><span data-stu-id="f92e9-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f92e9-135"><dt>Cpl.h</dt></span><span class="sxs-lookup"><span data-stu-id="f92e9-135"><dt>Cpl.h</dt></span></span> </dl> |



 

 
