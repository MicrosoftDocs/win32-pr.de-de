---
description: Wird an die CPlApplet-Funktion einer System Steuerungsanwendung gesendet, um Informationen zu einem von der Anwendung unterstützten Dialogfeld anzufordern.
title: CPL_INQUIRE Meldung (cpl. h)
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
ms.openlocfilehash: 8f4c75a2610dab9e94a97eb7920c9de43cf44efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128464"
---
# <a name="cpl_inquire-message"></a><span data-ttu-id="ce2ae-103">CPL- \_ Anfrage Nachricht</span><span class="sxs-lookup"><span data-stu-id="ce2ae-103">CPL\_INQUIRE message</span></span>

<span data-ttu-id="ce2ae-104">Wird an die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion einer System Steuerungsanwendung gesendet, um Informationen zu einem von der Anwendung unterstützten Dialogfeld anzufordern.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce2ae-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce2ae-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce2ae-106">*uappnum*</span><span class="sxs-lookup"><span data-stu-id="ce2ae-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="ce2ae-107">Die Dialogfeld Nummer.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-107">The dialog box number.</span></span> <span data-ttu-id="ce2ae-108">Diese Zahl muss zwischen null und einem Wert liegen, der als Antwort auf die [**cpl- \_ GetCount**](cpl-getcount.md) -Nachricht (CPL \_ GetCount – 1) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="ce2ae-109">*lpcpli*</span><span class="sxs-lookup"><span data-stu-id="ce2ae-109">*lpcpli*</span></span> 
</dt> <dd>

<span data-ttu-id="ce2ae-110">Die Adresse einer [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-110">The address of a [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure.</span></span> <span data-ttu-id="ce2ae-111">Die Anwendung muss diese Struktur mit Ressourcen Bezeichner für das Symbol, den Kurznamen, die Beschreibung und jeden benutzerdefinierten Wert ausfüllen, der dem Dialogfeld zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-111">The application must fill this structure with resource identifiers for the icon, short name, description, and any user-defined value associated with the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce2ae-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce2ae-112">Return value</span></span>

<span data-ttu-id="ce2ae-113">Wenn die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion diese Nachricht erfolgreich verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce2ae-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce2ae-114">Remarks</span></span>

<span data-ttu-id="ce2ae-115">Die Systemsteuerung sendet die **cpl- \_ Anfrage** Nachricht einmal für jedes von der Anwendung unterstützte Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-115">The Control Panel sends the **CPL\_INQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="ce2ae-116">In der Systemsteuerung wird auch eine [**cpl- \_ netzernachricht**](cpl-newinquire.md) für jedes Dialogfeld gesendet.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-116">The Control Panel also sends a [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message for each dialog box.</span></span> <span data-ttu-id="ce2ae-117">Diese Nachrichten werden unmittelbar nach der [**cpl- \_ GetCount**](cpl-getcount.md) -Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-117">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="ce2ae-118">Das System garantiert jedoch nicht die Reihenfolge, in der die **cpl \_** -Anforderungen und die **cpl- \_ Netzwerkmeldungs** -Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-118">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="ce2ae-119">Sie können für das Dialogfeld eine Initialisierung durchführen, wenn Sie eine **cpl- \_ Anfrage** erhalten.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-119">You can perform initialization for the dialog box when you receive **CPL\_INQUIRE**.</span></span> <span data-ttu-id="ce2ae-120">Wenn Sie Speicher zuweisen müssen, tun Sie dies als Reaktion auf die [**cpl- \_ Init**](cpl-init.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-120">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="ce2ae-121">Die [**cpl- \_ Netzteil**](cpl-newinquire.md) Meldung gibt Informationen in einem Format zurück, das vom System nicht zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-121">The [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="ce2ae-122">Aus diesem Grund sollten die meisten [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktionen **cpl- \_ Anfragen** verarbeiten und **cpl- \_ newinquire** ignorieren.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-122">For this reason, most [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) functions should process **CPL\_INQUIRE** and ignore **CPL\_NEWINQUIRE**.</span></span>

<span data-ttu-id="ce2ae-123">Die einzigen Anwendungen, die [**cpl- \_ Netzteil**](cpl-newinquire.md) verwenden sollten, sind diejenigen, die Ihr Symbol ändern oder Zeichen folgen auf der Grundlage des Status des Computers anzeigen müssen.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-123">The only applications that should use [**CPL\_NEWINQUIRE**](cpl-newinquire.md) are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="ce2ae-124">In diesem Fall sollte der **cpl \_** - \_ erstellungshandler den dynamischen cpl- \_ Res-Wert für die Member " **idion**", " **IDName**" oder " **idinfo** " der [**cplinfo**](/windows/win32/api/cpl/ns-cpl-cplinfo) -Struktur angeben, anstatt einen gültigen Ressourcen Bezeichner anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-124">In this case, your **CPL\_INQUIRE** handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="ce2ae-125">Dies bewirkt, dass in der Systemsteuerung jedes Mal, wenn das Symbol und die Anzeige Zeichenfolgen benötigt werden, die **cpl- \_ Netzteil** Zeichenfolge gesendet wird, sodass Sie basierend auf dem aktuellen Status des Computers Informationen angeben können.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-125">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="ce2ae-126">Dies ist deutlich langsamer als die Verwendung von zwischengespeicherten Informationen.</span><span class="sxs-lookup"><span data-stu-id="ce2ae-126">This is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce2ae-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ce2ae-127">Requirements</span></span>



| <span data-ttu-id="ce2ae-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce2ae-128">Requirement</span></span> | <span data-ttu-id="ce2ae-129">Wert</span><span class="sxs-lookup"><span data-stu-id="ce2ae-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ce2ae-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce2ae-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ce2ae-131">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce2ae-131">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ce2ae-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce2ae-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ce2ae-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce2ae-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ce2ae-134">Header</span><span class="sxs-lookup"><span data-stu-id="ce2ae-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce2ae-135"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce2ae-135"><dt>Cpl.h</dt></span></span> </dl> |



 

 
