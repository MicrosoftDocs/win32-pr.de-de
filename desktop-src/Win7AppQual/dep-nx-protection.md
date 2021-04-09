---
description: .
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: DEP/NX-Schutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c4a4cedead32504b6b78ba34bb72ee6b2ef400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868755"
---
# <a name="depnx-protection"></a><span data-ttu-id="b9483-103">DEP/NX-Schutz</span><span class="sxs-lookup"><span data-stu-id="b9483-103">DEP/NX Protection</span></span>

<span data-ttu-id="b9483-104">Ab Windows Internet Explorer 7 unter Windows Vista enthält das Element "Internet-Systemsteuerung" die Option " **Speicherschutz aktivieren** ", um Online Angriffe zu verringern.</span><span class="sxs-lookup"><span data-stu-id="b9483-104">Starting with Windows Internet Explorer 7 on Windows Vista, the Internet control panel item includes an **Enable memory protection** option to help mitigate online attacks.</span></span> <span data-ttu-id="b9483-105">Diese Option wird auch als *Daten Ausführungs Verhinderung (Data Execution Prevention* , DEP) oder *No-Execute* (NX) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b9483-105">This option is also referred to as *Data Execution Prevention* (DEP) or *No-Execute* (NX).</span></span> <span data-ttu-id="b9483-106">Wenn diese Option aktiviert ist, funktioniert Sie mit dem Prozessor, um Pufferüberlauf Angriffe durch Blockieren der Codeausführung aus dem Arbeitsspeicher zu verhindern, der als nicht ausführbare Datei markiert ist.</span><span class="sxs-lookup"><span data-stu-id="b9483-106">When this option is enabled, it works with the processor to help prevent buffer overflow attacks by blocking code execution from memory that is marked as non-executable.</span></span>

<span data-ttu-id="b9483-107">In Windows Internet Explorer 8 unter dem Betriebssystem Windows Vista mit Service Pack 1 (SP1) oder einer höheren Version ist diese Option standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b9483-107">In Windows Internet Explorer 8 on the Windows Vista with Service Pack 1 (SP1) operating system or a later version, this option is enabled by default.</span></span> <span data-ttu-id="b9483-108">DEP/NX schützt nicht vor allen Speicher basierten Sicherheitsrisiken.</span><span class="sxs-lookup"><span data-stu-id="b9483-108">DEP/NX does not protect against all memory-based vulnerabilities.</span></span> <span data-ttu-id="b9483-109">Wenn Sie jedoch mit anderen Technologien wie Address Space Layout Randomization (ASLR) kombiniert werden, hilft Sie dabei, häufige Sicherheitsrisiken für Pufferüberlauf in Windows Internet Explorer und die von ihr Auslastungen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="b9483-109">But when it is combined with other technologies like Address Space Layout Randomization (ASLR), it helps prevent common buffer overflow vulnerabilities in Windows Internet Explorer and the add-ons that it loads.</span></span> <span data-ttu-id="b9483-110">Es ist keine zusätzliche Benutzerinteraktion erforderlich, um diesen Schutz zu gewährleisten, und es werden keine neuen Eingabe Aufforderungen eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b9483-110">No additional user interaction is required to provide this protection, and no new prompts are introduced.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9483-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b9483-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9483-112">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht</span><span class="sxs-lookup"><span data-stu-id="b9483-112">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



