---
title: Allgemeine Initialisierungs Flags für Dialog Felder
description: Flags werden verwendet, um das Verhalten und die Darstellung eines allgemeinen Dialog Felds zu ändern.
ms.assetid: 072cdcab-00d1-4a09-97fb-a6de2d51392e
keywords:
- Allgemeine Dialog Feld Bibliothek, Initialisierung
- Allgemeine Dialogfelder, initialisieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c994e743178e3b6a17129275affed099d3004
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/19/2020
ms.locfileid: "104474730"
---
# <a name="common-dialog-box-initialization-flags"></a><span data-ttu-id="8f312-105">Allgemeine Initialisierungs Flags für Dialog Felder</span><span class="sxs-lookup"><span data-stu-id="8f312-105">Common Dialog Box Initialization Flags</span></span>

<span data-ttu-id="8f312-106">Flags werden verwendet, um das Verhalten und die Darstellung eines allgemeinen Dialog Felds zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8f312-106">Flags are used to modify the behavior and appearance of a common dialog box.</span></span> <span data-ttu-id="8f312-107">Initialisierungsflags sind die Werte, die Sie im **Flags** -Member der-Struktur festlegen, die zum Erstellen des Dialog Felds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f312-107">Initialization flags are the values that you set in the **Flags** member of the structure that is used to create the dialog box.</span></span> <span data-ttu-id="8f312-108">Mithilfe der Flags geben Sie an, welche Steuerelemente in einem Dialogfeld Anfangswerte empfangen, welche Steuerelemente deaktiviert werden und wie Sie den Wertebereich ändern können, den der Benutzer mit den Steuerelementen festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="8f312-108">You use the flags to specify which controls in a dialog box receive initial values, to disable selected controls, and to modify the range of values that the user can set with the controls.</span></span> <span data-ttu-id="8f312-109">Außerdem verwenden Sie die Flags, um Hook-Prozeduren und benutzerdefinierte Vorlagen für die Dialogfelder zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f312-109">You also use the flags to enable hook procedures and custom templates for the dialog boxes.</span></span>

<span data-ttu-id="8f312-110">Beispielsweise können Sie den Wert von **CF- \_ Effekten** im **Flags** -Member der [**choosefont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) -Struktur festlegen, um das Dialogfeld **Schriftart** anzuweisen, die Effekte-Steuerelemente anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8f312-110">For example, you can set the **CF\_EFFECTS** value in the **Flags** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to direct the **Font** dialog box to display the effects controls.</span></span> <span data-ttu-id="8f312-111">Mit diesen Steuerelementen können Benutzer sowohl eine Schriftart Farbe als auch durchgestrichen und Unterstreichung auswählen.</span><span class="sxs-lookup"><span data-stu-id="8f312-111">These controls let the user choose a font color as well as strikethrough and underline effects.</span></span>

<span data-ttu-id="8f312-112">Die Initialisierungs Kennzeichen-Werte sind für jedes allgemeine Dialogfeld eindeutig und werden ausführlich von den **Flags** -Membern der folgenden Strukturen beschrieben, die Ihnen entsprechen:</span><span class="sxs-lookup"><span data-stu-id="8f312-112">The initialization flag values are unique to each common dialog box and are described in detail by the **Flags** members of the following structures that correspond to them:</span></span>

-   [<span data-ttu-id="8f312-113">**CHOOSECOLOR**</span><span class="sxs-lookup"><span data-stu-id="8f312-113">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
-   [<span data-ttu-id="8f312-114">**Auswahl Schriftart**</span><span class="sxs-lookup"><span data-stu-id="8f312-114">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [<span data-ttu-id="8f312-115">**FindReplace**</span><span class="sxs-lookup"><span data-stu-id="8f312-115">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
-   [<span data-ttu-id="8f312-116">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="8f312-116">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
-   [<span data-ttu-id="8f312-117">**Pagesetupdlg**</span><span class="sxs-lookup"><span data-stu-id="8f312-117">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
-   [<span data-ttu-id="8f312-118">**PRINTDLG**</span><span class="sxs-lookup"><span data-stu-id="8f312-118">**PRINTDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlga)
-   [<span data-ttu-id="8f312-119">**Printdlgex**</span><span class="sxs-lookup"><span data-stu-id="8f312-119">**PRINTDLGEX**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

 

 




