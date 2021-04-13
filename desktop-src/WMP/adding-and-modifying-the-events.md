---
title: Hinzufügen und Ändern der Ereignisse
description: Hinzufügen und Ändern der Ereignisse
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Windows Media Player-Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample-Eigenschaften Seiten
- DSP-Plug-ins, Echo Sample-Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c8e069c20dc2c953998b9e5c2a47f509166ca3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310607"
---
# <a name="adding-and-modifying-the-events"></a><span data-ttu-id="a4cf8-109">Hinzufügen und Ändern der Ereignisse</span><span class="sxs-lookup"><span data-stu-id="a4cf8-109">Adding and Modifying the Events</span></span>

<span data-ttu-id="a4cf8-110">Sie müssen Ereignishandler für die en- \_ Änderungs Ereignisse angeben, die auftreten, wenn der Benutzer den Text in den Bearbeitungs Feldern der Eigenschaften Seite ändert.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-110">You need to supply event handlers for the EN\_CHANGE events that occur when the user changes the text in the property page edit boxes.</span></span> <span data-ttu-id="a4cf8-111">Diese Ereignishandler verfügen über eine einfache Implementierung, die im Dialogfeld Eigenschaften Seite nur die Option **anwenden** ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-111">These event handlers have a simple implementation that merely enables **Apply** in the property page dialog box.</span></span>

## <a name="modifying-the-scale-factor-event-handler"></a><span data-ttu-id="a4cf8-112">Ändern des Skalierungsfaktor-Ereignis Handlers</span><span class="sxs-lookup"><span data-stu-id="a4cf8-112">Modifying the Scale Factor Event Handler</span></span>

<span data-ttu-id="a4cf8-113">Sie müssen den Namen des vorhandenen Ereignis Handlers ändern, den der Plug-in-Assistent für das Bearbeitungsfeld "Skalierungsfaktor" bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-113">You need to change the name of the existing event handler that the plug-in wizard provided for the scale factor edit box.</span></span> <span data-ttu-id="a4cf8-114">Sie sollten den Namen in "onchangescale" in "onchangedelay" an drei Stellen ändern:</span><span class="sxs-lookup"><span data-stu-id="a4cf8-114">You should change the name from OnChangeScale to OnChangeDelay in three locations:</span></span>

1.  <span data-ttu-id="a4cf8-115">Ändern Sie in "echoproppage. h" den Namen im Abschnitt "Message Map Macro".</span><span class="sxs-lookup"><span data-stu-id="a4cf8-115">In EchoPropPage.h, change the name in the message map macro section.</span></span> <span data-ttu-id="a4cf8-116">Ersetzen Sie die Zeile, in der das Ereignis für den Skalierungsfaktor geändert wird, mit dem folgenden Code der onchangescale-Methode:</span><span class="sxs-lookup"><span data-stu-id="a4cf8-116">Replace the line that maps the scale factor change event to the OnChangeScale method with the following code:</span></span>
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  <span data-ttu-id="a4cf8-117">Ändern Sie in "echoproppage. h" den Namen in der Zeile, in der die onchangescale-Funktion Prototypen ist:</span><span class="sxs-lookup"><span data-stu-id="a4cf8-117">In EchoPropPage.h, change the name in the line that prototypes the OnChangeScale function:</span></span>
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  <span data-ttu-id="a4cf8-118">Ändern Sie in "echoproppage. cpp" den Namen im Funktions Header:</span><span class="sxs-lookup"><span data-stu-id="a4cf8-118">In EchoPropPage.cpp, change the name in the function header:</span></span>
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a><span data-ttu-id="a4cf8-119">Hinzufügen des nass Mischungs Ereignis Handlers</span><span class="sxs-lookup"><span data-stu-id="a4cf8-119">Adding the Wet Mix Event Handler</span></span>

<span data-ttu-id="a4cf8-120">Sie können problemlos den Ereignishandler für das en- \_ Änderungs Ereignis hinzufügen, das an das Steuerelement für den IDC- \_ wetmix-Bearbeitungsfeld angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-120">You can easily add the event handler for the EN\_CHANGE event that is attached to the IDC\_WETMIX edit box control.</span></span> <span data-ttu-id="a4cf8-121">Im Dialogfeld Ressourcen-Editor:</span><span class="sxs-lookup"><span data-stu-id="a4cf8-121">From the dialog resource editor:</span></span>

