---
description: Die folgenden Überlegungen zum Tablet PC-Threading gelten speziell für die verwaltete Bibliothek.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Überlegungen zum Threading verwalteter Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60908618fe3b566a552167f3448ee1d4269f9246c7b08f9bb1acf3269cf2ae77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031708"
---
# <a name="managed-library-threading-considerations"></a>Überlegungen zum Threading verwalteter Bibliotheken

Die folgenden Überlegungen zum Tablet PC-Threading gelten speziell für die verwaltete Bibliothek.

-   [Threadsicherheit](#thread-safety)
-   [STA- und MTA-Anwendungen](#sta-and-mta-applications)
-   [Windows Überlegungen zum Threading von Formularen](#windows-forms-threading-considerations)
-   [Überlegungen zur Zwischenablage](#clipboard-considerations)
-   [Ausnahmen in Ereignishandlern](#exceptions-within-event-handlers)
-   [Entfernen von Objekten und Steuerelementen](#disposing-objects-and-controls)
-   [StylusInput-APIs](#stylusinput-apis)

## <a name="thread-safety"></a>Thread-Safety

Die verwalteten Bibliotheksklassen der Tablet PC-Plattform sind im Allgemeinen nicht threadsicher. Die folgenden Auflistungen sind threadsicher auf Memberebene. Diese Auflistungen garantieren jedoch nicht, dass ein Enumerator geschützt ist, wenn ein anderer Thread gleichzeitig mit der Auflistung arbeitet:

-   [Cursorbuttons](/previous-versions/ms839506(v=msdn.10))
-   [Cursor](/previous-versions/ms839493(v=msdn.10))
-   [Divisionunits](/previous-versions/ms837954(v=msdn.10))
-   [Recognitionalternates](/previous-versions/ms830115(v=msdn.10))
-   [Erkennungen](/previous-versions/ms828520(v=msdn.10))
-   [Tablets](/previous-versions/ms827599(v=msdn.10))

## <a name="sta-and-mta-applications"></a>STA- und MTA-Anwendungen

Verwaltete Anwendungen, die mithilfe der in Microsoft Visual Studio .NET enthaltenen Assistenten erstellt wurden, sind standardmäßig Singlethread-Apartment (STA). Sie können das Apartment für Ihre Anwendung ändern, indem Sie den STA-Thread oder das MTA-Threadattribut (Multithreaded Apartment) auf dem Einstiegspunkt Ihrer Anwendung festlegen.

Wenn Ihre Anwendung in einem MTA ausgeführt wird, müssen Sie threadsicheren Code schreiben. Auf diese Weise können Sie jedoch bestimmte Leistungsprobleme bei der Ereignisbehandlung verbessern.

Weitere Informationen zum STA-Thread und den MTA-Threadattributen finden Sie unter [STAThreadAttribute-Klasse](/dotnet/api/system.stathreadattribute?view=netcore-3.1) und [MTAThreadAttribute-Klasse.](/dotnet/api/system.mtathreadattribute?view=netcore-3.1)

## <a name="windows-forms-threading-considerations"></a>Windows Überlegungen zum Threading von Formularen

Die [Steuerelemente InkPicture](/previous-versions/aa514604(v=msdn.10)) und [InkEdit](/previous-versions/ms552265(v=vs.100)) erweitern Windows Forms-Steuerelemente. Windows Formularsteuerelemente verwenden das STA-Modell (Singlethread-Apartment), da Windows Forms auf nativen Win32-Fenstern basieren, die grundsätzlich singlethreaded sind. In verwaltetem Code sollten Ink-Steuerelemente im gleichen Thread wie der Hauptthread für das Formular erstellt werden.

In einer STA-Anwendung werden bestimmte Ereignisse in einem anderen Thread als dem Benutzeroberflächenthread der Anwendung ausgeführt. Verwenden Sie beim Aufrufen eines Windows Forms-Objekts oder -Steuerelements, einschließlich der [Steuerelemente InkPicture](/previous-versions/aa514604(v=msdn.10)) und [InkEdit,](/previous-versions/ms552265(v=vs.100)) innerhalb eines Tablet PC-Ereignishandlers die geerbte [Control.Invoke-Methode](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) des Objekts oder Steuerelements. Die [InvokeRequired-Eigenschaft,](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) die von der Control-Klasse geerbt wurde, kann verwendet werden, um zu bestimmen, ob dies erforderlich ist.

Im folgenden Ereignishandler für das [Recognition-Ereignis](/previous-versions/ms829424(v=msdn.10)) wird beispielsweise die [InvokeRequired-Eigenschaft](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) getestet, und bei **TRUE** wird der Ereignishandler über den Benutzeroberflächenthread erneut aufgerufen.


```C++
void recoContext_Recognition(object sender, 
        RecognizerContextRecognitionEventArgs e)
{
    if (InvokeRequired)
    {
        Invoke( new RecognizerContextRecognitionEventHandler(  
                     recoContext_Recognition ),
                    new object[] { sender, e } );
        return;
    }
     // Use the recognition result here.
}
```



Wenn Sie ein [UserControl-Steuerelement](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) in einem Browser auf einerWebseite speichern (siehe [Websteuerelemente),](web-controls.md)wird es als STA-Anwendung ausgeführt. Für intelligente Clientanwendungen (siehe [No Touch Deployment](no-touch-deployment.md)) hat der Entwickler die vollständige Kontrolle über [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1). (Der Standardwert ist in der Regel STA, kann aber je nach CLR-Version MTA sein.) Informationen zu Threadingproblemen im Zusammenhang [**mit dem RealTimeStylus**](realtimestylus-class.md)finden Sie unter Überlegungen zum Threading für [die StylusInput-APIs.](threading-considerations-for-the-stylusinput-apis.md)

Weitere Informationen zum Aufrufen von Windows Forms aus einer MTA-Anwendung finden Sie unter [Beispiel für multithreaded Windows Forms-Steuerelement.](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71))

## <a name="clipboard-considerations"></a>Überlegungen zur Zwischenablage

Das [Zwischenablageobjekt](../dataxchg/clipboard.md) funktioniert nur über einen STA-Thread. Wenn Sie versuchen, aus einem Thread, der nicht STA ist, in die Zwischenablage zu kopieren oder aus ihr zu kopieren, erhalten Sie eine [ThreadStateException.](/previous-versions/windows/) Wenn Ihre Anwendung MTA ist, erstellen Sie einen STA-Thread, um die Methodenaufrufe der Zwischenablage und einige der anderen Aspekte der Benutzeroberfläche Ihrer Anwendung zu verarbeiten.

## <a name="exceptions-within-event-handlers"></a>Ausnahmen in Ereignishandlern

Ausnahmen können nicht innerhalb von Tablet PC-Ereignishandlern ausgelöst werden. Wenn beispielsweise ein Ereignishandler-Delegat für ein Tablet PC-Objekt oder eine Tablet PC-Sammlung über drei registrierte Handler verfügt und der erste handler eine Ausnahme auslöst, tritt die folgende Sequenz auf:

1.  Der erste Handler wird beendet.
2.  Die Ausnahme geht verloren.
3.  Die verbleibenden Handler werden nicht aufgerufen.

## <a name="disposing-objects-and-controls"></a>Entfernen von Objekten und Steuerelementen

Um einen Speicherverlust zu vermeiden, müssen Sie die [Dispose-Methode](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) explizit für jedes Tablet PC-Objekt oder -Steuerelement aufrufen, an das ein Ereignishandler angefügt wurde, bevor das Objekt oder Steuerelement den Gültigkeitsbereich übergeht.

Um die Leistung in Ihrer Anwendung zu verbessern, löschen Sie jedes Tablet PC-Objekt oder -Steuerelement manuell, das die [Dispose-Methode](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) implementiert, wenn das Objekt oder Steuerelement nicht mehr benötigt wird.

## <a name="stylusinput-apis"></a>StylusInput-APIs

Informationen zu Threadingüberlegungen für das [**RealTimeStylus-Objekt**](realtimestylus-class.md) und die Anwendungsprogrammierschnittstellen (APIs) von StylusInput finden Sie unter Überlegungen zum Threading für die [StylusInput-APIs.](threading-considerations-for-the-stylusinput-apis.md)

 

 
