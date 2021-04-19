---
description: Dieses Beispiel baut auf dem Formular Beispiel für automatische Ansprüche auf, indem das Objekt "pinputpanel" integriert wird. Das Beispiel befindet sich im Verzeichnis "C \# pipanel" im Ordner "autoclaims".
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: Beispiel für "pinputpanel"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d60f33ff3f61e1a2930841e5fd3d3ce3f9fc5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369825"
---
# <a name="peninputpanel-sample"></a><span data-ttu-id="f5bf2-104">Beispiel für "pinputpanel"</span><span class="sxs-lookup"><span data-stu-id="f5bf2-104">PenInputPanel Sample</span></span>

<span data-ttu-id="f5bf2-105">Dieses Beispiel baut auf dem Formular Beispiel für automatische Ansprüche auf, indem das Objekt " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) " integriert wird.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-105">This sample builds on the Auto Claims Form sample by integrating the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span> <span data-ttu-id="f5bf2-106">Das Beispiel befindet sich im Verzeichnis "C \# pipanel" im Ordner "autoclaims".</span><span class="sxs-lookup"><span data-stu-id="f5bf2-106">The sample is in the C\# PIPanel directory in the AutoClaims folder.</span></span>

> [!Note]  
> <span data-ttu-id="f5bf2-107">Für dieses Beispiel ist es erforderlich, dass das System mit einem Stift Gerät ausgestattet ist.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-107">This sample requires that your system is equipped with a pen device.</span></span> <span data-ttu-id="f5bf2-108">Wenn Sie nur eine Maus verwenden (oder ein anderes Gerät, das kein Personal Interface (HID) ist), wird das " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) " nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-108">If you are using just a mouse (or other non-human interface device (HID) pointing device) the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) does not appear.</span></span>

 

<span data-ttu-id="f5bf2-109">Weitere Informationen zum Beispiel für ein automatisches Anspruchsformular finden Sie unter [Beispiel für automatisches Anspruchsformular](auto-claims-form-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f5bf2-109">For more information about the Auto Claims Form sample, see [Auto Claims Form Sample](auto-claims-form-sample.md).</span></span> <span data-ttu-id="f5bf2-110">Weitere Informationen zum Objekt " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) " finden [Sie unter Programmieren des Eingabe Panels mithilfe der Klasse "pinputpanel](programming-the-input-panel-using-the-peninputpanel-class.md)".</span><span class="sxs-lookup"><span data-stu-id="f5bf2-110">For more information about the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object, see [Programming the Input Panel Using the PenInputPanel Class](programming-the-input-panel-using-the-peninputpanel-class.md).</span></span>

