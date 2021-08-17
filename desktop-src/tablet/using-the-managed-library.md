---
description: Übersicht über die verwaltete Bibliothek und Hinweise zur Verwendung der verwalteten Bibliothek der Tablet PC-Plattform.
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: Verwenden der verwalteten Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1241787b680045d6c84b440717ced5426e4352d8c280ef58c1bb7f75c9fc66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449246"
---
# <a name="using-the-managed-library"></a>Verwenden der verwalteten Bibliothek

Die Common Language Runtime ist die Grundlage der Microsoft .NET Framework. Sie können sich die Common Language Runtime als Agent für die Verwaltung von Code zur Ausführungszeit und zum Bereitstellen von Kerndiensten wie Speicherverwaltung, Threadverwaltung und Remoting sowie zur Erzwingen strikter Codesicherheit denken. Tatsächlich ist das Konzept der Codeverwaltung ein grundlegendes Prinzip der Common Language Runtime. Code für die Common Language Runtime wird als verwalteter Code bezeichnet. Code, der nicht auf die Common Language Runtime abzielt, wird als nativer Code bezeichnet.

Die Framework-Klassenbibliothek ist eine umfassende, objektorientierte Sammlung wiederverwendbarer Klassen, die Sie verwenden können, um Anwendungen zu entwickeln, die von herkömmlichen Befehlszeilen- oder grafischen Benutzeroberflächenanwendungen (GUI) bis hin zu Anwendungen reichen, die auf den neuesten Innovationen von ASP.NET und Webdiensten basieren.

Die verwaltete Tablet PC-Bibliothek enthält eine Reihe verwalteter Objekte, die das Framework erweitern, um Unterstützung für die Eingabe und Ausgabe von Handschrift auf Dem Tablet PC sowie für den Datenaustausch mit anderen Computern zu bieten.

## <a name="exceptions"></a>Ausnahmen

Die verwalteten Bibliotheksobjekte in der Tablet PC-API umschließen die Implementierungen der COM-Bibliothek. Wenn das zugrunde liegende COM-Bibliotheksobjekt oder -Steuerelement einen Fehler zurückgibt, löst die verwaltete API eine Marshal.ThrowExceptionForHR-Ausnahme aus, die die Details zur inneren COM-Ausnahme enthält. Details zu möglichen Fehlern, die zurückgegeben werden können, finden Sie in der COM-Bibliotheksreferenz unter HRESULT-Werte.

## <a name="object-comparison"></a>Objektvergleich

Für alle Objekte in der von der Tablet PC-Plattform verwalteten Bibliothek wird [**Equals**](/previous-versions/windows/) nicht überschrieben, um zwei identische Objekte ordnungsgemäß zu vergleichen. Die verwaltete Anwendungsprogrammierschnittstelle (API) unterstützt weder über die **Equals-Funktion** noch über den Equals-Operator (==) den Vergleich von Objekten auf Gleichheit.

## <a name="binding-to-the-latest-microsoftinkdll"></a>Bindung an die neueste Microsoft.Ink.dll

Die neueste Microsoft.Ink.dll assembly ist ein kompatibler Ersatz für Microsoft.Ink.dll Version 1.0 und Microsoft.Ink.15.dll. In den meisten Fällen müssen Sie keine Änderungen an Ihren Anwendungen vornehmen, die mit den älteren Assemblys verteilt werden. In einigen Fällen müssen Sie jedoch das Common Language Runtime-Lademodul anweisen, die neuere DLL (Dynamic Link Library) überall dort zu verwenden, wo auf die älteren DLLs verwiesen wurde.

Sie müssen nur dann explizit eine Bindung an die neue Assembly mithilfe der folgenden Technik erstellen, wenn Ihre Anwendung eine Komponente verwendet, die auf die Assembly der Version 1.0 oder 1.5 in Kombination mit einer Komponente verweist, die auf eine neuere Versions-Assembly verweist, z.B. 1.7, und wenn diese Komponenten Möglicherweise Daten austauschen.

