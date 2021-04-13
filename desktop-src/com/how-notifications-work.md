---
title: Funktionsweise von Benachrichtigungen
description: Funktionsweise von Benachrichtigungen
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9665b327d164a4e105f8adba3328be284fbe1fa0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391080"
---
# <a name="how-notifications-work"></a><span data-ttu-id="c9883-103">Funktionsweise von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="c9883-103">How Notifications Work</span></span>

<span data-ttu-id="c9883-104">Benachrichtigungen stammen aus der Objekt Anwendung und fließen mithilfe des Objekt Handlers zum Container.</span><span class="sxs-lookup"><span data-stu-id="c9883-104">Notifications originate in the object application and flow to the container by way of the object handler.</span></span> <span data-ttu-id="c9883-105">Wenn das Objekt ein verknüpftes Objekt ist, fängt das verknüpfte Objekt die Benachrichtigungen vom Objekt Handler ab und benachrichtigt den Container direkt.</span><span class="sxs-lookup"><span data-stu-id="c9883-105">If the object is a linked object, the linked object intercepts the notifications from the object handler and notifies the container directly.</span></span>

<span data-ttu-id="c9883-106">Eine Objekt Anwendung muss Registrierungsanforderungen verwalten und nachverfolgen, wohin welche Benachrichtigungen gesendet und welche Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c9883-106">An object application must manage registration requests, keeping track of where to send which notifications and sending those notifications when appropriate.</span></span> <span data-ttu-id="c9883-107">OLE stellt zwei Komponenten Objekte zur Vereinfachung dieser Aufgabe bereit: oleadviseholder für Verbund Dokument Benachrichtigungen und dataadviseholder für Daten Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="c9883-107">OLE provides two component objects to simplify this task: the OleAdviseHolder for compound document notifications and the DataAdviseHolder for data notifications.</span></span>

<span data-ttu-id="c9883-108">Objekt Anwendungen bestimmen die Bedingungen, die das Senden der einzelnen Benachrichtigungen auffordern, sowie die Häufigkeit, mit der jede Benachrichtigung gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9883-108">Object applications determine the conditions that prompt the sending of each specific notification and the frequency with which each notification should be sent.</span></span> <span data-ttu-id="c9883-109">Wenn es sinnvoll ist, mehrere Benachrichtigungen zu senden, spielt es keine Rolle, welche Benachrichtigung zuerst gesendet wird. Sie können in beliebiger Reihenfolge gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9883-109">When it is appropriate for multiple notifications to be sent, it does not matter which notification is sent first; they can be sent in any order.</span></span>

<span data-ttu-id="c9883-110">Die zeitliche Steuerung von Benachrichtigungen wirkt sich auf die Leistung und Koordination zwischen einer Objekt Anwendung und ihren Containern aus.</span><span class="sxs-lookup"><span data-stu-id="c9883-110">The timing of notifications affects the performance and coordination between an object application and its containers.</span></span> <span data-ttu-id="c9883-111">Benachrichtigungen, die zu häufig zu langsam verarbeitet werden, führen zu einem nicht synchron gesendeten Benachrichtigungs Container.</span><span class="sxs-lookup"><span data-stu-id="c9883-111">Whereas notifications sent too frequently slow processing, notifications sent too infrequently result in an out-of-sync container.</span></span> <span data-ttu-id="c9883-112">Die Benachrichtigungs Häufigkeit kann mit der Rate verglichen werden, mit der eine Anwendung neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="c9883-112">Notification frequency can be compared with the rate at which an application repaints.</span></span> <span data-ttu-id="c9883-113">Daher ist die Verwendung einer ähnlichen Logik für die zeitliche Steuerung von Benachrichtigungen (wie zum Neuzeichnen verwendet) ratsam.</span><span class="sxs-lookup"><span data-stu-id="c9883-113">Therefore, using similar logic for the timing of notifications (as is used for repainting) is wise.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9883-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9883-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9883-115">**"Kreatedataadvierholder"**</span><span class="sxs-lookup"><span data-stu-id="c9883-115">**CreateDataAdviseHolder**</span></span>](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[<span data-ttu-id="c9883-116">**"Kreateoleadvicholder"**</span><span class="sxs-lookup"><span data-stu-id="c9883-116">**CreateOleAdviseHolder**</span></span>](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[<span data-ttu-id="c9883-117">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="c9883-117">Notifications</span></span>](notifications.md)
</dt> </dl>

 

 