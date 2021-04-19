---
description: Übersicht über die verwaltete Bibliothek und Hinweise zur Verwendung der von Tablet PC Platform verwalteten Bibliothek.
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: Verwenden der verwalteten Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1a1050705a6d74e6b183d04ec1c8f82d3954f0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106349754"
---
# <a name="using-the-managed-library"></a>Verwenden der verwalteten Bibliothek

Der Common Language Runtime ist die Grundlage des Microsoft .NET-Frameworks. Sie können sich den Common Language Runtime als einen Agent vorstellen, der Code zur Ausführungszeit verwaltet, Kerndienste wie Speicherverwaltung, Thread Verwaltung und Remoting bereitstellt und gleichzeitig eine strikte Code Sicherheit erzwingt. Tatsächlich ist das Konzept der Code Verwaltung ein grundlegendes Prinzip der Common Language Runtime. Code, der auf den Common Language Runtime abzielt, wird als verwalteter Code bezeichnet. Code, der nicht auf den Common Language Runtime ausgerichtet ist, wird als nativer Code bezeichnet.

Die Framework-Klassenbibliothek ist eine umfassende, objektorientierte Auflistung wiederverwendbarer Klassen, die Sie verwenden können, um Anwendungen zu entwickeln, die von herkömmlichen Befehlszeilen-oder grafischen Benutzeroberflächen Anwendungen (GUI) bis hin zu Anwendungen abhängig sind, die auf den neuesten Innovationen von ASP.net und Webdiensten basieren.

Die verwaltete Tablet PC-Bibliothek enthält eine Reihe verwalteter Objekte, die das Framework erweitern, um die Eingabe und Ausgabe der Handschrift auf Tablet PC sowie den Datenaustausch mit anderen Computern zu unterstützen.

## <a name="exceptions"></a>Ausnahmen

Die verwalteten Bibliotheksobjekte in der Tablet PC-API umschließen die Implementierungen der com-Bibliothek. Wenn das zugrunde liegende Objekt oder Steuerelement der com-Bibliothek einen Fehler zurückgibt, löst die verwaltete API eine Marshal. ThrowExceptionForHR-Ausnahme aus, die die Details der inneren com-Ausnahme bereitstellt. Weitere Informationen zu den möglichen Fehlern, die zurückgegeben werden können, finden Sie in der Referenz zu den HRESULT-Werten in der COM-Bibliotheks Referenz.

## <a name="object-comparison"></a>Objektvergleich

Für alle Objekte in der von Tablet PC Platform verwalteten Bibliothek wird gleich nicht außer Kraft gesetzt, um zwei gleich [**wertige**](/previous-versions/windows/) Objekte ordnungsgemäß zu vergleichen. Die verwaltete Anwendungsprogrammierschnittstelle (API) unterstützt nicht den Vergleich von Objekten auf Gleichheit, entweder über die **Gleichheits** Funktion oder über den Gleichheits Operator (= =).

## <a name="binding-to-the-latest-microsoftinkdll"></a>Binden an den neuesten Microsoft.Ink.dll

Die neueste Microsoft.Ink.dll Assembly ist ein kompatibles Ersatz für Microsoft.Ink.dll Version 1,0 und Microsoft.Ink.15.dll. In den meisten Fällen müssen Sie keine Änderungen an Ihren Anwendungen vornehmen, die mit den älteren Assemblys verteilt werden. In einigen Fällen müssen Sie jedoch das Common Language Runtime Lade Modul anweisen, die neuere Dynamic Link Library (dll) zu verwenden, wo immer auf die älteren DLLs verwiesen wird.

Das einzige Mal, dass Sie mithilfe der folgenden Vorgehensweise explizit an die neue Assembly binden müssen, ist, wenn Ihre Anwendung eine Komponente verwendet, die auf die Assembly der Version 1,0 oder 1,5 in Verbindung mit einer Komponente verweist, die auf eine neuere versionsassembly (z. b. 1,7) verweist, und wenn diese Komponenten Daten austauschen können.

Die beste Möglichkeit, den Common Language Runtime Loader anzuweisen, die neuere DLL zu verwenden, besteht darin, die Assemblyversionen auf Anwendungsebene umzuleiten. Sie können angeben, dass Ihre Anwendung die neuere Version der Assembly verwendet, indem Sie Assemblybindungsinformationen in die Konfigurationsdatei der Anwendung einfügen. Weitere Informationen zum Umleiten von Assemblyversionen auf Anwendungsebene finden Sie unter [umleiten](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue)von Assemblyversionen, insbesondere im Abschnitt "angeben der Assemblybindung in Konfigurationsdateien".

Sie müssen eine Konfigurationsdatei im gleichen Verzeichnis wie die ausführbare Datei erstellen. Die Konfigurationsdatei muss denselben Namen wie die ausführbare Datei aufweisen, gefolgt von der Dateierweiterung ". config". Beispielsweise muss für eine Anwendung MyApp.exe die Konfigurationsdatei die MyApp.exe.config Datei sein. Die Konfigurationsdatei verwendet ein [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) -Element, um zu erzwingen, dass alle früheren Versionen der aktuellen Version zugeordnet werden, wie im folgenden Beispiel gezeigt:

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

Weitere Informationen zu Konfigurationsdateien, einschließlich Beispielen zum Erstellen der Extensible Markup Language (XML) für die Konfigurationsdatei, finden Sie unter [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) und [umleiten](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue)von Assemblyversionen.

