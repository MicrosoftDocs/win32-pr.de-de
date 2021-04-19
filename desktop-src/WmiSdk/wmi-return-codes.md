---
description: Dieser Abschnitt enthält eine Liste der WMI-Rückgabecodes, symbolischen Konstanten, Literalwerte und Beschreibungen. Diese Codes können von Skripts, C++-Anwendungen oder WMIC-Befehlen zurückgegeben werden.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: WMI-Rückgabe Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e05455b109bd05b7a1693b8a05b13f6f7aeb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348878"
---
# <a name="wmi-return-codes"></a><span data-ttu-id="f2416-104">WMI-Rückgabe Codes</span><span class="sxs-lookup"><span data-stu-id="f2416-104">WMI Return Codes</span></span>

<span data-ttu-id="f2416-105">Dieser Abschnitt enthält eine Liste der WMI-Rückgabecodes, symbolischen Konstanten, Literalwerte und Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="f2416-105">This section provides a list of the WMI return codes, symbolic constants, literal values, and descriptions.</span></span> <span data-ttu-id="f2416-106">Diese Codes können von Skripts, C++-Anwendungen oder [**WMIC**](wmic.md) -Befehlen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f2416-106">These codes may be returned by scripts, C++ applications, or [**Wmic**](wmic.md) commands.</span></span>

<span data-ttu-id="f2416-107">Wenn ein Fehler auftritt, gibt WMI einen der folgenden Fehlercodes als 32-Bit-Wert zurück, wobei die zwei höherwertigen Bits den Schweregrad Code der Nachricht angeben.</span><span class="sxs-lookup"><span data-stu-id="f2416-107">If an error occurs, WMI returns one of the following error codes as a 32-bit value where the two high-order bits indicate the severity code of the message.</span></span>

<dl> <dt>

<span data-ttu-id="f2416-108"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="f2416-108"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="f2416-109">Erfolg</span><span class="sxs-lookup"><span data-stu-id="f2416-109">Success</span></span>

</dd> <dt>

<span data-ttu-id="f2416-110"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="f2416-110"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="f2416-111">Informational</span><span class="sxs-lookup"><span data-stu-id="f2416-111">Informational</span></span>

</dd> <dt>

<span data-ttu-id="f2416-112"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="f2416-112"><span id="2"></span>2</span></span>
</dt> <dd>

<span data-ttu-id="f2416-113">Warnung</span><span class="sxs-lookup"><span data-stu-id="f2416-113">Warning</span></span>

</dd> <dt>

<span data-ttu-id="f2416-114"><span id="3"></span>€</span><span class="sxs-lookup"><span data-stu-id="f2416-114"><span id="3"></span>3</span></span>
</dt> <dd>

<span data-ttu-id="f2416-115">Fehler</span><span class="sxs-lookup"><span data-stu-id="f2416-115">Error</span></span>

</dd> </dl>

> [!Note]
>
> <span data-ttu-id="f2416-116">Wenn WMI Fehlermeldungen zurückgibt, beachten Sie, dass Sie möglicherweise nicht auf Probleme im WMI-Dienst oder in WMI-Anbietern hinweisen.</span><span class="sxs-lookup"><span data-stu-id="f2416-116">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="f2416-117">Fehler können aus anderen Teilen des Betriebssystems stammen und als Fehler über WMI auftreten.</span><span class="sxs-lookup"><span data-stu-id="f2416-117">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="f2416-118">Löschen Sie das WMI-Repository unter Umständen nicht als erste Aktion, da das Löschen des Repository zu Beschädigungen des Systems oder der installierten Anwendungen führen kann.</span><span class="sxs-lookup"><span data-stu-id="f2416-118">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="f2416-119">Um weitere Informationen zur Ursache des Problems zu erhalten, können Sie das Befehlszeilen Tool [WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) Diagnose herunterladen und ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2416-119">To obtain more information about the source of the problem, you can download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="f2416-120">Mit diesem Tool wird ein Bericht erstellt, der in der Regel die Ursache des Problems isolieren und Anweisungen zur Behebung des Problems bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f2416-120">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="f2416-121">Der Bericht hilft Ihnen auch bei der Unterstützung durch den Microsoft-Support.</span><span class="sxs-lookup"><span data-stu-id="f2416-121">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="f2416-122">Sie können die WMI-Diagnosehilfsprogramm [hier](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="f2416-122">You can download the WMI Diagnosis Utility [here](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

-   [<span data-ttu-id="f2416-123">**WMI-Fehler Konstanten**</span><span class="sxs-lookup"><span data-stu-id="f2416-123">**WMI Error Constants**</span></span>](wmi-error-constants.md)
-   [<span data-ttu-id="f2416-124">**WMI-nicht-Fehler-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="f2416-124">**WMI Non-Error Constants**</span></span>](wmi-non-error-constants.md)

 

 



