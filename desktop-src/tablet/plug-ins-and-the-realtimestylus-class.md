---
description: Das RealTimeStylus-Objekt ist so konzipiert, dass es Echtzeitzugriff auf den Datenstrom über den Tablettstift bietet.
ms.assetid: 7217e2d5-ca62-4d65-bf22-9511b367c798
title: Plug-Ins und die RealTimeStylus-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc522eb6f73b384d0c2c1846edb2b20cdcb89d34ef42633b08ca865950c8ce16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843380"
---
# <a name="plug-ins-and-the-realtimestylus-class"></a>Plug-Ins und die RealTimeStylus-Klasse

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) ist für den Echtzeitzugriff auf den Datenstrom über den Tablettstift konzipiert. Plug-Ins, Objekte, die die [**IStylusSyncPlugin-**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) oder [**IStylusAsyncPlugin-Schnittstelle**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) implementieren, können einem **RealTimeStylus-Objekt hinzugefügt** werden. Synchrone Plug-Ins werden im Allgemeinen direkt vom **RealTimeStylus-Objekt** in einem Thread mit hoher Priorität aufgerufen, während asynchrone Plug-Ins im Allgemeinen im Ui-Thread der Anwendung aufgerufen werden. Erstellen oder verwenden Sie synchrone Plug-Ins für Aufgaben, die Echtzeitzugriff auf den Datenstrom erfordern und berechnungsbasiertes Undemanding durchführen, z. B. Paketfilterung. Erstellen oder verwenden Sie asynchrone Plug-Ins für Aufgaben, die keinen Echtzeitzugriff auf den Datenstrom erfordern, z. B. die Sammlung von Ink-Daten.

Bestimmte Aufgaben können rechenintensiv sein, erfordern jedoch Echtzeitzugriff auf den Datenstrom, z. B. die Erkennung von Multistrokegesten. Um diese Anforderungen zu erfüllen, bieten die StylusInput-APIs ein kaskadiertes [**RealTimeStylus-Modell,**](realtimestylus-class.md) mit dem Sie zwei **RealTimeStylus-Objekte** verwenden können, die jeweils in einem eigenen Thread ausgeführt werden. Weitere Informationen zum kaskadierten **RealTimeStylus-Modell** finden Sie unter [Das kaskadierte RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md).

Sowohl die [**Schnittstellen IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) als auch [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) definieren die gleichen Methoden. Mit diesen Methoden kann das [**RealTimeStylus-Objekt**](realtimestylus-class.md) die Stiftdaten an jedes Plug-In übergeben, unabhängig davon, ob es sich um ein asynchrones oder synchrones Plug-In handelt. Mit den [Eigenschaften Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) und [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) kann jedes Plug-In bestimmte Daten im Tablettstiftdatenstrom abonnieren. Ein Plug-In sollte nur die Daten abonnieren, die zum Ausführen seiner Aufgabe erforderlich sind, wodurch die Leistungsanforderungen minimiert werden. Weitere Informationen zum Threading und zur **RealTimeStylus-Klasse** finden Sie unter Überlegungen zum Threading für [die StylusInput-APIs.](threading-considerations-for-the-stylusinput-apis.md)

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) verwendet Objekte im [Microsoft.StylusInput.PluginData-Namespace,](/previous-versions/ms823992(v=msdn.10)) um die Stiftdaten an die Plug-Ins zu übergeben. Der **RealTimeStylus fängt** auch Ausnahmen ab, die von Plug-Ins ausgelöst werden. Wenn **RealTimeStylus Ausnahmen** abfängt, benachrichtigt er die Plug-Ins durch Aufrufen der [IStylusSyncPlugin.Error-](/previous-versions/ms824754(v=msdn.10)) oder [IStylusAsyncPlugin.Error-Methode.](/previous-versions/ms824771(v=msdn.10)) Weitere Informationen zur Verwendung von Plug-In-Daten finden Sie unter [Plug-In-Daten und die RealTimeStylus-Klasse.](plug-in-data-and-the-realtimestylus-class.md) Weitere Informationen zur Fehlerbehandlung finden Sie unter Überlegungen zur Fehlerbehandlung für die [StylusInput-APIs](error-handling-considerations-for-the-stylusinput-apis.md) und im Abschnitt Fehlerdaten von Plug-In-Daten und der RealTimeStylus-Klasse.

