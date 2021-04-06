---
title: Lokalisierungsunterstützung für allgemeine Steuerelemente
description: In diesem Thema wird die Unterstützung für nationale Sprachen beschrieben, die in die allgemeinen Steuerelemente integriert sind.
ms.assetid: c5720198-9071-4213-8dad-50b4c015c5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccc307defa687c8640425dd781660641fe78a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947509"
---
# <a name="localization-support-for-common-controls"></a><span data-ttu-id="b8966-103">Lokalisierungsunterstützung für allgemeine Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b8966-103">Localization Support for Common Controls</span></span>

<span data-ttu-id="b8966-104">In diesem Thema wird die Unterstützung für nationale Sprachen beschrieben, die in die allgemeinen Steuerelemente integriert sind.</span><span class="sxs-lookup"><span data-stu-id="b8966-104">This topic describes the support for national languages that is built into the common controls.</span></span> <span data-ttu-id="b8966-105">Die integrierte Unterstützung für nationale Sprachen vereinfacht die Implementierung lokalisierter Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="b8966-105">The built-in national language support simplifies the implementation of localized applications.</span></span>

<span data-ttu-id="b8966-106">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="b8966-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b8966-107">Angeben einer Sprache für die allgemeinen Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b8966-107">Specifying a Language for the Common Controls</span></span>](#specifying-a-language-for-the-common-controls)
-   [<span data-ttu-id="b8966-108">Angeben einer Sprache für Steuerelemente in einem Dialog Feld</span><span class="sxs-lookup"><span data-stu-id="b8966-108">Specifying a Language for Controls in a Dialog Box</span></span>](#specifying-a-language-for-controls-in-a-dialog-box)
-   [<span data-ttu-id="b8966-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b8966-109">Related topics</span></span>](#related-topics)

## <a name="specifying-a-language-for-the-common-controls"></a><span data-ttu-id="b8966-110">Angeben einer Sprache für die allgemeinen Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b8966-110">Specifying a Language for the Common Controls</span></span>

<span data-ttu-id="b8966-111">Wenn Sie eine Sprache für die allgemeinen Steuerelemente angeben möchten, die sich von der Systemsprache unterscheiden, wenden Sie sich an [**initmuilanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="b8966-111">If you want to specify a language for the common controls that is different than the system language, call [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span></span> <span data-ttu-id="b8966-112">Die von dieser Funktion angegebene Sprache gilt nur für den Prozess, von dem die Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b8966-112">The language specified by this function applies only to the process from which the function is called.</span></span>

<span data-ttu-id="b8966-113">Um die Sprache zu bestimmen, die derzeit von den allgemeinen Steuerelementen verwendet wird, nennen Sie [**getmuilanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="b8966-113">To determine the language currently being used by the common controls, call [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage).</span></span> <span data-ttu-id="b8966-114">Er gibt den Wert zurück, der durch einen vorherigen [**initmuilanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage)-Rückruf festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="b8966-114">It returns the value that was set by a previous call to [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span></span> <span data-ttu-id="b8966-115">Die zurückgegebene Sprache ist die, die für den Prozess angegeben wurde, von dem Sie aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b8966-115">The language returned is the one that was specified for the process it is called from.</span></span> <span data-ttu-id="b8966-116">Wenn **initmuilanguage** nicht aufgerufen wurde oder von einem anderen Prozess aufgerufen wurde, gibt **getmuilanguage** einen Standardwert zurück.</span><span class="sxs-lookup"><span data-stu-id="b8966-116">If **InitMUILanguage** has not been called, or was called from another process, **GetMUILanguage** will return a default value.</span></span>

## <a name="specifying-a-language-for-controls-in-a-dialog-box"></a><span data-ttu-id="b8966-117">Angeben einer Sprache für Steuerelemente in einem Dialog Feld</span><span class="sxs-lookup"><span data-stu-id="b8966-117">Specifying a Language for Controls in a Dialog Box</span></span>

<span data-ttu-id="b8966-118">Im Gegensatz zu allgemeinen Steuerelementen wird die aktuelle Systemsprache von vordefinierten Steuerelementen wie Schaltflächen oder Bearbeitungs Feldern nicht standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8966-118">Unlike common controls, predefined controls such as buttons or edit boxes do not use the current system language by default.</span></span> <span data-ttu-id="b8966-119">Das Native Schriftart Steuerelement ist ein unsichtbares Steuerelement, das im Hintergrund funktioniert, damit die vordefinierten Steuerelemente eines Dialog Felds die aktuelle Systemsprache anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="b8966-119">The native font control is an invisible control that works in the background to allow a dialog box's predefined controls to display the current system language.</span></span>

<span data-ttu-id="b8966-120">Gehen Sie folgendermaßen vor, um das Native Schriftart Steuerelement zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8966-120">To use the native font control, follow this procedure.</span></span>

1.  <span data-ttu-id="b8966-121">Initialisieren Sie das Native Schriftart Steuerelement durch Aufrufen von [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span><span class="sxs-lookup"><span data-stu-id="b8966-121">Initialize the native font control by calling [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span></span> <span data-ttu-id="b8966-122">Legen Sie den **dwicc** -Member der [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur, auf die von *lpinitctrls* verwiesen wird, auf die Klasse "ICC \_ nativefntctl" fest \_ .</span><span class="sxs-lookup"><span data-stu-id="b8966-122">Set the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure pointed to by *lpInitCtrls* to ICC\_NATIVEFNTCTL\_CLASS.</span></span>
2.  <span data-ttu-id="b8966-123">Fügen Sie dem Ressourcen Skript für das Dialogfeld das-Steuerelement hinzu.</span><span class="sxs-lookup"><span data-stu-id="b8966-123">Add the control to the resource script for the dialog box.</span></span> <span data-ttu-id="b8966-124">Legen Sie mindestens eines der folgenden stilflags fest, um anzugeben, welche Steuerelemente betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="b8966-124">Set one or more of the following style flags to specify which controls will be affected.</span></span> 

    | <span data-ttu-id="b8966-125">Flag</span><span class="sxs-lookup"><span data-stu-id="b8966-125">Flag</span></span>              | <span data-ttu-id="b8966-126">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="b8966-126">Applies to</span></span>                                                                                                                                                                                                                                                       |
    |-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="b8966-127">NFS- \_ Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="b8966-127">NFS\_EDIT</span></span>         | <span data-ttu-id="b8966-128">Steuerelemente bearbeiten</span><span class="sxs-lookup"><span data-stu-id="b8966-128">Edit controls</span></span>                                                                                                                                                                                                                                                    |
    | <span data-ttu-id="b8966-129">NFS \_ static</span><span class="sxs-lookup"><span data-stu-id="b8966-129">NFS\_STATIC</span></span>       | <span data-ttu-id="b8966-130">Statische Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b8966-130">Static controls</span></span>                                                                                                                                                                                                                                                  |
    | <span data-ttu-id="b8966-131">NFS- \_ listcombo</span><span class="sxs-lookup"><span data-stu-id="b8966-131">NFS\_LISTCOMBO</span></span>    | <span data-ttu-id="b8966-132">Listen-, ComboBox-, List-View-und ComboBoxEx-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b8966-132">List, ComboBox, List-View, and ComboBoxEx controls</span></span>                                                                                                                                                                                                               |
    | <span data-ttu-id="b8966-133">NFS- \_ Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="b8966-133">NFS\_BUTTON</span></span>       | <span data-ttu-id="b8966-134">Schaltflächen-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b8966-134">Button controls</span></span>                                                                                                                                                                                                                                                  |
    | <span data-ttu-id="b8966-135">\_alle NFS</span><span class="sxs-lookup"><span data-stu-id="b8966-135">NFS\_ALL</span></span>          | <span data-ttu-id="b8966-136">Alle Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b8966-136">All controls</span></span>                                                                                                                                                                                                                                                     |
    | <span data-ttu-id="b8966-137">NFS \_ usefontassoc</span><span class="sxs-lookup"><span data-stu-id="b8966-137">NFS\_USEFONTASSOC</span></span> | <span data-ttu-id="b8966-138">Ostasiatische Plattform.</span><span class="sxs-lookup"><span data-stu-id="b8966-138">East Asian platform.</span></span> <span data-ttu-id="b8966-139">Das-Steuerelement verwendet die Schriftart Zuordnungs Funktion, anstatt zur systemeigenen Schriftart zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="b8966-139">The control uses the font association feature instead of switching to the native font.</span></span> <span data-ttu-id="b8966-140">Alle anderen Plattformen ignorieren diese.</span><span class="sxs-lookup"><span data-stu-id="b8966-140">All other platforms ignore it.</span></span> <span data-ttu-id="b8966-141">Dies ist für Windows Vista veraltet und wird in COMCTL V6 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b8966-141">This is deprecated for Windows Vista, and is not supported in comctl v6.</span></span> <span data-ttu-id="b8966-142">Dies ist in COMCTL V5 aus Legacy Gründen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b8966-142">This exists in comctl v5 for legacy reasons.</span></span> |

    

     

<span data-ttu-id="b8966-143">Im folgenden Beispiel wird veranschaulicht, wie einem Ressourcen Skript ein System eigenes Schriftart Steuerelement hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b8966-143">The following example illustrates how to add a native font control to a resource script.</span></span> <span data-ttu-id="b8966-144">Dies bewirkt, dass die Steuerelemente bearbeiten, auflisten und Kombinations Feld des Dialog Felds Text mithilfe der aktuellen Systemsprache anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b8966-144">It causes the dialog box's edit, list, and combo box controls to display text using the current system language.</span></span>


```
CONTROL    "",-1,"NativeFontCtl",NFS_EDIT|NFS_LISTCOMBO,0,0,0,0
```



## <a name="related-topics"></a><span data-ttu-id="b8966-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b8966-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8966-146">Informationen zu allgemeinen Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="b8966-146">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 