Die beste Möglichkeit, das Common Language Runtime-Lademodul anweisen, die neuere DLL zu verwenden, besteht in der Umleitung von Assemblyversionen auf Anwendungsebene. Sie können angeben, dass Ihre Anwendung die neuere Version der Assembly verwendet, indem Sie Assemblybindungsinformationen in der Konfigurationsdatei Ihrer Anwendung speichern. Weitere Informationen zum Umleiten von Assemblyversionen auf Anwendungsebene finden Sie unter [Umleiten](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue)von Assemblyversionen, insbesondere im Abschnitt "Angeben der Assemblybindung in Konfigurationsdateien".

Sie müssen eine Konfigurationsdatei im gleichen Verzeichnis wie die ausführbare Datei erstellen. Die Konfigurationsdatei muss den gleichen Namen wie die ausführbare Datei haben, gefolgt von der .config Dateierweiterung. Beispielsweise muss die Konfigurationsdatei für MyApp.exe Anwendung die MyApp.exe.config sein. Die Konfigurationsdatei verwendet ein [bindingRedirect-Element,](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) um zu erzwingen, dass alle früheren Versionen der neuesten Version zugeordnet werden, wie im folgenden Beispiel gezeigt:

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

Weitere Informationen zu Konfigurationsdateien, einschließlich Beispielen zum Erstellen des Extensible Markup Language (XML) für die Konfigurationsdatei, finden Sie unter [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) und [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).

Anwendungen, die mit Microsoft Windows XP Tablet PC Edition Development Kit 1.7 und höher erstellt wurden, werden automatisch an die neue Version der Microsoft.Ink-Assembly gebunden. Weitere Informationen zur Assemblybindung finden Sie unter [How the Runtime Locates Assemblies](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).

> [!Note]  
> Die Verwendung einer Anwendungsrichtlinie zum Binden an die aktualisierte Assembly funktioniert nicht für Anwendungen, die die [Divider-Klasse](/previous-versions/ms583616(v=vs.100)) oder die [PenInputPanel-Klasse](/previous-versions/aa514041(v=msdn.10)) verwenden. Anwendungen, die eine dieser Klassen verwenden, müssen entweder weiterhin Microsoft.Ink.15.dll oder nach dem Verweisen auf die aktualisierte Assembly neu kompiliert werden.

 

## <a name="working-with-events"></a>Arbeiten mit Ereignissen

Wenn der Code in einem Ereignishandler für eines der verwalteten Objekte eine Ausnahme auslöst, wird die Ausnahme nicht an den Benutzer übermittelt. Um sicherzustellen, dass Ausnahmen übermittelt werden, verwenden Sie try-catch-Blöcke in Ihren Ereignishandlern für verwaltete Ereignisse.

## <a name="managing-forms"></a>Verwalten von Formularen

Die [Form-Klasse](/dotnet/api/system.windows.forms.form?view=netcore-3.1) und ihre Basisklassen definieren keinen Finalizer. Um Ihre Ressourcen in einem Formular zu bereinigen, schreiben Sie eine Unterklasse, die einen Finalizer (z. B. den C-Destruktor mit ~) zur Verfügung stellt, der \# [Dispose aufruft.](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) Um die Bereinigung zu tun, überschreibt der Finalizer Dispose und ruft dann die Basisklasse Dispose auf. Verweisen Sie nicht auf andere Objekte, die die [Finalize-Methode](/previous-versions/windows/) in der Dispose-Methode erfordern, wenn der boolesche Parameter **FALSE** ist, da diese Objekte möglicherweise bereits finalisiert wurden. Weitere Informationen zum Freigeben von Ressourcen finden Sie unter [Finalize Methods and Destructors](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).

## <a name="forms-and-the-recognizercontext"></a>Formulare und recognizerContext