Anwendungen, die mit Microsoft Windows XP Tablet PC Edition Development Kit 1,7 und höheren Versionen erstellt wurden, werden automatisch an die neue Version der Microsoft. Ink-Assembly gebunden. Weitere Informationen zur Assemblybindung finden Sie [unter so](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp)sucht Common Language Runtime nach Assemblys.

> [!Note]  
> Die Verwendung der Anwendungs Richtlinie für die Bindung an die aktualisierte Assembly funktioniert nicht für Anwendungen, die die [Divider](/previous-versions/ms583616(v=vs.100)) - [Klasse oder die Klasse](/previous-versions/aa514041(v=msdn.10)) "-Klasse" verwenden. Anwendungen, die eine dieser Klassen verwenden, müssen entweder weiterhin Microsoft.Ink.15.dll verwenden oder nach Verweis auf die aktualisierte Assembly neu kompiliert werden.

 

## <a name="working-with-events"></a>Arbeiten mit Ereignissen

Wenn der Code in einem Ereignishandler für eines der verwalteten Objekte eine Ausnahme auslöst, wird die Ausnahme nicht an den Benutzer übermittelt. Um sicherzustellen, dass Ausnahmen übermittelt werden, verwenden Sie try-catch-Blöcke in ihren Ereignis Handlern für verwaltete Ereignisse.

## <a name="managing-forms"></a>Verwalten von Formularen

Die [Formular](/dotnet/api/system.windows.forms.form?view=netcore-3.1) Klasse und ihre Basisklassen definieren keinen Finalizer. Zum Bereinigen der Ressourcen in einem Formular schreiben Sie eine Unterklasse, die einen Finalizer (z. b. den C- \# debugtor mit ~) [bereitstellt,](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1)der "verwerfen" aufruft. Um die Bereinigung durchzuführen, überschreibt der Finalizer den Löschvorgang und ruft dann die-Basisklasse ab. Verweisen Sie nicht auf andere Objekte, die die [Finalize](/previous-versions/windows/) -Methode in der verwerfen-Methode benötigen, wenn der boolesche Parameter **false** ist, da diese Objekte möglicherweise bereits fertiggestellt wurden. Weitere Informationen zum Freigeben von Ressourcen finden Sie unter [Finalize-Methoden und-debugktoren](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).

## <a name="forms-and-the-recognizercontext"></a>Formulare und Erkennungs Kontext

[Erkenzercontext](/previous-versions/ms552546(v=vs.100)) -Ereignisse werden in einem anderen Thread als dem Thread ausgeführt, in dem sich das Formular befindet. Steuerelemente in Windows Forms sind an einen bestimmten Thread gebunden und sind nicht Thread sicher. Daher müssen Sie eine der Methoden zum Aufrufen des Steuer Elements verwenden, um den Aufruf an den richtigen Thread zu Mars Hallen. Vier Methoden in einem Steuerelement sind Thread sicher: die Methoden " [Aufruf](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1)", " [begincallback](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1)", " [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)" und " [forategraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) ". Verwenden Sie für alle anderen Methodenaufrufe eine dieser Aufruf Methoden, wenn Sie von einem anderen Thread aufrufen. Weitere Informationen zur Verwendung dieser Methoden finden Sie unter Bearbeiten [von Steuerelementen aus Threads](/previous-versions/757y83z4(v=vs.140)).

## <a name="waiting-for-events"></a>Warten auf Ereignisse

Die Tablet PC-Umgebung ist multithreaded. Verwenden Sie die [**cowaitformultiplehandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) -Funktion anstelle von anderen Wait-Methoden, um die Eingabe von com-aufrufen (Re-Entrant Component Object Model) in Ihr Multithread-Apartment (MTA) zuzulassen, während die Anwendung auf ein Ereignis wartet.

## <a name="using-ink-strokes-collections"></a>Verwenden von Ink-Auflistungen

Instanzen von [Striche](/previous-versions/ms552701(v=vs.100)) -Auflistungen, die von einem [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekt abgerufen werden, werden nicht in die Garbage Collection Um einen Speicher Verluste zu vermeiden, verwenden Sie jedes Mal, wenn Sie mit einer dieser Auflistungen arbeiten, die using-Anweisung, wie unten gezeigt.


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a>Verwerfen von verwalteten Objekten und Steuerelementen

Um einen Speicher Verluste zu vermeiden, müssen Sie explizit [die verwerfen](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) -Methode für ein Tablet PC-Objekt oder-Steuerelement, an das ein Ereignishandler angefügt wurde, abrufen, bevor das Objekt oder das Steuerelement den Gültigkeitsbereich verlässt.

Um die Leistung Ihrer Anwendung zu verbessern, müssen Sie die folgenden Objekte, Steuerelemente und Sammlungen manuell löschen, wenn Sie nicht mehr benötigt werden.

-   [Unter Teiler](/previous-versions/ms583616(v=vs.100))
-   [Freihand](/previous-versions/aa515768(v=msdn.10))
-   [InkCollector](/previous-versions/ms583683(v=vs.100))
-   [InkEdit](/previous-versions/ms552265(v=vs.100))
-   [InkOverlay](/previous-versions/ms552322(v=vs.100))
-   [InkPicture](/previous-versions/aa514604(v=msdn.10))
-   ["Pendel Panel"](/previous-versions/aa514041(v=msdn.10))
-   [Erkennungs Kontext](/previous-versions/ms552546(v=vs.100))
-   [Striche](/previous-versions/ms552701(v=vs.100))

Das folgende C- \# Beispiel veranschaulicht einige Szenarien, in [](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) denen die verwerfen-Methode verwendet wird.


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



 

 