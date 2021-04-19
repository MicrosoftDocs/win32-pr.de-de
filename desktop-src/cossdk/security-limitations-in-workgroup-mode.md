---
description: Sicherheitseinschränkungen im Arbeitsgruppen Modus
ms.assetid: 05c0aba7-b94b-49d4-a0fc-1ff0a23550b3
title: Sicherheitseinschränkungen im Arbeitsgruppen Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eabe38b8d05c49382ae6dd8337b883a6f4a8079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345433"
---
# <a name="security-limitations-in-workgroup-mode"></a><span data-ttu-id="eda15-103">Sicherheitseinschränkungen im Arbeitsgruppen Modus</span><span class="sxs-lookup"><span data-stu-id="eda15-103">Security Limitations in Workgroup Mode</span></span>

<span data-ttu-id="eda15-104">Die Konfiguration der [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) Arbeitsgruppe lässt nicht zu, dass der com+-Dienst in der Warteschlange die Anwendungssicherheit unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eda15-104">The [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) workgroup configuration does not permit the COM+ queued components service to support application security.</span></span> <span data-ttu-id="eda15-105">Wenn Sie Message Queuing mit der Arbeitsgruppen Konfiguration installiert haben, müssen Sie die [Sicherheit](specifying-the-authentication-protocol.md) für jede Anwendung in der Warteschlange, auf die in dieser Konfiguration zugegriffen wird, deaktivieren, indem Sie im Dialogfeld " **Eigenschaften** " der com+-Anwendung auf **der Registerkarte** "Queue" die Option **keine Meldungen authentifizieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="eda15-105">If you've installed Message Queuing with the workgroup configuration, you must [disable security](specifying-the-authentication-protocol.md) on each queued application accessed in this configuration by selecting **Do not authenticate messages** on the **Queuing** tab for the COM+ application's **Properties** dialog, using the Component Services administrative tool.</span></span> <span data-ttu-id="eda15-106">Dies sollte nur in einem vertrauenswürdigen Netzwerk erfolgen und muss sowohl auf dem Client als auch auf dem Server ausgeführt werden, wenn die Anwendung bereits exportiert wurde.</span><span class="sxs-lookup"><span data-stu-id="eda15-106">This should be done only on a trusted network and must be done at both client and server if the application has already been exported.</span></span>

 

 