[RecognizerContext-Ereignisse](/previous-versions/ms552546(v=vs.100)) werden in einem anderen Thread als der Thread ausgeführt, in dem sich das Formular befindet. Steuerelemente in Windows Forms sind an einen bestimmten Thread gebunden und nicht threadsicher. Daher müssen Sie eine der Aufrufmethoden des Steuerelements verwenden, um den Aufruf an den richtigen Thread zu marshallen. Vier Methoden für ein Steuerelement sind threadsicher: die [Invoke-,](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) [BeginInvoke-,](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1) [EndInvoke-](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)und [CreateGraphics-Methoden.](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) Verwenden Sie für alle anderen Methodenaufrufe eine dieser Aufrufmethoden, wenn Sie von einem anderen Thread aufrufen. Weitere Informationen zur Verwendung dieser Methoden finden Sie unter [Manipulating Controls from Threads](/previous-versions/757y83z4(v=vs.140)).

## <a name="waiting-for-events"></a>Warten auf Ereignisse

Die Tablet PC-Umgebung ist multithreaded. Verwenden Sie die [**CoWaitForMultipleHandles-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) anstelle anderer Wartemethoden, um erneuten Eintritt in Component Object Model-Aufrufe (COM) zu ermöglichen, um ihr Multithread-Apartment (MTA) zu öffnen, während Ihre Anwendung auf ein Ereignis wartet.

## <a name="using-ink-strokes-collections"></a>Verwenden von Ink Strokes-Auflistungen

Instanzen von [Strokes-Auflistungen,](/previous-versions/ms552701(v=vs.100)) die von einem [Ink-Objekt](/previous-versions/aa515768(v=msdn.10)) erhalten werden, werden nicht von der Garbage Collection erfasst. Um einen Arbeitsspeicherverlust zu vermeiden, verwenden Sie bei jeder Arbeit mit einer dieser Sammlungen die Using-Anweisung, wie unten dargestellt.


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a>Entfernen von verwalteten Objekten und Steuerelementen

Um einen Speicherverlust zu vermeiden, müssen Sie die [Dispose-Methode](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) explizit für jedes Tablet PC-Objekt oder -Steuerelement aufrufen, an das ein Ereignishandler angefügt wurde, bevor das Objekt oder Steuerelement den Gültigkeitsbereich übergeht.

Um die Leistung Ihrer Anwendung zu verbessern, löschen Sie die folgenden Objekte, Steuerelemente und Sammlungen manuell, wenn sie nicht mehr benötigt werden.

-   [Teiler](/previous-versions/ms583616(v=vs.100))
-   [Freihand](/previous-versions/aa515768(v=msdn.10))
-   [Inkcollector](/previous-versions/ms583683(v=vs.100))
-   [Inkedit](/previous-versions/ms552265(v=vs.100))
-   [Inkoverlay](/previous-versions/ms552322(v=vs.100))
-   [Inkpicture](/previous-versions/aa514604(v=msdn.10))
-   [Peninputpanel](/previous-versions/aa514041(v=msdn.10))
-   [Recognizercontext](/previous-versions/ms552546(v=vs.100))
-   [Striche](/previous-versions/ms552701(v=vs.100))

Im folgenden \# C-Beispiel werden einige Szenarien veranschaulicht, in denen die [Dispose-Methode](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) verwendet wird.


```C++
// A field for a Divider object
private Microsoft.Ink.Divider theDivider;

// A method that creates a Divider object
public void CreateDivider()
{
    // Make sure any previous Divider object was disposed of.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
    // Create the Divider object.
    theDivider = new Microsoft.Ink.Divider();

    // The remainder of the method
}

// A method that disposes of the Divider object
public void DisposeDivider()
{
    // The remainder of the method

    // Dispose of the Divider object.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
}

// A method that uses a local PenInputPanel object.
public void UsePenInputPanel()
{
    // Create the PenInputPanel object.
    Microsoft.Ink.PenInputPanel thePenInputPanel =
        new Microsoft.Ink.PenInputPanel();

    // The remainder of the method

    // Dispose of the PenInputPanel object before exiting.
    thePenInputPanel.Dispose();
    thePenInputPanel = null;
}
```



 

 