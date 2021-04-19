---
description: Das RealTimeStylus-Objekt dient zum Bereitstellen von Echtzeitzugriff auf den Datenstrom vom Tablettstift.
ms.assetid: 7217e2d5-ca62-4d65-bf22-9511b367c798
title: Plug-ins und die RealTimeStylus-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08177c5f4110897fa1887857788766f67ae38167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352750"
---
# <a name="plug-ins-and-the-realtimestylus-class"></a>Plug-ins und die RealTimeStylus-Klasse

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt dient zum Bereitstellen von Echtzeitzugriff auf den Datenstrom vom Tablettstift. Plug-ins, Objekte, die die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -oder [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle implementieren, können einem **RealTimeStylus** -Objekt hinzugefügt werden. Synchrone Plug-ins werden im allgemeinen direkt durch das **RealTimeStylus** -Objekt in einem Thread mit hoher Priorität aufgerufen, während asynchrone Plug-ins im Allgemeinen für den Benutzeroberflächen Thread der Anwendung aufgerufen werden. Erstellen oder verwenden Sie synchrone Plug-Ins für Aufgaben, die Echtzeitzugriff auf den Datenstrom benötigen und Rechen mäßig nicht anspruchsvoll sind (z. b. Paketfilterung). Erstellen oder verwenden Sie asynchrone Plug-Ins für Aufgaben, die keinen Echtzeitzugriff auf den Datenstrom benötigen, z. b. eine frei Hand Auflistung.

Bestimmte Aufgaben sind möglicherweise Rechen anspruchsvoll und erfordern trotzdem Echtzeitzugriff auf den Datenstrom, wie z. b. die Erkennung von Zeitgeber-Gesten. Um diese Anforderungen zu erfüllen, stellen die StylusInput-APIs ein kaskadierenden [**RealTimeStylus**](realtimestylus-class.md) -Modell bereit, das es Ihnen ermöglicht, zwei **RealTimeStylus** -Objekte zu verwenden, die jeweils in einem eigenen Thread ausgeführt werden. Weitere Informationen zum kaskadierenden **RealTimeStylus** -Modell finden Sie [im kaskadierenden RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md).

Sowohl die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -Schnittstelle als auch die [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle definieren die gleichen Methoden. Diese Methoden ermöglichen es dem [**RealTimeStylus**](realtimestylus-class.md) -Objekt, die Stift Daten an jedes Plug-in zu übergeben, unabhängig davon, ob es sich um ein asynchrones oder synchrones Plug-in handelt. Mit den Eigenschaften " [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) " und " [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) " können alle Plug-ins bestimmte Daten im Tablet Pen-Datenstream abonnieren. Ein Plug-in sollte nur die Daten abonnieren, die für die Ausführung der Aufgabe erforderlich sind, sodass Leistungsanforderungen minimiert werden. Weitere Informationen zum Threading und zur **RealTimeStylus** -Klasse finden Sie unter [Threading Überlegungen für die StylusInput-APIs](threading-considerations-for-the-stylusinput-apis.md).

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt verwendet Objekte im [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) -Namespace, um die Stift Daten an die Plug-ins zu übergeben. Der **RealTimeStylus** fängt auch Ausnahmen ab, die von Plug-ins ausgelöst werden. Wenn der **RealTimeStylus** Ausnahmen abfängt, werden die Plug-ins benachrichtigt, indem die [IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) -Methode oder die [IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) -Methode aufgerufen wird. Weitere Informationen zur Verwendung von Plug-in-Daten finden Sie unter [Plug-in-Daten und die RealTimeStylus-](plug-in-data-and-the-realtimestylus-class.md) Klasse. Weitere Informationen zur Fehlerbehandlung finden Sie unter [Überlegungen zur Fehlerbehandlung für die StylusInput-APIs](error-handling-considerations-for-the-stylusinput-apis.md) und im Abschnitt "Fehler Daten" der Plug-in-Daten und der RealTimeStylus-Klasse.

> [!Note]  
> Mindestens ein Plug-in muss an das [**RealTimeStylus**](realtimestylus-class.md) -Objekt angefügt werden, bevor das **RealTimeStylus** -Objekt aktiviert werden kann.

 

In den folgenden Themen werden einige allgemeine Kategorien von Plug-Ins beschrieben.

-   [Plug-Ins für die frei Hand Erfassung](ink-collection-plug-ins.md)
-   [Plug-Ins für dynamisches Renderer](dynamic-renderer-plug-ins.md)
-   [Erkennungs-Plug-ins](recognizer-plug-ins.md)

## <a name="special-considerations"></a>Besondere Überlegungen

Aufgrund der komplexen Natur des [**RealTimeStylus**](realtimestylus-class.md) -Objekts sollten Sie Folgendes beachten:

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt löst eine Ausnahme aus, wenn ein Plug-in die Plug-in-Sammlung ändert, an die es angefügt ist. Dies geschieht nur, wenn das Plug-in Dies bewirkt, während es vom **RealTimeStylus** -Objekt als Member dieser Auflistung aufgerufen wird.

Im folgenden C- \# Beispiel handelt es sich um Code, der bewirkt, dass das [**RealTimeStylus**](realtimestylus-class.md) -Objekt eine Ausnahme auslöst.


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.Dispose();
    }
    
    // ...
}
```



Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt löst eine Ausnahme aus, wenn ein Plug-in die verwerfen- [Methode des](/previous-versions/ms825891(v=msdn.10)) **RealTimeStylus** -Objekts aufruft. Dies geschieht nur, wenn das Plug-in Dies bewirkt, während es vom **RealTimeStylus** -Objekt aufgerufen wird.

Im folgenden C- \# Beispiel handelt es sich um Code, der bewirkt, dass das [**RealTimeStylus**](realtimestylus-class.md) -Objekt eine Ausnahme auslöst.


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    Microsoft.StylusInput.GestureRecognizer theGestureRecognizer;

    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.AsyncPluginCollection.Add(this.theGestureRecognizer);
    }
    
    // ...
}
```



