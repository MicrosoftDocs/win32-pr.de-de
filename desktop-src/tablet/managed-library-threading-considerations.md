---
description: Die folgenden Überlegungen zum Tablet PC-Threading gelten speziell für die verwaltete Bibliothek.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Überlegungen zum Threading verwalteter Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8677375b8bbdb5f171329927d01e6178b5cb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362347"
---
# <a name="managed-library-threading-considerations"></a>Überlegungen zum Threading verwalteter Bibliotheken

Die folgenden Überlegungen zum Tablet PC-Threading gelten speziell für die verwaltete Bibliothek.

-   [Thread Sicherheit](#thread-safety)
-   [STA-und MTA-Anwendungen](#sta-and-mta-applications)
-   [Überlegungen zum Windows Forms Threading](#windows-forms-threading-considerations)
-   [Überlegungen Zwischenablage](#clipboard-considerations)
-   [Ausnahmen innerhalb von Ereignis Handlern](#exceptions-within-event-handlers)
-   [Verwerfen von Objekten und Steuerelementen](#disposing-objects-and-controls)
-   [StylusInput-APIs](#stylusinput-apis)

## <a name="thread-safety"></a>Thread-Safety

Die verwalteten Bibliotheks Klassen der Tablet PC-Plattform sind im Allgemeinen nicht Thread sicher. Die folgenden Auflistungen sind auf Element Ebene Thread sicher. Diese Auflistungen garantieren jedoch nicht, dass ein Enumerator geschützt ist, wenn ein anderer Thread gleichzeitig mit der Auflistung arbeitet:

-   [Cursor Buttons](/previous-versions/ms839506(v=msdn.10))
-   [Cursor](/previous-versions/ms839493(v=msdn.10))
-   [DivisionUnits](/previous-versions/ms837954(v=msdn.10))
-   [Erkennungs Alternativen](/previous-versions/ms830115(v=msdn.10))
-   [Erkennungen](/previous-versions/ms828520(v=msdn.10))
-   [Tablets](/previous-versions/ms827599(v=msdn.10))

## <a name="sta-and-mta-applications"></a>STA-und MTA-Anwendungen

Verwaltete Anwendungen, die mithilfe der in Microsoft Visual Studio .net enthaltenen Assistenten erstellt werden, sind standardmäßig Single Thread-Apartment (STA). Sie können das Apartment für Ihre Anwendung ändern, indem Sie das STA-Thread-oder Multithread-Apartment-Thread Attribut (MTA) auf dem Einstiegspunkt der Anwendung festlegen.

Wenn Ihre Anwendung in einem MTA ausgeführt wird, müssen Sie Thread sicheren Code schreiben. auf diese Weise können Sie jedoch bestimmte Leistungsprobleme bei der Ereignis Behandlung verbessern.

Weitere Informationen zu den STA-und MTA-Thread Attributen finden Sie unter " [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) Class" und " [mtathlesattribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) Class".

## <a name="windows-forms-threading-considerations"></a>Überlegungen zum Windows Forms Threading

Die Steuerelemente [InkPicture](/previous-versions/aa514604(v=msdn.10)) und [InkEdit](/previous-versions/ms552265(v=vs.100)) erweitern Windows Forms-Steuerelemente. Windows Forms Steuerelemente verwenden das STA-Modell (Single Thread-Apartment), da Windows Forms auf systemeigenen Win32-Fenstern basieren, die von Natur aus Single Thread sind. In verwaltetem Code sollten frei Hand Steuerelemente im gleichen Thread wie der Haupt Thread für das Formular erstellt werden.

In einer STA-Anwendung treten bestimmte Ereignisse in einem anderen Thread als dem Benutzeroberflächen Thread der Anwendung auf. Wenn Sie ein Windows Forms Objekt oder Steuerelement aufrufen, einschließlich der [InkPicture](/previous-versions/aa514604(v=msdn.10)) -und [InkEdit](/previous-versions/ms552265(v=vs.100)) -Steuerelemente, verwenden Sie in einem Tablet PC-Ereignishandler die geerbte [Control.](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) Call-Methode des-Objekts oder des-Steuer Elements. Die [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) -Eigenschaft, die von der Control-Klasse geerbt wurde, kann verwendet werden, um zu bestimmen, ob dies erforderlich ist.

Beispielsweise wird im folgenden Ereignishandler für das [Erkennungs](/previous-versions/ms829424(v=msdn.10)) Ereignis die [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) -Eigenschaft getestet, und wenn **true**, wird der Ereignishandler aus dem Benutzeroberflächen Thread erneut aufgerufen.


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



Wenn Sie ein [UserControl-Steuer](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) Element in einem Browser (siehe [websteuer Elemente](web-controls.md)) in awebpagein platzieren, wird es als STA-Anwendung ausgeführt. Für intelligente Client Anwendungen (siehe [keine Berührungs Bereitstellung](no-touch-deployment.md)) hat der Entwickler vollständige Kontrolle über den [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1). (Der Standardwert ist in der Regel STA, kann jedoch MTA sein, je nach Version der CLR.) Informationen zu Threading Problemen im Zusammenhang mit [**RealTimeStylus**](realtimestylus-class.md)finden Sie unter [Threading Überlegungen für die StylusInput-APIs](threading-considerations-for-the-stylusinput-apis.md).

Weitere Informationen zum Aufrufen von Windows Forms aus einer MTA-Anwendung finden Sie unter [Beispiel für Multithreaded Windows Forms Control](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).

## <a name="clipboard-considerations"></a>Überlegungen Zwischenablage

Das [Zwischenablage](../dataxchg/clipboard.md) Objekt funktioniert nur in einem STA-Thread. Wenn Sie versuchen, in einen Thread, der nicht STA ist, in die Zwischenablage zu kopieren oder aus der Zwischenablage einzufügen, erhalten Sie eine [ThreadStateException](/previous-versions/windows/). Wenn es sich bei der Anwendung um einen MTA handelt, erstellen Sie einen STA-Thread, um die Methodenaufrufe der Zwischenablage und einige andere Aspekte der Benutzeroberfläche Ihrer Anwendung zu verarbeiten.

## <a name="exceptions-within-event-handlers"></a>Ausnahmen innerhalb von Ereignis Handlern

Ausnahmen können nicht innerhalb von Tablet PC-Ereignis Handlern ausgelöst werden. Wenn z. b. ein Ereignishandlerdelegat für ein Tablet PC-Objekt oder eine Sammlung über drei registrierte Handler verfügt und der erste eine Ausnahme auslöst, wird die folgende Sequenz ausgeführt:

1.  Der erste Handler wird beendet.
2.  Die Ausnahme ist verloren gegangen.
3.  Die verbleibenden Handler werden nicht aufgerufen.

## <a name="disposing-objects-and-controls"></a>Verwerfen von Objekten und Steuerelementen

Um einen Speicher Verluste zu vermeiden, müssen Sie explizit [die verwerfen](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) -Methode für ein Tablet PC-Objekt oder-Steuerelement, an das ein Ereignishandler angefügt wurde, abrufen, bevor das Objekt oder das Steuerelement den Gültigkeitsbereich verlässt.

Um die Leistung in Ihrer Anwendung zu verbessern, löschen Sie alle Tablet PC-Objekte oder Steuerelemente, die die verwerfen [-Methode implementieren](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) , manuell, wenn das Objekt oder Steuerelement nicht mehr benötigt wird.

## <a name="stylusinput-apis"></a>StylusInput-APIs

Informationen zu Threading Überlegungen für das [**RealTimeStylus**](realtimestylus-class.md) -Objekt und die StylusInput-Anwendungs Programmierschnittstellen (APIs) finden Sie unter [Überlegungen zum Threading für die StylusInput-APIs](threading-considerations-for-the-stylusinput-apis.md).

 

 
