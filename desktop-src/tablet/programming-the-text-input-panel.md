---
description: Ab Windows Vista ersetzt TextInputPanel den "tabinputpanel", um die Bildschirmdarstellung und das Verhalten des Tablet-Eingabe Bereichs zu steuern. in den folgenden Abschnitten wird beschrieben, wie Sie den Eingabebereich mithilfe der Anwendungs Programmierschnittstellen für den Text Eingabebereich programmieren. TextInputPanel für Benutzer von "tzinputpanelusing" im Eingabebereich "Automatische vervollstänteaktivierung" Textkorrektur für benutzerdefinierte frei Hand Collector. der Texteingabebereich wird in eine ausführbare Datei mit dem Namen "TabTip.exe" implementiert. Wenn Sie TabTip.exe mit dem/SeekDesktop-Parameter ausführen, wird versucht, eine reduzierte Funktionalitäts Version des Eingabe Panels auf einem nicht dem Standard interaktiven Desktop auszuführen Bei den meisten erstellten Desktops wird der Eingabebereich automatisch in diesem Modus ausgeführt. Dieser Parameter bietet die Möglichkeit, Sie in ungewöhnlichen Anwendungsszenarien zu starten, die andernfalls den automatischen Start verhindern. Wenn der Eingabebereich bereits auf dem Desktop ausgeführt wird, hat dieser Parameter keine Auswirkungen, und die Instanz von TabTip.exe wird sofort beendet.
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: Programmieren des Text Eingabe Panels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e6b379a26199e602fc68402d77fa89fb4f8fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351110"
---
# <a name="programming-the-text-input-panel"></a><span data-ttu-id="95c3a-107">Programmieren des Text Eingabe Panels</span><span class="sxs-lookup"><span data-stu-id="95c3a-107">Programming the Text Input Panel</span></span>

<span data-ttu-id="95c3a-108">Ab Windows Vista ersetzt [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) das [**tabinputpanel**](peninputpanel-class.md) zum Steuern der Bildschirmdarstellung und des Verhaltens des Tablet-Eingabe Bereichs.</span><span class="sxs-lookup"><span data-stu-id="95c3a-108">Starting with Windows Vista, the [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) supersedes the [**PenInputPanel**](peninputpanel-class.md) for controlling the onscreen appearance and behavior of the Tablet Input Panel.</span></span>

<span data-ttu-id="95c3a-109">In den folgenden Abschnitten wird beschrieben, wie Sie den Eingabebereich mit dem Text Eingabe Panel-Anwendungs Programmierschnittstellen programmieren.</span><span class="sxs-lookup"><span data-stu-id="95c3a-109">The following sections describe programming the Input Panel using the Text Input Panel application programming interfaces.</span></span>

-   [<span data-ttu-id="95c3a-110">TextInputPanel für Benutzer von "" in "".</span><span class="sxs-lookup"><span data-stu-id="95c3a-110">TextInputPanel for Users of PenInputPanel</span></span>](textinputpanel-for-users-of-peninputpanel.md)
-   [<span data-ttu-id="95c3a-111">Verwenden des Auto Vervollständigen-Eingabe Bereichs</span><span class="sxs-lookup"><span data-stu-id="95c3a-111">Using Input Panel AutoComplete</span></span>](using-input-panel-autocomplete.md)
-   [<span data-ttu-id="95c3a-112">Aktivieren der Text Korrektur für benutzerdefinierte frei Hand Sammler</span><span class="sxs-lookup"><span data-stu-id="95c3a-112">Enabling Text Correction for Custom Ink Collectors</span></span>](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> <span data-ttu-id="95c3a-113">Der Text Eingabebereich wird in eine ausführbare Datei mit dem Namen TabTip.exe implementiert.</span><span class="sxs-lookup"><span data-stu-id="95c3a-113">The Text Input Panel is implemented in an executable file called TabTip.exe.</span></span> <span data-ttu-id="95c3a-114">Wenn Sie TabTip.exe mit dem */SeekDesktop* -Parameter ausführen, wird versucht, eine reduzierte Funktionalitäts Version des Eingabe Panels auf einem [**nicht dem Standard**](/windows/win32/api/winuser/nf-winuser-createdesktopa)interaktiven Desktop auszuführen</span><span class="sxs-lookup"><span data-stu-id="95c3a-114">Running TabTip.exe with the */SeekDesktop* parameter attempts to run a reduced functionality version of Input Panel on a nonstandard interactive desktop, as created with [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span></span> <span data-ttu-id="95c3a-115">Bei den meisten erstellten Desktops wird der Eingabebereich automatisch in diesem Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95c3a-115">For most created desktops, Input Panel will automatically run in this mode already.</span></span> <span data-ttu-id="95c3a-116">Dieser Parameter bietet die Möglichkeit, Sie in ungewöhnlichen Anwendungsszenarien zu starten, die andernfalls den automatischen Start verhindern.</span><span class="sxs-lookup"><span data-stu-id="95c3a-116">This parameter provides the means for launching it in unusual application scenarios that otherwise prevent the automatic launch.</span></span> <span data-ttu-id="95c3a-117">Wenn der Eingabebereich bereits auf dem Desktop ausgeführt wird, hat dieser Parameter keine Auswirkungen, und die Instanz von TabTip.exe wird sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="95c3a-117">If Input Panel is already running on the desktop, this parameter will have no effect and the instance of TabTip.exe will exit immediately.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="95c3a-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95c3a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95c3a-119">Programmieren des Eingabe Bereichs mithilfe der Klasse "pinputpanel"</span><span class="sxs-lookup"><span data-stu-id="95c3a-119">Programming the Input Panel Using the PenInputPanel Class</span></span>](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