Plug-in-Auflistungen können geändert werden, während das [**RealTimeStylus**](realtimestylus-class.md) -Objekt aktiviert ist. Dies kann jedoch die Vorhersage des Verhaltens ihrer Anwendung erschweren. Wenn ein Plug-in hinzugefügt wird, während das **RealTimeStylus** -Objekt aktiviert ist, ruft das **RealTimeStylus** -Objekt die [IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) -Methode oder die [IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) -Methode des Plug-Ins auf. Wenn ein Plug-in entfernt wird, während das **RealTimeStylus** -Objekt aktiviert ist, ruft das **RealTimeStylus** -Objekt die [IStylusAsyncPlugin. realtimestylusdeaktiviert](/previous-versions/ms824774(v=msdn.10)) -Methode oder die [IStylusSyncPlugin. realtimestylusdeaktiviert](/previous-versions/ms824757(v=msdn.10)) -Methode des Plug-Ins auf. Dadurch kann das Plug-in seinen ordnungsgemäßen Zustand beibehalten, ohne die [aktivierte](/previous-versions/ms824832(v=msdn.10)) Eigenschaft des **RealTimeStylus** -Objekts überprüfen zu müssen.

Wenn ein Plug-in hinzugefügt wird, während das [**RealTimeStylus**](realtimestylus-class.md) -Objekt aktiviert ist, enthalten die Plug-in-Daten, die das Plug-in empfängt, möglicherweise nicht genügend Informationen, um den Kontext der anfänglichen Daten adäquat festzulegen. Beispielsweise könnte das neu hinzugefügte Plug-in mit dem Empfang von Paketdaten von einem Stift beginnen, der einen Mittel Strich ist. Ebenso kann ein Plug-in, das beim Aktivieren des **RealTimeStylus** -Objekts entfernt wurde, nicht ausreichen, um die Verarbeitung der Daten abzuschließen.

> [!Note]  
> Setzen Sie für die Gesamtstabilität den internen Zustand eines Plug-ins zurück, wenn entweder die zugehörige [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) -Methode oder die [**realtimestylusdeaktivierte**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) -Methode aufgerufen wird.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Cascaded RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Überlegungen zur Fehlerbehandlung für die StylusInput-APIs](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Plug-In-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Threading Überlegungen für die StylusInput-APIs](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
