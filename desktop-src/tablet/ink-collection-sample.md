---
description: Diese Anwendung basiert auf dem InkCollector-Objekt und veranschaulicht die Auflistung von frei Hand Eingaben.
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: Ink Collection-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f31ce83a55b6f352d76ad1cb8d184b41618c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128996"
---
# <a name="ink-collection-sample"></a><span data-ttu-id="28348-103">Ink Collection-Beispiel</span><span class="sxs-lookup"><span data-stu-id="28348-103">Ink Collection Sample</span></span>

<span data-ttu-id="28348-104">Diese Anwendung basiert auf dem [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt und veranschaulicht die Auflistung von frei Hand Eingaben.</span><span class="sxs-lookup"><span data-stu-id="28348-104">This application is based on the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object and demonstrates the collection of ink.</span></span> <span data-ttu-id="28348-105">Die Anwendung erstellt ein Fenster, fügt ein InkCollector-Objekt an Sie an und stellt dem Benutzermenü Optionen zur Verfügung, die zum Ändern der frei Hand Farbe, der frei Handbreite und zum Aktivieren und Deaktivieren der frei Hand Eingabe verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="28348-105">The application creates a window, attaches an InkCollector object to it, and provides the user with menu choices that can be used to change the ink color, the ink width, and enable and disable ink collection.</span></span>

> [!Note]  
> <span data-ttu-id="28348-106">Die in diesem Abschnitt erörterte Version ist Visual Basic .net.</span><span class="sxs-lookup"><span data-stu-id="28348-106">The version discussed in this section is Visual Basic .NET.</span></span> <span data-ttu-id="28348-107">Die Konzepte sind zwischen anderen Sprachversionen in der Samples Library identisch.</span><span class="sxs-lookup"><span data-stu-id="28348-107">The concepts are the same between other language versions in the samples library.</span></span>

 

## <a name="declaring-the-inkcollector"></a><span data-ttu-id="28348-108">Der InkCollector wird deklariert.</span><span class="sxs-lookup"><span data-stu-id="28348-108">Declaring the InkCollector</span></span>

<span data-ttu-id="28348-109">Die Anwendung importiert zuerst den [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) -Namespace.</span><span class="sxs-lookup"><span data-stu-id="28348-109">The application first imports the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace.</span></span> <span data-ttu-id="28348-110">Anschließend deklariert die Anwendung `myInkCollector` , die das [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt für das Formular enthält.</span><span class="sxs-lookup"><span data-stu-id="28348-110">Then, the application declares `myInkCollector`, which holds the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object for the form.</span></span>


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a><span data-ttu-id="28348-111">Einrichten von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="28348-111">Setting Things Up</span></span>

<span data-ttu-id="28348-112">Die-Methode des Formulars `InkCollection_Load` behandelt das [Lade](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) Ereignis des Formulars.</span><span class="sxs-lookup"><span data-stu-id="28348-112">The form's `InkCollection_Load` method handles the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event.</span></span> <span data-ttu-id="28348-113">Es erstellt ein [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt, das dem Formular zugewiesen ist, ändert die [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) -Eigenschaft des InkCollector-Objekts und aktiviert das InkCollector-Objekt.</span><span class="sxs-lookup"><span data-stu-id="28348-113">It creates a [InkCollector](/previous-versions/ms836493(v=msdn.10)) object assigned to the form modifies the [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property of the InkCollector object and enables the InkCollector object.</span></span>


```C++
Private Sub InkCollection_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

    ' Create an ink collector and assign it to this form's window
    myInkCollector = New InkCollector(Me.Handle)

    ' Set the pen width to be a medium width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth

    ' If you do not modify the default drawing attributes, the default 
    ' drawing attributes will use the following properties and values:
    ' ...

    ' Turn the ink collector on
    myInkCollector.Enabled = True
End Sub
```



<span data-ttu-id="28348-114">Der [InkCollector](/previous-versions/ms836493(v=msdn.10)) wird dem Fenster des Formulars zugewiesen, indem das Fenster Handle des Formulars der [handle](/previous-versions/ms836504(v=msdn.10)) -Eigenschaft des InkCollector-Objekts zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="28348-114">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) is assigned to the form's window by assigning the form's window handle to the InkCollector object's [Handle](/previous-versions/ms836504(v=msdn.10)) property.</span></span> <span data-ttu-id="28348-115">Die frei Hand Auflistung wird aktiviert, indem die [aktivierte](/previous-versions/ms836503(v=msdn.10)) Eigenschaft des InkCollector-Objekts auf **true** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="28348-115">Ink collection is turned on by setting the InkCollector object's [Enabled](/previous-versions/ms836503(v=msdn.10)) property to **TRUE**.</span></span>

<span data-ttu-id="28348-116">Die [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) -Eigenschaft des [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekts legt die Standard Attribute fest, die einem neuen Cursor zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="28348-116">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property sets the default attributes that are assigned to a new cursor.</span></span> <span data-ttu-id="28348-117">Um unterschiedliche Attribute für einen neuen Cursor festzulegen, verwenden Sie die [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) -Eigenschaft des [Cursor](/previous-versions/ms839521(v=msdn.10)) Objekts.</span><span class="sxs-lookup"><span data-stu-id="28348-117">To set different attributes on a new cursor, use the [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) property of the [Cursor](/previous-versions/ms839521(v=msdn.10)) object.</span></span> <span data-ttu-id="28348-118">Verwenden Sie die [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) -Eigenschaft des [Stroke](/previous-versions/ms827842(v=msdn.10)) -Objekts, um die Zeichnungs Attribute eines einzelnen Strichs zu ändern.</span><span class="sxs-lookup"><span data-stu-id="28348-118">To change the drawing attributes of a single stroke, use the [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) property of the [Stroke](/previous-versions/ms827842(v=msdn.10)) object.</span></span>

## <a name="changing-the-properties"></a><span data-ttu-id="28348-119">Ändern der Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28348-119">Changing the Properties</span></span>

<span data-ttu-id="28348-120">Der Rest dieser einfachen Anwendung besteht aus Handlern für die verschiedenen Menü Optionen, die der Benutzer treffen kann.</span><span class="sxs-lookup"><span data-stu-id="28348-120">The rest of this simple application consists of handlers for the various menu selections the user can make.</span></span> <span data-ttu-id="28348-121">Wenn der Benutzer z. b. die frei Hand Farbe in Rot ändern möchte, indem er im frei Hand Menü Rot ausgewählt wird, wird die Farbe mithilfe der [Color](/previous-versions/ms837933(v=msdn.10)) -Eigenschaft für die [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) -Eigenschaft des [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekts im Ereignishandler für das Menü geändert.</span><span class="sxs-lookup"><span data-stu-id="28348-121">For example, when the user chooses to change the ink color to red by selecting Red from the Ink menu, the color is changed using the [Color](/previous-versions/ms837933(v=msdn.10)) property on [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property in the event handler for the menu.</span></span>


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a><span data-ttu-id="28348-122">Schließen des Formulars</span><span class="sxs-lookup"><span data-stu-id="28348-122">Closing the Form</span></span>

<span data-ttu-id="28348-123">Die [verwerfen-Methode des Formulars](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) gibt das [InkCollector](/previous-versions/ms836493(v=msdn.10)) -Objekt frei `myInkCollector` .</span><span class="sxs-lookup"><span data-stu-id="28348-123">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object, `myInkCollector`.</span></span>

 

 
