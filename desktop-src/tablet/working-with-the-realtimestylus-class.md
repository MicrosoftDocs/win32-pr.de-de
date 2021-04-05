---
description: Die RealTimeStylus-Klasse ist Teil der StylusInput-APIs (Application Programming Interfaces). In den folgenden Abschnitten werden die wichtigsten Elemente der RealTimeStylus-Klasse und der StylusInput-APIs beschrieben.
ms.assetid: 6385c387-5b11-4719-a6ec-e0bebe875348
title: Arbeiten mit der RealTimeStylus-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 919c4de38cb0835996928c877ca4c42faf6a5f96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752432"
---
# <a name="working-with-the-realtimestylus-class"></a>Arbeiten mit der RealTimeStylus-Klasse

Die [**RealTimeStylus**](realtimestylus-class.md) -Klasse ist Teil der StylusInput-APIs (Application Programming Interfaces). In den folgenden Abschnitten werden die wichtigsten Elemente der **RealTimeStylus** -Klasse und der StylusInput-APIs beschrieben.

## <a name="instantiating-the-realtimestylus-class"></a>Instanziieren der RealTimeStylus-Klasse

Wenn Sie ein [**RealTimeStylus**](realtimestylus-class.md) -Objekt erstellen, können Sie es an ein Fenster Handle oder an ein Steuerelement anfügen. Das Anfügen des **RealTimeStylus** -Objekts an ein Fenster Handle erfordert zusätzliche Berechtigungen. Weitere Informationen zu diesen Berechtigungen finden Sie [unter Überlegungen zu partiellen Vertrauens Stellungen für die StylusInput-APIs](partial-trust-considerations-for-the-stylusinput-apis.md).

> [!Note]  
> Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt kann nicht an ein Fenster oder ein Steuerelement in einem anderen Prozess angefügt werden.

 

Wenn Sie den Standardkonstruktor verwenden, erstellen Sie ein [**RealTimeStylus**](realtimestylus-class.md) -Objekt, das nur Eingaben von einem anderen **RealTimeStylus** -Objekt akzeptieren kann. Weitere Informationen zum Verbinden von zwei **RealTimeStylus** -Objekten finden Sie [im Cascaded RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md).

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt implementiert die [iverwerfbare](/dotnet/api/system.idisposable) Schnittstelle.

## <a name="extending-the-realtimestylus-class"></a>Erweitern der RealTimeStylus-Klasse

Damit die Plug-ins mit dem Datenstrom vom Tablettstift interagieren können, verwaltet das [**RealTimeStylus**](realtimestylus-class.md) -Objekt zwei Plug-in-Auflistungen, auf die durch das [**getstylussyncplugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylussyncplugin) und die [**getstylusasyncplugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstylusasyncplugin) -Methoden in C++ und die Eigenschaften [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) und [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) in verwaltetem Code zugegriffen werden kann. Sie können ein Plug-in hinzufügen, indem Sie entweder die [**addstylussyncplugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylussyncplugin) -Methode oder die [**addstylusasyncplugin**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addstylusasyncplugin) -Methode der-Auflistung innerhalb der entsprechenden-Eigenschaft aufrufen. Weitere Informationen zum Erstellen und Verwenden von Plug-Ins finden Sie unter [Plug-ins und RealTimeStylus-Klasse](plug-ins-and-the-realtimestylus-class.md). Informationen zur Entscheidung, ob ein synchrones oder asynchrones Plug-in für eine bestimmte Aufgabe erstellt werden soll, finden Sie unter [Threading Überlegungen für die StylusInput-APIs](threading-considerations-for-the-stylusinput-apis.md) und [Leistungs Überlegungen für die StylusInput-APIs](performance-considerations-for-the-stylusinput-apis.md).

