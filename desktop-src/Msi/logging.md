---
description: Diese pro-Computer-System Richtlinie wird nur verwendet, wenn die Protokollierung nicht durch die \# Befehlszeilenoption "&0034;/L&\# 0034;" oder durch "msienablelog" aktiviert wurde.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Protokollierung (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a461051022791e414fe7e211e4dde33c7e83101b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756613"
---
# <a name="logging-windows-installer"></a><span data-ttu-id="b6eba-103">Protokollierung (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="b6eba-103">Logging (Windows Installer)</span></span>

<span data-ttu-id="b6eba-104">Diese Computer spezifische [System Richtlinie](system-policy.md) wird nur verwendet, wenn die Protokollierung nicht durch die Befehlszeilenoption "/L" oder durch " [**msienablelog**](/windows/desktop/api/Msi/nf-msi-msienableloga)" aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="b6eba-104">This per-machine [system policy](system-policy.md) is used only if logging has not been enabled by the "/L" command line option or by [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga).</span></span> <span data-ttu-id="b6eba-105">Wenn die Richtlinie in diesem Fall festgelegt wird, erstellt das Installationsprogramm eine Protokolldatei in% Temp% mit dem zufälligen Namen MSI \* . Angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b6eba-105">If the policy is set in this case, the installer creates a log file in %temp% with the random name: MSI\*.LOG.</span></span> <span data-ttu-id="b6eba-106">Legen Sie den Protokollierungs Modus fest, indem Sie den Richtlinien Wert auf eine Zeichenfolge festlegen.</span><span class="sxs-lookup"><span data-stu-id="b6eba-106">Specify the logging mode by setting the policy value to a string of characters.</span></span> <span data-ttu-id="b6eba-107">Verwenden Sie die gleichen Zeichen, um die Protokollierungs Modus-Richtlinie anzugeben, die von der [Befehlszeilenoption](command-line-options.md)"/L" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b6eba-107">Use the same characters to specify logging mode policy as used by the "/L" [command line option](command-line-options.md).</span></span> <span data-ttu-id="b6eba-108">Beachten Sie, dass Sie nicht "+" und " \* " für die Richtlinie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b6eba-108">Note that you cannot use "+" and "\*" for the policy.</span></span>

<span data-ttu-id="b6eba-109">Der Protokollierungs Modus kann mithilfe von Richtlinie, einer Befehlszeilenoption oder Programm gesteuert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b6eba-109">The logging mode can be set using policy, a command line option, or programmatically.</span></span> <span data-ttu-id="b6eba-110">Weitere Informationen zu allen Methoden, die zum Festlegen des Protokollierungs Modus verfügbar sind, finden Sie unter [normale Protokollierung](normal-logging.md) im Abschnitt [Windows Installer Protokollierung](windows-installer-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="b6eba-110">For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.</span></span>

<span data-ttu-id="b6eba-111">Sie können verhindern, dass vertrauliche Informationen, z. b. Kenn Wörter, in die Protokolldatei eingegeben und sichtbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="b6eba-111">You can prevent confidential information, for example passwords, from being entered into the log file and made visible.</span></span> <span data-ttu-id="b6eba-112">Weitere Informationen finden Sie unter [verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden](preventing-confidential-information-from-being-written-into-the-log-file.md) .</span><span class="sxs-lookup"><span data-stu-id="b6eba-112">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)</span></span>

## <a name="registry-key"></a><span data-ttu-id="b6eba-113">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="b6eba-113">Registry Key</span></span>

<span data-ttu-id="b6eba-114">Legen Sie den Wert Logging unter dem folgenden Registrierungsschlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="b6eba-114">Set the value named Logging under the following registry key.</span></span>

<span data-ttu-id="b6eba-115">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="b6eba-115">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="b6eba-116">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b6eba-116">Data Type</span></span>

<span data-ttu-id="b6eba-117">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="b6eba-117">**REG\_SZ**</span></span>

 

 



