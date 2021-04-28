---
description: DEP/NX-Schutz
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: DEP/NX-Schutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3565460cbfd2e6b13c3c5ba6b1f0693a3d5b25ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088568"
---
# <a name="depnx-protection"></a><span data-ttu-id="4e815-103">DEP/NX-Schutz</span><span class="sxs-lookup"><span data-stu-id="4e815-103">DEP/NX Protection</span></span>

<span data-ttu-id="4e815-104">Ab Windows Internet Explorer 7 unter Windows Vista enthält das  Element der Internetsteuerung die Option Speicherschutz aktivieren, um Onlineangriffe zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="4e815-104">Starting with Windows Internet Explorer 7 on Windows Vista, the Internet control panel item includes an **Enable memory protection** option to help mitigate online attacks.</span></span> <span data-ttu-id="4e815-105">Diese Option wird auch als Datenausführungsverhindung (Data *Execution Prevention,* DEP) oder *No-Execute* (NX) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4e815-105">This option is also referred to as *Data Execution Prevention* (DEP) or *No-Execute* (NX).</span></span> <span data-ttu-id="4e815-106">Wenn diese Option aktiviert ist, arbeitet sie mit dem Prozessor zusammen, um Pufferüberlaufangriffe zu verhindern, indem die Codeausführung im Arbeitsspeicher blockiert wird, der als nicht ausführbare Datei gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="4e815-106">When this option is enabled, it works with the processor to help prevent buffer overflow attacks by blocking code execution from memory that is marked as non-executable.</span></span>

<span data-ttu-id="4e815-107">In Windows Internet Explorer 8 unter Windows Vista mit Service Pack 1 -Betriebssystem (SP1) oder einer neueren Version ist diese Option standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4e815-107">In Windows Internet Explorer 8 on the Windows Vista with Service Pack 1 (SP1) operating system or a later version, this option is enabled by default.</span></span> <span data-ttu-id="4e815-108">DEP/NX schützt nicht vor allen speicherbasierten Sicherheitsrisiken.</span><span class="sxs-lookup"><span data-stu-id="4e815-108">DEP/NX does not protect against all memory-based vulnerabilities.</span></span> <span data-ttu-id="4e815-109">Wenn sie jedoch mit anderen Technologien wie der zufälligen Anordnung des Adressraumlayouts (Address Space Layout Randomization, ASLR) kombiniert wird, trägt sie dazu bei, häufige Pufferüberlauf-Sicherheitsrisiken in Windows Internet Explorer und den add-ons zu verhindern, die geladen werden.</span><span class="sxs-lookup"><span data-stu-id="4e815-109">But when it is combined with other technologies like Address Space Layout Randomization (ASLR), it helps prevent common buffer overflow vulnerabilities in Windows Internet Explorer and the add-ons that it loads.</span></span> <span data-ttu-id="4e815-110">Für diesen Schutz ist keine zusätzliche Benutzerinteraktion erforderlich, und es werden keine neuen Eingabeaufforderungen eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4e815-110">No additional user interaction is required to provide this protection, and no new prompts are introduced.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e815-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4e815-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e815-112">Beheben von Kompatibilitätsproblemen in Webanwendungen mit Kompatibilitätsansicht</span><span class="sxs-lookup"><span data-stu-id="4e815-112">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