> [!Note]  
> Mindestens ein Plug-In muss an das [**RealTimeStylus-Objekt**](realtimestylus-class.md) angefügt werden, bevor das **RealTimeStylus-Objekt** aktiviert werden kann.

 

In den folgenden Themen werden einige allgemeine Kategorien von Plug-Ins beschrieben.

-   [Ink-Collection-Plug-Ins](ink-collection-plug-ins.md)
-   [Dynamic-Renderer-Plug-Ins](dynamic-renderer-plug-ins.md)
-   [Erkennen von Plug-Ins](recognizer-plug-ins.md)

## <a name="special-considerations"></a>Besondere Überlegungen

Aufgrund der Komplexität des [**RealTimeStylus-Objekts**](realtimestylus-class.md) sollten Sie Folgendes beachten.

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) löst eine Ausnahme aus, wenn ein Plug-In die Plug-In-Auflistung ändert, an die es angefügt ist. Dies geschieht nur, wenn das Plug-In dies tut, während es vom **RealTimeStylus-Objekt** als Member dieser Auflistung aufgerufen wird.

Das folgende \# C-Beispiel ist Code, der bewirkt, dass das [**RealTimeStylus-Objekt**](realtimestylus-class.md) eine Ausnahme auslöst.


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



Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) löst eine Ausnahme aus, wenn ein Plug-In die Dispose-Methode des **RealTimeStylus-Objekts** aufruft. [](/previous-versions/ms825891(v=msdn.10)) Dies geschieht nur, wenn das Plug-In dies tut, während es vom **RealTimeStylus-Objekt aufgerufen** wird.

Das folgende \# C-Beispiel ist Code, der bewirkt, dass das [**RealTimeStylus-Objekt**](realtimestylus-class.md) eine Ausnahme auslöst.


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



Plug-In-Sammlungen können geändert werden, während das [**RealTimeStylus-Objekt**](realtimestylus-class.md) aktiviert ist. Dies kann jedoch die Vorhersage des Verhaltens Ihrer Anwendung erschweren. Wenn ein Plug-In hinzugefügt wird, während das **RealTimeStylus-Objekt** aktiviert ist, ruft das **RealTimeStylus-Objekt** die [IStylusAsyncPlugin.RealTimeStylusEnabled-](/previous-versions/ms824775(v=msdn.10)) oder [IStylusSyncPlugin.RealTimeStylusEnabled-Methode](/previous-versions/ms824758(v=msdn.10)) des Plug-Ins auf. Wenn ein Plug-In entfernt wird, während das **RealTimeStylus-Objekt** aktiviert ist, ruft das **RealTimeStylus-Objekt** die [IStylusAsyncPlugin.RealTimeStylusDisabled-](/previous-versions/ms824774(v=msdn.10)) oder [IStylusSyncPlugin.RealTimeStylusDisabled-Methode](/previous-versions/ms824757(v=msdn.10)) des Plug-Ins auf. Dadurch kann das Plug-In seinen richtigen Zustand erhalten, ohne die [Enabled-Eigenschaft](/previous-versions/ms824832(v=msdn.10)) des **RealTimeStylus-Objekts überprüfen zu** müssen.

Wenn ein Plug-In hinzugefügt wird, während das [**RealTimeStylus-Objekt**](realtimestylus-class.md) aktiviert ist, enthalten die plug-in-Daten, die das Plug-In empfängt, möglicherweise nicht genügend Informationen, um den Kontext der ursprünglichen Daten angemessen zu erstellen. Das neu hinzugefügte Plug-In könnte z. B. beginnen, Paketdaten von einem Stift mit Strichmitte zu empfangen. Wenn ein Plug-In entfernt wird, während das **RealTimeStylus-Objekt** aktiviert ist, sind die vom Plug-In empfangenen Plug-In-Daten möglicherweise nicht ausreichend, um die Verarbeitung der Daten fertig zu stellen.

> [!Note]  
> Setzen Sie den internen Zustand eines Plug-Ins zurück, wenn entweder seine [**RealTimeStylusEnabled-**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) oder [**RealTimeStylusDisabled-Methode**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) aufgerufen wird.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das kaskadierte RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Überlegungen zur Fehlerbehandlung für die StylusInput-APIs](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Plug-In-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Überlegungen zum Threading für die StylusInput-APIs](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
