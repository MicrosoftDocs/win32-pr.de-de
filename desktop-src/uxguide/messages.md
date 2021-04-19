---
title: Nachrichten (Entwurfs Grundlagen)
description: Bei den Nachrichten handelt es sich um eine beliebige Art von Nachrichten, die Benutzer bei der Verwendung Ihrer APP benötigen. Erfahren Sie, wie Sie Fehler, Warnungen, Bestätigungen und Benachrichtigungen in Ihrer APP präsentieren.
ms.assetid: 700F1F1F-B41D-4C0A-B2EC-91C84E46E526
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dba3296c9824b2153184c45b6a021ea823b4d151
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106366537"
---
# <a name="messages-design-basics"></a><span data-ttu-id="468f7-104">Nachrichten (Entwurfs Grundlagen)</span><span class="sxs-lookup"><span data-stu-id="468f7-104">Messages (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="468f7-105">Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="468f7-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="468f7-106">Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="468f7-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="468f7-107">Bei den Nachrichten handelt es sich um eine beliebige Art von Nachrichten, die Benutzer bei der Verwendung Ihrer APP benötigen.</span><span class="sxs-lookup"><span data-stu-id="468f7-107">Messages are any kind of message users need or want to see as they use your app.</span></span> <span data-ttu-id="468f7-108">Erfahren Sie, wie Sie Fehler, Warnungen, Bestätigungen und Benachrichtigungen in Ihrer APP präsentieren.</span><span class="sxs-lookup"><span data-stu-id="468f7-108">Learn how to present errors, warning, confirmations, and notifications in your app.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="468f7-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="468f7-109">In this section</span></span>



| <span data-ttu-id="468f7-110">Thema</span><span class="sxs-lookup"><span data-stu-id="468f7-110">Topic</span></span>                                        | <span data-ttu-id="468f7-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="468f7-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="468f7-112">Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="468f7-112">Error Messages</span></span>](mess-error.md)<br/>  | <span data-ttu-id="468f7-113">Eine Fehlermeldung warnt Benutzer über ein bereits aufgetretene Problem.</span><span class="sxs-lookup"><span data-stu-id="468f7-113">An error message alerts users of a problem that has already occurred.</span></span> <span data-ttu-id="468f7-114">Im Gegensatz dazu warnt eine Warnmeldung Benutzer über eine Bedingung, die in der Zukunft ein Problem verursachen könnte.</span><span class="sxs-lookup"><span data-stu-id="468f7-114">By contrast, a warning message alerts users of a condition that might cause a problem in the future.</span></span> <span data-ttu-id="468f7-115">Fehlermeldungen können mithilfe von modalen Dialogfeldern, direkten Nachrichten, Benachrichtigungen oder Luftballons angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="468f7-115">Error messages can be presented using modal dialog boxes, in-place messages, notifications, or balloons.</span></span><br/>                                                  |
| [<span data-ttu-id="468f7-116">Warnmeldungen</span><span class="sxs-lookup"><span data-stu-id="468f7-116">Warning Messages</span></span>](mess-warn.md)<br/> | <span data-ttu-id="468f7-117">Eine Warnmeldung ist ein modales Dialogfeld, eine direkte Nachricht, eine Benachrichtigung oder eine Sprechblase, die den Benutzer über eine Bedingung benachrichtigt, die möglicherweise in der Zukunft ein Problem verursacht.</span><span class="sxs-lookup"><span data-stu-id="468f7-117">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="468f7-118">Bestätigungen</span><span class="sxs-lookup"><span data-stu-id="468f7-118">Confirmations</span></span>](mess-confirm.md)<br/> | <span data-ttu-id="468f7-119">Eine Bestätigung ist ein modales Dialogfeld, in dem Sie gefragt werden, ob der Benutzer eine Aktion fortsetzen möchte.</span><span class="sxs-lookup"><span data-stu-id="468f7-119">A confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span><br/>                                                                                                                                                                                                                                          |
| [<span data-ttu-id="468f7-120">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="468f7-120">Notifications</span></span>](mess-notif.md)<br/>   | <span data-ttu-id="468f7-121">Eine Benachrichtigung informiert Benutzer über Ereignisse, die nicht mit der aktuellen Benutzeraktivität in Zusammenhang stehen, indem eine Sprechblase von einem Symbol im Benachrichtigungsbereich kurz angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="468f7-121">A notification informs users of events that are unrelated to the current user activity, by briefly displaying a balloon from an icon in the notification area.</span></span> <span data-ttu-id="468f7-122">Die Benachrichtigung kann aus einer Benutzeraktion oder einem signifikanten System Ereignis resultieren oder potenziell nützliche Informationen von Microsoft Windows oder einer Anwendung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="468f7-122">The notification could result from a user action or significant system event, or could offer potentially useful information from Microsoft Windows or an application.</span></span><br/> |



 

 

