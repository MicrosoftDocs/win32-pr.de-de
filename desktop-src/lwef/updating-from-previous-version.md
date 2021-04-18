---
title: Aktualisieren aus vorheriger Version
description: Aktualisieren aus vorheriger Version
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e2cf49fbe21c2522226ec61ab57c93d9df27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341636"
---
# <a name="updating-from-previous-version"></a><span data-ttu-id="644d6-103">Aktualisieren aus vorheriger Version</span><span class="sxs-lookup"><span data-stu-id="644d6-103">Updating from Previous Version</span></span>

<span data-ttu-id="644d6-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="644d6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="644d6-105">Anwendungen, die mit der vorherigen Version 1,5 des Microsoft-Agents erstellt und kompiliert wurden, sollten unverändert unter der neuen 2,0-Version ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="644d6-105">Applications built and compiled with the previous 1.5 version of Microsoft Agent should run without modification under the new 2.0 version.</span></span> <span data-ttu-id="644d6-106">Die [**verbundene**](connected-property.md) Eigenschaft kann nicht mehr auf **false** festgelegt werden. bestimmte Eigenschaften des bereits ersetzten speechinput-Objekts sind immer noch vorhanden, aber keine Werte mehr, und der Server löst nicht mehr die [**Neustart**](https://www.bing.com/search?q=**Restart**) -und [**Shutdown**](https://www.bing.com/search?q=**Shutdown**) -Ereignisse aus.</span><span class="sxs-lookup"><span data-stu-id="644d6-106">The [**Connected**](connected-property.md) property can no longer be set to **False**; certain properties of the SpeechInput object that have been replaced still exist, but no longer turn any values, and the server no longer fires the [**Restart**](https://www.bing.com/search?q=**Restart**) and [**Shutdown**](https://www.bing.com/search?q=**Shutdown**) events.</span></span>

<span data-ttu-id="644d6-107">Wenn Sie Ihre Anwendungen jedoch für die Verwendung des Agent 2,0-Steuer Elements aktualisieren, müssen Sie möglicherweise den Code ändern.</span><span class="sxs-lookup"><span data-stu-id="644d6-107">However, if you update your applications to use the Agent 2.0 control, you may have to modify your code.</span></span> <span data-ttu-id="644d6-108">Wenn Sie die 2,0-Version des Microsoft-Agents installiert haben und ein Visual Basic-Projekt laden, verwenden Sie die frühere Version des-Agent-Steuer Elements. Visual Basic enthält eine Option, die automatisch eine Meldung anzeigt, die anzeigt, dass eine neue Version des-Steuer Elements erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="644d6-108">If you have installed the 2.0 version of Microsoft Agent and load a Visual Basic project use the earlier version of the Agent control, Visual Basic includes an option that will automatically display a message indicating that it detected a new version of the control.</span></span> <span data-ttu-id="644d6-109">Um den ordnungsgemäßen Betrieb Ihrer Anwendung sicherzustellen, sollten Sie immer die spätere Version verwenden.</span><span class="sxs-lookup"><span data-stu-id="644d6-109">To ensure proper operation of your application, always choose to use the later version.</span></span>

<span data-ttu-id="644d6-110">Für andere Programmiersprachen (z. b. Microsoft Office 97 VBA) müssen Sie, um das Steuerelement zu aktualisieren, möglicherweise zuerst das Steuerelement 1,5-Agent entfernen und den Code speichern.</span><span class="sxs-lookup"><span data-stu-id="644d6-110">For other programming languages (such as Microsoft Office 97 VBA), to update the control, you may have to first remove the 1.5 Agent control and save your code.</span></span> <span data-ttu-id="644d6-111">Beenden Sie dann die Programmierumgebung, starten Sie die Programmierumgebung neu, laden Sie den Code neu, und fügen Sie das neue Steuerelement ein.</span><span class="sxs-lookup"><span data-stu-id="644d6-111">Then, quit the programming environment, restart the programming environment, reload your code and insert the new control.</span></span> <span data-ttu-id="644d6-112">Vermeiden Sie die Bearbeitung einer Anwendung mit Agent 2,0-Aktivierung in derselben Instanz der Programmierumgebung, in der Sie eine mit Agents 1,5 aktivierte Anwendung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="644d6-112">Avoid editing an Agent 2.0-enabled application in the same instance of the programming environment that you are editing an Agent 1.5-enabled application in.</span></span> <span data-ttu-id="644d6-113">In einigen Programmierumgebungen werden die Unterschiede zwischen den beiden Versionen von Steuerelementen möglicherweise nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="644d6-113">Some programming environments may not handle the differences between the two versions of controls.</span></span>

<span data-ttu-id="644d6-114">Sie sollten in der Lage sein, die-Agent-Version 1,5 auf Ihrem System zu deinstallieren, nachdem Sie die-2,0 Agent-Version von</span><span class="sxs-lookup"><span data-stu-id="644d6-114">You should be able to uninstall the Agent 1.5 release on your system after installing the Agent 2.0 release.</span></span> <span data-ttu-id="644d6-115">Wenn jedoch der Agent 1,5 über die 2,0-Version installiert ist, müssen Sie möglicherweise 2,0 neu installieren.</span><span class="sxs-lookup"><span data-stu-id="644d6-115">However, if Agent 1.5 is installed over the 2.0 release, you may have to reinstall 2.0.</span></span>

 

 




