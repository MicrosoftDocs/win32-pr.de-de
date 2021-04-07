---
title: Joystick Benachrichtigungen
description: Joystick Benachrichtigungen
ms.assetid: 523dfae3-bbd5-4955-96f3-1710e29d003f
keywords:
- Joysticks, Benachrichtigungen
- Joysticks, Meldungen
- erfasste Joystick
- entkoppelt-Joystick
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2791f8da14107d50afe90d8efbdbfe79acba3093
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038950"
---
# <a name="joystick-notifications"></a><span data-ttu-id="17eee-107">Joystick Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="17eee-107">Joystick Notifications</span></span>

<span data-ttu-id="17eee-108">Mithilfe der [**joysetcapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) -Funktion können Sie direkte Joystick Nachrichten erfassen, die an eine Funktion gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="17eee-108">You can capture direct joystick messages to be sent to a function by using the [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) function.</span></span> <span data-ttu-id="17eee-109">Nur eine Anwendung kann Nachrichten von einem Joystick erfassen, aber Sie können den Joystick mithilfe der [**joygetpos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) -Funktion oder der [**joygetposex**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) -Funktion von einer anderen Anwendung Abfragen.</span><span class="sxs-lookup"><span data-stu-id="17eee-109">Only one application at a time can capture messages from a joystick, but you can query the joystick from another application by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) or [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) function.</span></span>

> [!Note]  
> <span data-ttu-id="17eee-110">Eine Joystick Nachricht kann die Anwendung, die den Joystick aufgezeichnet hat, nicht erreichen, wenn eine zweite Anwendung **joygetpos** oder **joygetposex** verwendet, um den Joystick ungefähr zur gleichen Zeit abzufragen, in der die Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="17eee-110">A joystick message can fail to reach the application that captured the joystick if a second application uses **joyGetPos** or **joyGetPosEx** to query the joystick at approximately the same time that the message is sent.</span></span> <span data-ttu-id="17eee-111">In diesem Fall könnte die zweite Anwendung die Nachricht abfangen.</span><span class="sxs-lookup"><span data-stu-id="17eee-111">In this case, the second application could intercept the message.</span></span>

 

<span data-ttu-id="17eee-112">Wenn Sie Nachrichten von zwei an das System angefügten Joystick erfassen möchten, verwenden Sie für jeden Joystick zweimal [**joysetcapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) .</span><span class="sxs-lookup"><span data-stu-id="17eee-112">If you want to capture messages from two joysticks attached to the system, use [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) twice, once for each joystick.</span></span> <span data-ttu-id="17eee-113">Ihr Fenster empfängt separate und unterschiedliche Meldungen für jedes Gerät.</span><span class="sxs-lookup"><span data-stu-id="17eee-113">Your window receives separate and distinct messages for each device.</span></span>

<span data-ttu-id="17eee-114">Sie können einen aufgezeichneten Joystick mithilfe der [**joyreleasecapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="17eee-114">You can release a captured joystick by using the [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) function.</span></span> <span data-ttu-id="17eee-115">Wenn eine Anwendung den Joystick vor dem Beenden nicht freigibt, wird der Joystick automatisch kurz nach dem Zerstören des Erfassungs Fensters freigegeben.</span><span class="sxs-lookup"><span data-stu-id="17eee-115">If an application does not release the joystick before ending, the joystick is automatically released shortly after the capture window is destroyed.</span></span>

<span data-ttu-id="17eee-116">Ein nicht ausgezeichteter Joystick kann nicht erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="17eee-116">You cannot capture an unplugged joystick.</span></span> <span data-ttu-id="17eee-117">Die Funktion " **joysetcapture** " gibt "joyerr" zurück, \_ Wenn das angegebene Gerät nicht getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="17eee-117">The **joySetCapture** function returns JOYERR\_UNPLUGGED if the specified device is unplugged.</span></span>

 

 