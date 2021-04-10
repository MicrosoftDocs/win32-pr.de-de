---
title: Steuerelement Steuerung
description: Definiert ein benutzerdefiniertes Steuerelement.
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703f95778c66522d67e40a51293c8fb8fe956ecb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948673"
---
# <a name="control-control"></a><span data-ttu-id="6454c-104">Steuerelement Steuerung</span><span class="sxs-lookup"><span data-stu-id="6454c-104">CONTROL control</span></span>

<span data-ttu-id="6454c-105">Definiert ein benutzerdefiniertes Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="6454c-105">Defines a user-defined control.</span></span>

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span data-ttu-id="6454c-106"><span id="class"></span><span id="CLASS"></span>*klassi*</span><span class="sxs-lookup"><span data-stu-id="6454c-106"><span id="class"></span><span id="CLASS"></span>*class*</span></span>
</dt> <dd>

<span data-ttu-id="6454c-107">Ein neu definierter Name, eine Zeichenfolge oder ein 16-Bit-ganz Zahl Wert ohne Vorzeichen, der die Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="6454c-107">Redefined name, character string, or a 16-bit unsigned integer value that defines the class.</span></span> <span data-ttu-id="6454c-108">Dabei kann es sich um eine beliebige Steuerelement Klasse handeln. eine Liste der Steuerelement Klassen finden Sie in der ersten Liste, die dieser Beschreibung folgt.</span><span class="sxs-lookup"><span data-stu-id="6454c-108">This can be any one of the control classes; for a list of the control classes, see the first list following this description.</span></span> <span data-ttu-id="6454c-109">Wenn der Wert ein neu definierter Name ist, der von der Anwendung bereitgestellt wird, muss er eine Zeichenfolge sein, die in doppelten Anführungszeichen (") eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6454c-109">If the value is a redefined name supplied by the application, it must be a string enclosed in double quotation marks (").</span></span>

</dd> <dt>

<span data-ttu-id="6454c-110"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="6454c-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="6454c-111">Neudefinierter Name oder ganzzahliger Wert, der den Stil des angegebenen Steuer Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="6454c-111">Redefined name or integer value that specifies the style of the given control.</span></span> <span data-ttu-id="6454c-112">Die genaue Bedeutung von *Style* hängt vom Wert der- *Klasse* ab.</span><span class="sxs-lookup"><span data-stu-id="6454c-112">The exact meaning of *style* depends on the *class* value.</span></span> <span data-ttu-id="6454c-113">In den Abschnitten nach dieser Beschreibung werden die Steuerelement Klassen und die entsprechenden Stile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6454c-113">The sections following this description show the control classes and corresponding styles.</span></span>

</dd> </dl>

<span data-ttu-id="6454c-114">Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6454c-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6454c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6454c-115">Remarks</span></span>

<span data-ttu-id="6454c-116">Die sechs möglichen Steuerelement Klassen werden in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6454c-116">The six possible control classes are described in the following sections.</span></span>

### <a name="the-button-control-class"></a><span data-ttu-id="6454c-117">Die Button-Steuerelement Klasse</span><span class="sxs-lookup"><span data-stu-id="6454c-117">The Button Control Class</span></span>

<span data-ttu-id="6454c-118">Ein Schaltflächen-Steuerelement ist ein kleines rechteckiges untergeordnetes Fenster, das der Benutzer aktivieren oder deaktivieren kann, indem er mit der Maus darauf klickt.</span><span class="sxs-lookup"><span data-stu-id="6454c-118">A button control is a small rectangular child window that the user can turn on or off by clicking it with the mouse.</span></span> <span data-ttu-id="6454c-119">Schaltflächen-Steuerelemente können allein oder in Gruppen verwendet werden und können entweder als bezeichnet oder ohne Text angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6454c-119">Button controls can be used alone or in groups, and can either be labeled or appear without text.</span></span> <span data-ttu-id="6454c-120">Schaltflächen Steuerelemente ändern die Darstellung normalerweise, wenn der Benutzer darauf klickt.</span><span class="sxs-lookup"><span data-stu-id="6454c-120">Button controls typically change appearance when the user clicks them.</span></span>

<span data-ttu-id="6454c-121">Die Schaltflächen Stile werden im folgenden Thema beschrieben: [Schalt](../controls/button-styles.md)Flächen Formate.</span><span class="sxs-lookup"><span data-stu-id="6454c-121">The button styles are described in the following topic: [Button Styles](../controls/button-styles.md).</span></span>

### <a name="the-combo-box-control-class"></a><span data-ttu-id="6454c-122">Die Kombinations Feld-Steuerelement Klasse</span><span class="sxs-lookup"><span data-stu-id="6454c-122">The Combo Box Control Class</span></span>

<span data-ttu-id="6454c-123">Kombinations Feld-Steuerelemente bestehen aus einem Auswahlfeld, das einem Bearbeitungs Steuerelement plus einem Listenfeld ähnelt.</span><span class="sxs-lookup"><span data-stu-id="6454c-123">Combo box controls consist of a selection field similar to an edit control plus a list box.</span></span> <span data-ttu-id="6454c-124">Das Listenfeld wird möglicherweise jederzeit oder nach unten angezeigt, wenn der Benutzer ein "Popbox" neben dem Auswahlfeld auswählt.</span><span class="sxs-lookup"><span data-stu-id="6454c-124">The list box may be displayed at all times or may be dropped down when the user selects a "pop box" next to the selection field.</span></span>

<span data-ttu-id="6454c-125">Abhängig vom Format des Kombinations Felds kann der Benutzer den Inhalt des Auswahl Felds oder nicht bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6454c-125">Depending on the style of the combo box, the user can or cannot edit the contents of the selection field.</span></span> <span data-ttu-id="6454c-126">Wenn das Listenfeld sichtbar ist, wird durch das Eingeben von Zeichen in das Auswahlfeld der erste Eintrag hervorgehoben, der mit den typisierten Zeichen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="6454c-126">If the list box is visible, typing characters into the selection box will cause the first entry that matches the characters typed to be highlighted.</span></span> <span data-ttu-id="6454c-127">Umgekehrt wird beim Auswählen eines Elements im Listenfeld der ausgewählte Text im Feldauswahl angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6454c-127">Conversely, selecting an item in the list box displays the selected text in the selection field.</span></span>

<span data-ttu-id="6454c-128">Die Kombinations Feld-Steuerelement Stile werden im folgenden Thema beschrieben: Kombinations [Feld-Stile](../controls/combo-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="6454c-128">The combo box control styles are described in the following topic: [Combo Box Styles](../controls/combo-box-styles.md).</span></span>

### <a name="the-edit-control-class"></a><span data-ttu-id="6454c-129">Die Edit-Steuerelement Klasse</span><span class="sxs-lookup"><span data-stu-id="6454c-129">The Edit Control Class</span></span>

<span data-ttu-id="6454c-130">Ein Bearbeitungs Steuerelement ist ein rechteckiges untergeordnetes Fenster, in dem der Benutzer Text von der Tastatur eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="6454c-130">An edit control is a rectangular child window in which the user can enter text from the keyboard.</span></span> <span data-ttu-id="6454c-131">Der Benutzer wählt das Steuerelement aus und gibt ihm den Eingabefokus, indem er auf die Maus klickt oder die Tab-Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="6454c-131">The user selects the control, and gives it the input focus, by clicking the mouse inside it or pressing the TAB key.</span></span> <span data-ttu-id="6454c-132">Der Benutzer kann Text eingeben, wenn das Steuerelement eine blinkende Einfügemarke anzeigt.</span><span class="sxs-lookup"><span data-stu-id="6454c-132">The user can enter text when the control displays a flashing insertion point.</span></span> <span data-ttu-id="6454c-133">Die Maus kann zum Verschieben des Cursors und zum Auswählen von zu ersetzenden Zeichen oder zum Positionieren des Cursors zum Einfügen von Zeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6454c-133">The mouse can be used to move the cursor and select characters to be replaced, or to position the cursor for inserting characters.</span></span> <span data-ttu-id="6454c-134">Mithilfe der RÜCKTASTE können Zeichen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="6454c-134">The BACKSPACE key can be used to delete characters.</span></span>

<span data-ttu-id="6454c-135">Bearbeitungs Steuerelemente verwenden die Schriftart mit fester Größe und Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6454c-135">Edit controls use the fixed-pitch font and display Unicode characters.</span></span> <span data-ttu-id="6454c-136">Sie erweitern Tabstopp Zeichen in so viele Leerzeichen, wie erforderlich sind, um den Cursor auf den nächsten Tabstopp zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="6454c-136">They expand tab characters into as many space characters as are required to move the cursor to the next tab stop.</span></span> <span data-ttu-id="6454c-137">Es wird davon ausgegangen, dass Tabstopps an jeder Position an acht Zeichen stehen.</span><span class="sxs-lookup"><span data-stu-id="6454c-137">Tab stops are assumed to be at every eighth character position.</span></span>

<span data-ttu-id="6454c-138">Die Bearbeitungs Steuerelement Stile werden im folgenden Thema beschrieben: [Bearbeiten von Steuerelement Stilen](../controls/edit-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="6454c-138">The edit control styles are described in the following topic: [Edit Control Styles](../controls/edit-control-styles.md).</span></span>

### <a name="the-list-box-control-class"></a><span data-ttu-id="6454c-139">Die Listenfeld-Steuerelement Klasse</span><span class="sxs-lookup"><span data-stu-id="6454c-139">The List Box Control Class</span></span>

<span data-ttu-id="6454c-140">Listenfeld-Steuerelemente bestehen aus einer Liste von Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="6454c-140">List box controls consist of a list of character strings.</span></span> <span data-ttu-id="6454c-141">Das-Steuerelement wird immer dann verwendet, wenn eine Anwendung eine Liste von Namen, z. b. Dateinamen, darstellen muss, die der Benutzer anzeigen und auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="6454c-141">The control is used whenever an application needs to present a list of names, such as filenames, that the user can view and select.</span></span> <span data-ttu-id="6454c-142">Der Benutzer kann eine Zeichenfolge auswählen, indem er mit der Maus auf die Zeichenfolge zeigt und auf eine Maustaste klickt.</span><span class="sxs-lookup"><span data-stu-id="6454c-142">The user can select a string by pointing to the string with the mouse and clicking a mouse button.</span></span> <span data-ttu-id="6454c-143">Wenn eine Zeichenfolge ausgewählt ist, wird Sie hervorgehoben, und eine Benachrichtigungs Meldung wird an das übergeordnete Fenster übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6454c-143">When a string is selected, it is highlighted and a notification message is passed to the parent window.</span></span> <span data-ttu-id="6454c-144">Eine Schiebe Leiste kann mit einem Listenfeld-Steuerelement verwendet werden, um Listen aufzulisten, die für das Steuerelement Fenster zu lang oder zu breit sind.</span><span class="sxs-lookup"><span data-stu-id="6454c-144">A scroll bar can be used with a list box control to scroll lists that are too long or too wide for the control window.</span></span>

<span data-ttu-id="6454c-145">Die Listenfeld-Steuerelement Stile werden im folgenden Thema beschrieben: [Listenfeld Stile](../controls/list-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="6454c-145">The list box control styles are described in the following topic: [List Box Styles](../controls/list-box-styles.md).</span></span>

### <a name="the-scroll-bar-control-class"></a><span data-ttu-id="6454c-146">Die Scroll-Bar Steuerelement Klasse</span><span class="sxs-lookup"><span data-stu-id="6454c-146">The Scroll-Bar Control Class</span></span>

<span data-ttu-id="6454c-147">Bei einem Schiebe leisten-Steuerelement handelt es sich um ein Rechteck, das einen Bild Lauf Zieh Punkt enthält und Richtungspfeile an beiden Enden aufweist.</span><span class="sxs-lookup"><span data-stu-id="6454c-147">A scroll-bar control is a rectangle that contains a scroll thumb and has direction arrows at both ends.</span></span> <span data-ttu-id="6454c-148">Die Bild Lauf Leiste sendet eine Benachrichtigungs Meldung an das übergeordnete Element, wenn der Benutzer im Steuerelement auf die Maus klickt.</span><span class="sxs-lookup"><span data-stu-id="6454c-148">The scroll bar sends a notification message to its parent whenever the user clicks the mouse in the control.</span></span> <span data-ttu-id="6454c-149">Das übergeordnete Element ist für die Aktualisierung der Thumb-Position verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="6454c-149">The parent is responsible for updating the thumb position, if necessary.</span></span> <span data-ttu-id="6454c-150">Bild Lauf leisten-Steuerelemente verfügen über die gleiche Darstellung und Funktion wie die Bild Lauf leisten, die in normalen Fenstern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6454c-150">Scroll-bar controls have the same appearance and function as the scroll bars used in ordinary windows.</span></span> <span data-ttu-id="6454c-151">Aber im Gegensatz zu Bild Lauf leisten können Schiebe leisten-Steuerelemente an beliebiger Stelle in einem Fenster positioniert und immer dann verwendet werden, wenn Sie scrolleingaben für ein Fenster bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="6454c-151">But unlike scroll bars, scroll-bar controls can be positioned anywhere within a window and used whenever needed to provide scrolling input for a window.</span></span>

<span data-ttu-id="6454c-152">Die Stile der Scrollleiste werden im folgenden Thema beschrieben: Bild Lauf leisten- [Steuerelement Stile](../controls/scroll-bar-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="6454c-152">The scroll bar styles are described in the following topic: [Scroll Bar Control Styles](../controls/scroll-bar-control-styles.md).</span></span>

### <a name="the-static-control-class"></a><span data-ttu-id="6454c-153">Die statische Steuerelement Klasse</span><span class="sxs-lookup"><span data-stu-id="6454c-153">The Static Control Class</span></span>

<span data-ttu-id="6454c-154">Statische Steuerelemente sind einfache Textfelder, Felder und Rechtecke, die verwendet werden können, um andere Steuerelemente zu bezeichnen, zu Schachteln oder zu trennen.</span><span class="sxs-lookup"><span data-stu-id="6454c-154">Static controls are simple text fields, boxes, and rectangles that can be used to label, box, or separate other controls.</span></span> <span data-ttu-id="6454c-155">Statische Steuerelemente nehmen keine Eingaben auf und stellen keine Ausgabe bereit.</span><span class="sxs-lookup"><span data-stu-id="6454c-155">Static controls take no input and provide no output.</span></span>

<span data-ttu-id="6454c-156">Die statischen Steuerelement Stile werden im folgenden Thema beschrieben: [statische Steuerelement Stile](../controls/static-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="6454c-156">The static control styles are described in the following topic: [Static Control Styles](../controls/static-control-styles.md).</span></span>

 

 