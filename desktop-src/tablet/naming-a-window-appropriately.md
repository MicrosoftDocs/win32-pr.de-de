---
description: Übersicht über das Ordnungs gerechte Benennen eines Fensters und Festlegen der Fenster Beschriftung für den Tablet PC.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Entsprechendes Benennen eines Fensters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaee320f621acf834d7c0ec5978a9e42f0811e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356931"
---
# <a name="naming-a-window-appropriately"></a><span data-ttu-id="44d61-103">Entsprechendes Benennen eines Fensters</span><span class="sxs-lookup"><span data-stu-id="44d61-103">Naming a Window Appropriately</span></span>

<span data-ttu-id="44d61-104">Weisen Sie jedem Fenster eine benutzerfreundliche Beschriftung zu, auch wenn das Fenster oder die Beschriftung unsichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="44d61-104">Assign every window a user-friendly caption, even if the window or its caption is invisible.</span></span> <span data-ttu-id="44d61-105">Dies ermöglicht es der Sprachfunktion, das Fenster und die Fenster Hierarchie zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="44d61-105">This allows the speech functionality to identify the window and the window hierarchy.</span></span> <span data-ttu-id="44d61-106">Diese Empfehlung gilt für alle Fenster: Fenster der obersten Ebene mit sichtbaren Frames. untergeordnete Fenster, z. b. Gleit Komma Zahlen; benutzerdefinierte Steuerelemente; Symbolleisten und Bereiche innerhalb eines Fensters, wenn Sie als untergeordnete Fenster implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="44d61-106">This recommendation applies to all windows: top-level windows with visible frames; child windows, such as floating palettes; custom controls; toolbars; and panes within a window, when implemented as child windows.</span></span>

<span data-ttu-id="44d61-107">Es gibt drei Möglichkeiten, die Fenster Beschriftung festzulegen:</span><span class="sxs-lookup"><span data-stu-id="44d61-107">There are three ways to set the window caption:</span></span>

-   <span data-ttu-id="44d61-108">Legen Sie die Zeichenfolge im Ressourcen Skript fest, wenn Sie [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) oder verwandte Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="44d61-108">Set the string in your resource script when calling [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or related functions.</span></span>
-   <span data-ttu-id="44d61-109">Aufrufen der [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="44d61-109">Call the [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) function.</span></span>
-   <span data-ttu-id="44d61-110">Definieren Sie den Namen der Steuerelemente in Dialogfeldern, indem Sie die unter Benennen von Steuer [Elementen in Dialogfeldern](naming-controls-in-dialog-boxes.md)beschriebenen Verfahren verwenden.</span><span class="sxs-lookup"><span data-stu-id="44d61-110">Define the name of controls in dialog boxes by using the techniques described in [Naming Controls in Dialog Boxes](naming-controls-in-dialog-boxes.md).</span></span> <span data-ttu-id="44d61-111">Dies ist die einzige Methode für die Bezeichnung eines Bearbeitungs Steuer Elements, da der Inhalt der Steuerelemente durch Festlegen der systeminternen Bezeichnung Steuerelemente geändert wird.</span><span class="sxs-lookup"><span data-stu-id="44d61-111">This is the only method for labeling an edit control, because setting the controls intrinsic label changes the controls contents.</span></span>

<span data-ttu-id="44d61-112">Sie können die Beschriftung entweder mithilfe von Microsoft Active Accessibility oder der WM \_ gettext-Nachricht Abfragen.</span><span class="sxs-lookup"><span data-stu-id="44d61-112">You can query the caption by using either Microsoft Active Accessibility or the WM\_GETTEXT message.</span></span>

<span data-ttu-id="44d61-113">Weitere Informationen zum Abfragen der Beschriftung mithilfe Active Accessibility finden Sie im Abschnitt zur [Barrierefreiheit](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="44d61-113">For more information about querying the caption by using Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