Synchrone Plug-Ins müssen die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -Schnittstelle implementieren, und asynchrone Plug-Ins müssen die [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle implementieren. Jedes Plug-in verfügt über die [**IStylusSyncPlugin. DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) -Eigenschaft oder die [**IStylusAsyncPlugin. DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) -Eigenschaft. Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt ruft nur die Benachrichtigungs Methoden des Plug-Ins für Methoden auf, die das Plug-in abonniert hat. Weitere Informationen zu den Benachrichtigungs Methoden finden Sie unter [Plug-in-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md).

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt implementiert die [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle. Die einzige Möglichkeit, ein **RealTimeStylus** -Objekt zu instanziieren, das Eingaben von einem anderen **RealTimeStylus** -Objekt akzeptiert, besteht darin, den Standardkonstruktor zu verwenden und das kaskadierenden **RealTimeStylus** -Modell zu implementieren. Weitere Informationen zum Verbinden von zwei **RealTimeStylus** -Objekten finden Sie [im Cascaded RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md).

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt verfügt über zwei interne Warteschlangen, die die Tablettstiftdaten, die Eingabe Warteschlange und die Ausgabe Warteschlange enthalten. Die Stift Daten werden in Instanzen der Klassen im [Microsoft. StylusInput. PluginData](/previous-versions/ms574862(v=vs.100)) -Namespace konvertiert. In der folgenden Liste wird beschrieben, wie das **RealTimeStylus** -Objekt die Tablet Pen-Daten behandelt.

1.  Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt sucht zuerst in der Eingabe Warteschlange und dann aus dem Tablet Pen-Datenstrom nach Plug-in-Datenobjekten.
2.  Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt sendet ein Plug-in-Datenobjekt an die Objekte in seiner synchronen Plug-in-Auflistung. Jedes synchrone Plug-in kann Daten der Eingabe-oder Ausgabe Warteschlange hinzufügen.
3.  Sobald das Plug-in-Datenobjekt an alle Elemente der synchronen Plug-in-Auflistung gesendet wurde, wird das Plug-in-Datenobjekt in der Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts abgelegt.
4.  Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt überprüft dann, ob das nächste zu verarbeitende Plug-in-Datenobjekt verarbeitet werden soll.
5.  Während die Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts Daten enthält, sendet das **RealTimeStylus** -Objekt ein Plug-in-Datenobjekt aus der Ausgabe Warteschlange an die Objekte in der asynchronen Plug-in-Auflistung. Jedes asynchrone Plug-in kann Daten der Eingabe-oder Ausgabe Warteschlange hinzufügen, aber da die asynchronen Plug-Ins auf dem Benutzeroberflächen Thread (UI) ausgeführt werden, werden die Daten in Bezug auf die aktuellen Stift Daten, die das **RealTimeStylus** -Objekt verarbeitet, der Warteschlange hinzugefügt.

Das folgende Diagramm veranschaulicht den Fluss von Tablet Pen-Daten durch das [**RealTimeStylus**](realtimestylus-class.md) -Objekt und seine Plug-in-Auflistungen.

![illustratiom mit Tablet PC-Pen-Datenfluss](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

In diesem Diagramm stellen die Kreise "A" und "B" Tablet Pen-Daten dar, die bereits der Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts hinzugefügt wurden und noch nicht an die asynchrone Plug-in-Auflistung gesendet wurden. Der Kreis mit dem Titel "C" stellt die Tablettstiftdaten dar, die das **RealTimeStylus** -Objekt gerade verarbeitet. Sie wird an die synchrone Plug-in-Auflistung gesendet und in der Ausgabe Warteschlange abgelegt. Der leere Kreis stellt die Position in der Ausgabe Warteschlange dar, an der zukünftige Tablet Pen-Daten hinzugefügt werden.

Weitere Informationen zur Art und Weise, wie bestimmte Daten der Warteschlange hinzugefügt und verarbeitet werden, finden Sie unter [Plug-in-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md).

Im folgenden finden Sie ein minimales Szenario für die Verwendung des [**RealTimeStylus**](realtimestylus-class.md) -Objekts in einem Formular, das frei Hand Eingaben sammelt.

1.  Erstellen Sie ein Formular, das die [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle implementiert.
2.  Erstellen Sie ein [**RealTimeStylus**](realtimestylus-class.md) -Objekt, das an ein Steuerelement im Formular angefügt ist.
3.  Legen Sie Interesse an den "StylusDown"-, "Pakete" und "StylusUp"-Benachrichtigungen in der [**IStylusAsyncPlugin. DataInterest**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-datainterest) -Eigenschaft des Formulars fest.
4.  Fügen Sie in den [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown)-,- [**Paketen**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)-und [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) -Methoden des Formulars Code hinzu, um die tablettstiftdown-, Pakete-und tablettstiftbenachrichtigungen zu verarbeiten, die aus dem [**RealTimeStylus**](realtimestylus-class.md) -Objekt des Formulars gesendet werden.

Ein Beispiel für eine solche Anwendung finden Sie im Beispiel für eine frei Hand [Sammlung in RealTimeStylus](realtimestylus-ink-collection-sample.md).

## <a name="working-with-tablet-objects"></a>Arbeiten mit Tablet-Objekten

Jedes aktivierte [**RealTimeStylus**](realtimestylus-class.md) -Objekt verwaltet eine Liste eindeutiger Bezeichner für die [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekte, mit denen er interagieren kann. Das **RealTimeStylus** -Objekt stellt zwei Methoden für die Übersetzung zwischen dem eindeutigen Bezeichner und dem **Tablet** -Objekt zur Verfügung: die [**GetTabletContextIdFromTablet**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletcontextidfromtablet) -Methode und die [**GetTabletFromTabletContextId**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-gettabletfromtabletcontextid) -Methode.

Das [TabletPropertyDescription](/previous-versions/ms827769(v=msdn.10)) -Objekt (in verwaltetem Code) enthält eine [packetpropertyid](/previous-versions/ms827780(v=msdn.10)) -Eigenschaft und eine [TabletPropertyMetrics](/previous-versions/ms827781(v=msdn.10)) -Struktur, die den Bereich, die Auflösung und die Einheiten der Eigenschaft für ein bestimmtes [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekt beschreibt. Die [**GetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription) -Methode des [**RealTimeStylus**](realtimestylus-class.md) -Objekts gibt ein Array von Global Unique Bezeichner (GUIDs) für die Paket Eigenschaften zurück, die das **RealTimeStylus** -Objekt an seine Plug-ins weiterleitet, wenn diese Paket Eigenschaften verfügbar sind. Um den Satz von Paket Eigenschaften zu ändern, die das **RealTimeStylus** -Objekt an seine Plug-ins übergibt, müssen Sie die [**SetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) -Methode des **RealTimeStylus** -Objekts aufrufen. Die [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) -Methode (in verwaltetem Code) des **RealTimeStylus** -Objekts übernimmt einen eindeutigen Tablet-Bezeichner und gibt eine Auflistung von [TabletPropertyDescription](/previous-versions/ms827760(v=msdn.10)) -Objekten zurück. Diese Paket Eigenschaften stellen die Teilmenge der Eigenschaften dar, die von dem Tablet unterstützt werden, das von der **GetDesiredPacketDescription** -Methode zurückgegeben wird.

Eine Liste der Standard-Paket Eigenschaften-GUIDs finden Sie unter der [packetpropertyguids-Konstanten](packetpropertyguids-constants.md) -Klasse.

## <a name="special-considerations"></a>Besondere Überlegungen

In der folgenden Liste werden andere Punkte beschrieben, die berücksichtigt werden müssen, wenn das [**RealTimeStylus**](realtimestylus-class.md) -Objekt mit einem [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekt verwendet wird.

-   Die [**SetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-setdesiredpacketdescription) -Methode kann nur aufgerufen werden, während das [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekt deaktiviert ist. Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt kann die Liste der gewünschten Paket Eigenschaften ändern. Daher müssen Sie nach dem Aufrufen der **SetDesiredPacketDescription** -Methode die [**GetDesiredPacketDescription**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getdesiredpacketdescription) -Methode aufrufen, um zu bestimmen, welche Paket Eigenschaften das **RealTimeStylus** -Objekt an seine Plug-ins weiterleiten kann. Ein Tablet unterstützt nur die Werte **X**, **Y** und **PacketStatus** für die [PacketProperty](packetproperty-guids.md). Daher muss Ihr Plug-in-Design möglicherweise den Empfang von weniger Paket Eigenschaften als gewünscht berücksichtigen.
-   Die [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) -Methode (für verwalteten Code) kann nur aufgerufen werden, während das [**RealTimeStylus**](realtimestylus-class.md) -Objekt aktiviert ist. Da eine Benachrichtigung an die Async-Plug-ins gesendet werden kann, nachdem das **RealTimeStylus** -Objekt deaktiviert wurde, müssen Sie möglicherweise die Informationen für die einzelnen [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekte zwischenspeichern. Die GetTabletPropertyDescriptionCollection-Methode gibt eine Liste der gewünschten Paket Eigenschaften zurück, die vom angegebenen Tablet unterstützt werden.
-   Wenn das [**RealTimeStylus**](realtimestylus-class.md) -Objekt aktiviert ist, empfängt jedes Plug-in einen-Befehl an seine [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) -Methode. Das in der Benachrichtigung weiter gegebene [realtimestylusenableddata](/previous-versions/ms824229(v=msdn.10)) -Objekt enthält eine Sammlung der Kontext Bezeichner für die verfügbaren Tablets zum Zeitpunkt der Aktivierung des **RealTimeStylus** -Objekts.
-   Wenn ein Tablet, das vom [**RealTimeStylus**](realtimestylus-class.md) -Objekt verwendet werden kann, zum Tablet PC hinzugefügt oder daraus entfernt wird, während das **RealTimeStylus** -Objekt aktiviert ist, benachrichtigt das **RealTimeStylus** -Objekt die Plug-ins, dass ein [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekt hinzugefügt oder entfernt wurde. Weitere Informationen finden Sie unter [Plug-in-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md).

## <a name="working-with-tablet-pens"></a>Arbeiten mit Tablet-stiften

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt übergibt Informationen über den Tablettstift an seine Plug-ins in einer Reihe von Benachrichtigungs Methoden. Informationen über den [Tablettstift](/previous-versions/ms824824(v=msdn.10)) werden durch ein tablettstiftobjekt dargestellt, das über die [**GetStyluses**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) -Methode abgerufen wird. Dieses Objekt ist eine Darstellung des Tablettstifts zu dem Zeitpunkt, zu dem die Daten gesammelt wurden. Da Plug-ins die Tablet Pen-Daten als Teil des Tablet Pen-Datenstroms empfangen, sollten die Plug-ins die Informationen im tablettstiftobjekt verwenden, anstatt den aktuellen Zustand eines bestimmten Tablet Stifts durch die [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Klasse zu überprüfen. Informationen zum Übertragen von Tablet Pen-und Tablet-Stift-Schaltflächen Daten an Plug-Ins finden Sie unter [Plug-in-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md).

Um ein [Array der tablettstiftobjekte zu](/previous-versions/ms824824(v=msdn.10)) erhalten, die seit der letzten Aktivierung des [**RealTimeStylus**](realtimestylus-class.md) -Objekts gefunden wurden, verwenden Sie die [**GetStyluses**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-getstyluses) -Methode des **RealTimeStylus** -Objekts.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft. Ink. Tablet](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms585724(v=vs.100))
</dt> <dt>

[Das Cascaded RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Überlegungen zur teilweisen Vertrauenswürdigkeit für die StylusInput-APIs](partial-trust-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Plug-In-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Threading Überlegungen für die StylusInput-APIs](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