<span data-ttu-id="f5bf2-111">Im Beispiel enthält das Formular für automatische Ansprüche fünf Felder, in die der Benutzer aufgefordert wird, relevante Informationen für den Anspruch zu platzieren: Richtlinien Nummer, Name des Versicherten, Jahr, Marke und Modell des Autos.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-111">In the sample, the Auto Claims Form contains five fields into which the user is asked to put information relevant to the claim: policy number, insured name, the year, make, and model of the car.</span></span> <span data-ttu-id="f5bf2-112">Ein [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) -Objekt wird an jedes Eingabefeld angehängt, um eine einfache Möglichkeit zum Eingeben von Werten mit einem Stift zu bieten.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-112">A [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is attached to each input field to provide an easy means for entering values with a pen.</span></span>

<span data-ttu-id="f5bf2-113">Es gibt zwei Verfahren zum Anfügen eines " [larinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekts an die Eingabefelder in Ihrem Formular.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-113">There are two techniques for attaching a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to the input fields on your form.</span></span> <span data-ttu-id="f5bf2-114">Die erste Methode besteht darin, jedem Eingabefeld zur Entwurfszeit eine separate Instanz des-Objekts zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-114">The first technique is to assign a separate instance of the object to each input field at design time.</span></span> <span data-ttu-id="f5bf2-115">Die zweite besteht darin, eine einzelne Instanz des Objekts zu erstellen und diese Objektinstanz zur Laufzeit an ein Feld anzufügen, wenn Sie den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-115">The second is to create a single instance of the object and then attach that object instance at run time to a field when it receives focus.</span></span> <span data-ttu-id="f5bf2-116">In diesem Beispiel werden beide Methoden veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-116">This sample demonstrates both techniques.</span></span>

<span data-ttu-id="f5bf2-117">Es gibt Kompromisse bei der Entscheidung, welches Verfahren Sie verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-117">There are tradeoffs involved in deciding which technique to use.</span></span> <span data-ttu-id="f5bf2-118">Das Erstellen einer eindeutigen Instanz des-Objekts für jedes Formularfeld erfordert etwas mehr Arbeitsspeicher, wenn das Formular geladen wird.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-118">Creating a unique instance of the object for each form field requires slightly more memory when the form is loaded.</span></span> <span data-ttu-id="f5bf2-119">Es speichert jedoch das Verarbeiten von Fokus Ereignissen für die Felder, um dem aktuellen Feld zur Laufzeit eine einzelne Instanz zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-119">However, it saves having to handle focus events for the fields to assign a single instance to the current field at run time.</span></span>

<span data-ttu-id="f5bf2-120">Da das " [cuinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekt nur auf einem Tablet PC unterstützt wird, erstellt das Beispiel die "cuinputpanel"-Objekte innerhalb eines Ausnahme Behandlungs Blocks.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-120">Because the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is supported only on a Tablet PC, the sample creates the PenInputPanel objects within an exception-handling block.</span></span>

## <a name="one-object-per-field"></a><span data-ttu-id="f5bf2-121">Ein Objekt pro Feld</span><span class="sxs-lookup"><span data-stu-id="f5bf2-121">One Object per Field</span></span>

<span data-ttu-id="f5bf2-122">Das Beispiel veranschaulicht das erste Verfahren (ein " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekt pro Feld), indem die Eingabefelder für die Richtlinien Nummer ( `inkEdPolicyNumber` ) und der Versicherte Name ( `inkEdName` ) eine eindeutige Instanz des "pinputpanel"-Objekts zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-122">The sample demonstrates the first technique (one [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object per field) by assigning the input fields for policy number (`inkEdPolicyNumber`) and insured name (`inkEdName`) a unique instance of the PenInputPanel object.</span></span> <span data-ttu-id="f5bf2-123">Ein überladener Konstruktor für das Objekt "pinputpanel" kann den Namen des Eingabe Steuer Elements als Argument annehmen und somit die Steuerelemente zuordnen.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-123">An overloaded constructor for the PenInputPanel object can take the name of the input control as an argument, thus associating the controls.</span></span> <span data-ttu-id="f5bf2-124">Die folgenden Zeilen aus dem [Lade](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) Ereignishandler des Formulars zeigen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f5bf2-124">The following lines from the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler shows this:</span></span>


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a><span data-ttu-id="f5bf2-125">Ein Objekt pro Formular</span><span class="sxs-lookup"><span data-stu-id="f5bf2-125">One Object per Form</span></span>

<span data-ttu-id="f5bf2-126">Das zweite Verfahren ist auch im Beispiel dargestellt: eine einzelne Instanz eines " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekts, `pipShared` , wird zwischen den Eingabefeldern "Year", "Make" und "Model" gemeinsam genutzt.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-126">The second technique is also shown in the sample: a single instance of a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object, `pipShared`, is shared between the Year, Make, and Model input fields.</span></span> <span data-ttu-id="f5bf2-127">Das freigegebene Objekt wird mit dem Standardkonstruktor erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-127">The shared object is created by using the default constructor.</span></span>


```C++
pipShared = new PenInputPanel();
```



<span data-ttu-id="f5bf2-128">Wenn Sie dieses Verfahren verwenden, muss das Formular nur über eine einzelne Instanz [des Objekts "](/previous-versions/aa514041(v=msdn.10)) " "" "" "</span><span class="sxs-lookup"><span data-stu-id="f5bf2-128">Using this technique requires that your form have only a single instance of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span> <span data-ttu-id="f5bf2-129">Dadurch wird Arbeitsspeicher gespart, aber Sie müssen Code hinzufügen, um das Ereignis zu behandeln, wenn ein Eingabefeld den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-129">This saves memory, but you must add code to handle the event when an input field receives focus.</span></span> <span data-ttu-id="f5bf2-130">Wenn ein Steuerelement, das eine freigegebene Instanz eines "pinputpanel"-Objekts verwendet, den Fokus erhält, legen Sie die Eigenschaft " [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) " des Objekts "pinputpanel" auf diese Steuer</span><span class="sxs-lookup"><span data-stu-id="f5bf2-130">When a control that uses a shared instance of a PenInputPanel object gets focus, set the PenInputPanel object's [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) property to that control.</span></span> <span data-ttu-id="f5bf2-131">Der folgende Code zeigt einen Ereignishandler für die Ereignisse "Year", "Make" und "Model" `Enter` .</span><span class="sxs-lookup"><span data-stu-id="f5bf2-131">The following code shows an event handler for the Year, Make, and Model fields' `Enter` events.</span></span>


```C++
private void inkEdYear_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Year field
    pipShared.AttachedEditControl = inkEdYear;

    // set the NUMBER factoid to bias recognition for numbers
    pipShared.Factoid = "NUMBER";

    // Enable correction UI on the inkEdYear field
    pipShared.EnableTsf(true);
}

private void inkEdMake_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Make field
    pipShared.AttachedEditControl = inkEdMake;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdMake field
    pipShared.EnableTsf(true);
}
private void inkEdModel_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Model field
    pipShared.AttachedEditControl = inkEdModel;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdModel field
    pipShared.EnableTsf(true);
}
```



<span data-ttu-id="f5bf2-132">Stellen Sie sicher, dass Sie alle Eigenschaften festlegen, die festgelegt werden müssen, wenn Änderungen auf ein neues Steuerelement fokussiert werden.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-132">Be sure to set any properties that need to be set when focus changes to a new control.</span></span> <span data-ttu-id="f5bf2-133">In den vorherigen Ereignis Handlern wird z. b. die Eigenschaft " [Faktoid](/previous-versions/ms571978(v=vs.100)) " entsprechend festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-133">In the previous event handlers, for example, the [Factoid](/previous-versions/ms571978(v=vs.100)) property is set as appropriate.</span></span>

## <a name="usability-considerations"></a><span data-ttu-id="f5bf2-134">Nutzbarkeits Überlegungen</span><span class="sxs-lookup"><span data-stu-id="f5bf2-134">Usability Considerations</span></span>

<span data-ttu-id="f5bf2-135">Berücksichtigen Sie die folgenden Überlegungen zur Benutzerfreundlichkeit, wenn Sie das Objekt " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) " in Ihrer Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-135">Keep the following usability considerations in mind when using the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object in your application.</span></span>

### <a name="positioning-the-peninputpanel"></a><span data-ttu-id="f5bf2-136">Positionieren von "pinputpanel"</span><span class="sxs-lookup"><span data-stu-id="f5bf2-136">Positioning the PenInputPanel</span></span>

<span data-ttu-id="f5bf2-137">Da die Felder auf dem Formular in diesem Beispiel vertikal angeordnet werden, wird die Benutzeroberfläche des Benutzer Steuer Elements für jedes Eingabe Steuerelement leicht auf der rechten Seite des Eingabe Steuer Elements positioniert, [um die Verwendung](/previous-versions/aa514041(v=msdn.10)) zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-137">Because the fields are laid out vertically on the form in this sample, the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) user interface for each input control is positioned slightly to the right of the input control to make it easier to use.</span></span> <span data-ttu-id="f5bf2-138">Dadurch wird verhindert, dass das angriffpanel-Element das nächste Bearbeitungsfeld abdeckt, sodass das nächste Bearbeitungsfeld einfacher als Ziel ist.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-138">This prevents the PenInputPanel from covering up the next edit box, making it easier to target the next edit box.</span></span>


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a><span data-ttu-id="f5bf2-139">Auswählen des anzuzeigenden Eingabe Panels</span><span class="sxs-lookup"><span data-stu-id="f5bf2-139">Selecting Input Panel to Display</span></span>

<span data-ttu-id="f5bf2-140">Da Richtlinien Nummern häufig Kombinationen aus Zahlen, Buchstaben und anderen Zeichen darstellen, können Sie zu Erkennungs Fehlern neigen.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-140">Because policy numbers are often combinations of numbers, letters, and other characters, they can be prone to recognition errors.</span></span> <span data-ttu-id="f5bf2-141">Aus diesem Grund legt das Beispiel den Standardbereich fest, [der vom Objekt "](/previous-versions/aa514041(v=msdn.10)) -ID" als Tastatur angezeigt wird, wenn es an das Feld "Richtlinien Nummer" angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-141">Therefore, the sample sets the default panel displayed by the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to be the keyboard when it is attached to the policy number field.</span></span>


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



<span data-ttu-id="f5bf2-142">Das Standardverhalten des " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekts besteht darin, den Bereich zu verwenden, der vom Benutzer zuletzt ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-142">The default behavior of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is to use the panel the user selected last.</span></span>

### <a name="text-services-framework-correction-user-interface"></a><span data-ttu-id="f5bf2-143">Benutzeroberfläche für die Korrektur von Text Services Framework</span><span class="sxs-lookup"><span data-stu-id="f5bf2-143">Text Services Framework Correction User Interface</span></span>

<span data-ttu-id="f5bf2-144">In diesem Beispiel sind alle Eingabefelder [InkEdit](/previous-versions/ms552265(v=vs.100)) -Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-144">In this sample all of the input fields are [InkEdit](/previous-versions/ms552265(v=vs.100)) controls.</span></span> <span data-ttu-id="f5bf2-145">Dies ist wichtig, da das InkEdit-Steuerelement über eine integrierte Unterstützung für das [Text Services-Framework](../tsf/text-services-framework.md) (TSF) verfügt und daher in der Lage ist, die Benutzeroberfläche für die direkte Korrektur für Eingaben zu unterstützen, die vom Objekt " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) " empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-145">This is significant because the InkEdit control has built-in support for the [Text Services Framework](../tsf/text-services-framework.md) (TSF) and is thus capable of supporting the in-place correction user interface for input received from the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span>

<span data-ttu-id="f5bf2-146">Der Standardwert für [enabletsf](/previous-versions/ms569656(v=vs.100)) ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="f5bf2-146">The default value for [EnableTsf](/previous-versions/ms569656(v=vs.100)) is **TRUE**.</span></span> <span data-ttu-id="f5bf2-147">Dies bewirkt, dass das Objekt " [tzinputpanel](/previous-versions/aa514041(v=msdn.10)) " versucht, das Text Dienst Framework (TSF) im angefügten Steuerelement zu starten.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-147">This causes the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to attempt to start the Text Services Framework (TSF) on the attached control.</span></span> <span data-ttu-id="f5bf2-148">Bei erfolgreicher Ausführung zeigt die Benutzeroberfläche für Korrekturen im-Steuerelement an und ermöglicht den Zugriff auf Erkennungs Alternativen.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-148">If successful, the correction user interface shows in the control, and it allows access to recognition alternates.</span></span> <span data-ttu-id="f5bf2-149">Wenn Sie diese Methode mit einem **false** -Parameter aufrufen, wird TSF für das angefügte Steuerelement heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-149">Calling this method with a **FALSE** parameter attempts to shut down TSF on the attached control.</span></span>

<span data-ttu-id="f5bf2-150">Das [InkEdit](/previous-versions/ms552265(v=vs.100)) -Steuerelement stellt bereits eine Korrektur Benutzeroberfläche bereit, aber im Beispiel wird [enabletsf](/previous-versions/ms569656(v=vs.100)) verwendet, [um die Verwendung](/previous-versions/aa514041(v=msdn.10)) des TSF-einfügeerkennungskontexts anstelle der [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) -Funktion zu ermöglichen, um die Handschrift Erkennungsergebnisse an das Steuerelement zu senden.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-150">The [InkEdit](/previous-versions/ms552265(v=vs.100)) control already provides a correction user interface, but in the sample [EnableTsf](/previous-versions/ms569656(v=vs.100)) is used to enable the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) to use the TSF insertion recognizer context rather than the [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) function to send the handwriting recognition results into the control.</span></span> <span data-ttu-id="f5bf2-151">Das Ergebnis ist, dass Text eingefügt werden kann, auch wenn das Feld nicht mehr den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-151">The result is that text can be inserted even if the field no longer has focus.</span></span>


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a><span data-ttu-id="f5bf2-152">Schließen des Formulars</span><span class="sxs-lookup"><span data-stu-id="f5bf2-152">Closing the Form</span></span>

<span data-ttu-id="f5bf2-153">Im vom Windows Form-Designer generierten Code werden die Steuerelemente [InkEdit](/previous-versions/ms552265(v=vs.100)) und [InkPicture](/previous-versions/aa514604(v=msdn.10)) der Komponentenliste des Formulars hinzugefügt, wenn das Formular initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-153">In the Windows Form Designer generated code, the [InkEdit](/previous-versions/ms552265(v=vs.100)) and [InkPicture](/previous-versions/aa514604(v=msdn.10)) controls are added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="f5bf2-154">Wenn das Formular geschlossen wird, werden die InkEdit-und InkPicture-Steuerelemente sowie die anderen Komponenten des Formulars von der [verwerfen-Methode](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) des Formulars entfernt.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-154">When the form closes, the InkEdit and InkPicture controls are disposed, as well as the other components of the form, by the form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method.</span></span> <span data-ttu-id="f5bf2-155">Die verwerfen-Methode des Formulars gibt auch die frei [Hand Objekte frei, die für](/previous-versions/aa515768(v=msdn.10)) das Formular erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f5bf2-155">The form's Dispose method also disposes the [Ink](/previous-versions/aa515768(v=msdn.10)) objects that are created for the form.</span></span>

 

 