1.  <span data-ttu-id="a4cf8-122">Klicken Sie mit der rechten Maustaste auf das \_ Bearbeitungsfeld IDC wetmix, und wählen Sie **Ereignisse**.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-122">Right-click the IDC\_WETMIX edit box and choose **Events**.</span></span> <span data-ttu-id="a4cf8-123">Das Dialogfeld neue Windows-Meldung und Ereignishandler wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-123">The New Windows Message and Event Handlers dialog box appears.</span></span>
2.  <span data-ttu-id="a4cf8-124">Klicken Sie im Feld **zu behandelnde Klasse oder Objekt auf** den Namen der Bearbeitungsfeld Ressource, IDC- \_ wetmix.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-124">In the **Class or object to handle** box, click the name of the edit box resource, IDC\_WETMIX.</span></span>
3.  <span data-ttu-id="a4cf8-125">Klicken Sie im Feld **neue Windows-Meldungen/Ereignisse** \_ auf en ändern, um es auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-125">In the **New Windows messages/events** box, click EN\_CHANGE to select it.</span></span>
4.  <span data-ttu-id="a4cf8-126">Klicken Sie auf **Handler hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-126">Click **Add Handler**.</span></span> <span data-ttu-id="a4cf8-127">Das Dialogfeld Element Funktion hinzufügen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-127">The Add Member Function dialog box appears.</span></span>
5.  <span data-ttu-id="a4cf8-128">Geben Sie im Feld Element **Funktionsname** den Namen onchangewetmix ein.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-128">In the **Member function name** box, type the name OnChangeWetmix.</span></span>
6.  <span data-ttu-id="a4cf8-129">Klicken Sie auf **OK** , um das Dialogfeld Element Funktion hinzufügen zu schließen.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-129">Click **OK** to close the Add Member Function dialog box.</span></span>
7.  <span data-ttu-id="a4cf8-130">Klicken Sie auf **OK** , um zum Dialogfeld Ressourcen-Editor zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-130">Click **OK** to return to the dialog box resource editor.</span></span>

<span data-ttu-id="a4cf8-131">Visual C++ fügt automatisch den Code für die Meldungs Zuordnung und die Ereignishandlerfunktion in "echoproppage. h" ein.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-131">Visual C++ automatically adds the code for the message map and for the event handler function to EchoPropPage.h.</span></span> <span data-ttu-id="a4cf8-132">Der Code, den er einfügt, bietet einen TODO-Kommentar, in dem Sie die-Implementierung in den-Header für die Funktion einfügen können.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-132">The code it inserts provides a TODO comment where you can add the implementation in the header for the function.</span></span> <span data-ttu-id="a4cf8-133">Dies ist ein etwas anderes Format als der Windows Media Player Plug-in-Assistent, der Beispielcode verwendet, aber akzeptabel ist.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-133">This is a slightly different style than the Windows Media Player Plug-in Wizard sample code uses, but is acceptable.</span></span>

<span data-ttu-id="a4cf8-134">Ob Sie Ihre Implementierung in die Header Datei schreiben oder Sie in "echoproppage. cpp" verschieben möchten, ist Ihnen überlassen.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-134">Whether you want to write your implementation in the header file or move it to EchoPropPage.cpp is up to you.</span></span> <span data-ttu-id="a4cf8-135">In beiden Fällen benötigt die Implementierung nur eine einzige zusätzliche Codezeile, um **Apply** im Dialogfeld der Eigenschaften Seite zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-135">In either case, the implementation needs only a single additional line of code to enable **Apply** in the property page dialog.</span></span> <span data-ttu-id="a4cf8-136">Fügen Sie diese Codezeile vor der Zeile ein, die von der-Funktion zurückgegeben wird:</span><span class="sxs-lookup"><span data-stu-id="a4cf8-136">Insert this line of code before the line that returns from the function:</span></span>


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a><span data-ttu-id="a4cf8-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4cf8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4cf8-138">**Ändern der Eigenschaften Seite Echo Sample**</span><span class="sxs-lookup"><span data-stu-id="a4cf8-138">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




