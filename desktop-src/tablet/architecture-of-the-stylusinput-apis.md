---
description: Die StylusInput-APIs ermöglichen Ihnen die Interaktion mit dem Tablet Pen-Datenstrom. Wenn Sie mit dem Datenstrom interagieren möchten, fügen Sie der Anwendung ein RealTimeStylus-Objekt hinzu, und fügen Sie dem RealTimeStylus-Objekt Plug-Ins hinzu.
ms.assetid: 88bab0ab-df9f-4813-9a9f-9a137813f0b4
title: Architektur der StylusInput-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeda6a6a0269e8306aed6a6b6de4c1bbe33bc46f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131897"
---
# <a name="architecture-of-the-stylusinput-apis"></a>Architektur der StylusInput-APIs

Die StylusInput-APIs ermöglichen Ihnen die Interaktion mit dem Tablet Pen-Datenstrom. Wenn Sie mit dem Datenstrom interagieren möchten, fügen Sie der Anwendung ein [**RealTimeStylus**](realtimestylus-class.md) -Objekt hinzu, und fügen Sie dem **RealTimeStylus** -Objekt Plug-Ins hinzu.

In den StylusInput-APIs werden zwei Plug-ins bereitgestellt. Das [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekt implementiert die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -Schnittstelle. Das **DynamicRenderer** -Objekt rendert die frei Hand Eingaben in Echtzeit, während Sie gezeichnet werden. Das [**GestureRecognizer**](gesturerecognizer-class.md) -Objekt implementiert die **IStylusSyncPlugin** -Schnittstelle und die [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle. Das **GestureRecognizer** -Objekt erkennt Anwendungs Gesten.

## <a name="definitions"></a>Definitionen

Die folgenden Begriffe werden in den Abschnitten verwendet, in denen die StylusInput-APIs beschrieben werden:

Synchrones Plug-in

Eine Klasse, die die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -Schnittstelle implementiert. Synchrone Plug-ins werden im allgemeinen direkt durch das [**RealTimeStylus**](realtimestylus-class.md) -Objekt aufgerufen.

Asynchrones Plug-in

Eine Klasse, die die [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle implementiert. Asynchrone Plug-ins werden im Allgemeinen für den Benutzeroberflächen Thread der Anwendung aufgerufen.

Synchrone Plug-in-Sammlung

Eine [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) -Auflistung, bei der es sich um eine geordnete Auflistung von [IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10)) -Objekten handelt. Eine synchrone Plug-in-Auflistung bezieht sich in der Regel auf die Sammlung, die der [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) -Eigenschaft eines [RealTimeStylus](/previous-versions/ms824830(v=msdn.10)) -Objekts zugewiesen ist. Einer synchronen Plug-in-Sammlung können nur synchrone Plug-Ins hinzugefügt werden.

Asynchrone Plug-in-Sammlung

Eine [StylusAsyncPluginCollection](/previous-versions/ms824808(v=msdn.10)) -Auflistung, bei der es sich um eine geordnete Auflistung von [IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10)) -Objekten handelt. Eine asynchrone Plug-in-Auflistung verweist in der Regel auf die Sammlung, die der [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) -Eigenschaft eines [RealTimeStylus](/previous-versions/ms824830(v=msdn.10)) -Objekts zugewiesen ist. Der asynchronen Plug-in-Sammlung können nur asynchrone Plug-Ins hinzugefügt werden.

## <a name="synchronous-and-asynchronous-plug-ins"></a>Synchrone und asynchrone Plug-ins

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt ist darauf ausgelegt, Echtzeitzugriff auf den Datenstrom von einem Tablettstift aus bereitzustellen. Erstellen oder verwenden Sie synchrone Plug-Ins für Aufgaben, die Echtzeitzugriff auf den Datenstrom benötigen und Rechen mäßig nicht anspruchsvoll sind, z. b. für die Paketfilterung. Erstellen oder verwenden Sie asynchrone Plug-Ins für Aufgaben, die keinen Echtzeitzugriff auf den Datenstrom benötigen, z. b. zum Erstellen und Speichern von Strichen in einem [**InkDisp**](inkdisp-class.md) -Objekt.

Bestimmte Aufgaben sind möglicherweise Rechen anspruchsvoll und erfordern trotzdem Echtzeitzugriff auf den Datenstrom, wie z. b. die Erkennung von Zeitgeber-Gesten. Um diese Anforderungen zu erfüllen, stellen die StylusInput-APIs ein kaskadierenden [**RealTimeStylus**](realtimestylus-class.md) -Modell bereit, das es Ihnen ermöglicht, zwei **RealTimeStylus** -Objekte zu verwenden, die jeweils in einem eigenen Thread ausgeführt werden. Weitere Informationen zum kaskadierenden **RealTimeStylus** -Modell finden Sie [im kaskadierenden RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md).

Weitere Informationen zum verwenden und Erstellen von Plug-Ins finden Sie unter [Arbeiten mit den StylusInput-APIs](working-with-the-stylusinput-apis.md).

## <a name="the-tablet-pen-data-stream"></a>Der Tablet Pen-Datenstrom

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt verfügt über zwei interne Warteschlangen, die die Tablettstiftdaten, die Eingabe Warteschlange und die Ausgabe Warteschlange enthalten. Die Stift Daten werden in Instanzen der Klassen im [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) -Namespace konvertiert. In der folgenden Liste wird beschrieben, wie das **RealTimeStylus** -Objekt die Tablet Pen-Daten behandelt:

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt sucht zuerst in der Eingabe Warteschlange und dann aus dem Tablet Pen-Datenstrom nach Plug-in-Datenobjekten.

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt sendet ein Plug-in-Datenobjekt an die Objekte in seiner synchronen Plug-in-Auflistung. Jedes synchrone Plug-in kann Daten der Eingabe-oder Ausgabe Warteschlange hinzufügen.

Nachdem das Plug-in-Datenobjekt an alle Mitglieder der synchronen Plug-in-Auflistung gesendet wurde, wird das Plug-in-Datenobjekt in der Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts abgelegt.

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt überprüft dann, ob das nächste zu verarbeitende Plug-in-Datenobjekt verarbeitet werden soll.

Während die Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts Daten enthält, sendet das **RealTimeStylus** -Objekt ein Plug-in-Datenobjekt aus der Ausgabe Warteschlange an die Objekte in der asynchronen Plug-in-Auflistung. Jedes asynchrone Plug-in kann der Eingabe-oder Ausgabe Warteschlange Daten hinzufügen. Da die asynchronen Plug-ins jedoch im UI-Thread ausgeführt werden, werden die Daten in Bezug auf die aktuellen Pen-Daten, die das **RealTimeStylus** -Objekt verarbeitet, und nicht in Bezug auf die Daten, die das asynchrone Plug-in verarbeitet, der Warteschlange hinzugefügt.

Das folgende Diagramm veranschaulicht den Fluss von Tablet Pen-Daten durch das [**RealTimeStylus**](realtimestylus-class.md) -Objekt und seine Plug-in-Auflistungen.

![Fluss von Tablet Pen-Daten durch das RealTimeStylus-Objekt und seine Plug-in-Auflistungen](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

In diesem Diagramm stellen die Kreise mit den Bezeichnungen "A" und "B" Tablet Pen-Daten dar, die bereits der Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts hinzugefügt wurden und noch nicht an die asynchrone Plug-in-Auflistung gesendet wurden. Der Kreis mit der Bezeichnung "C" stellt die Tablet Pen-Daten dar, die das **RealTimeStylus** -Objekt gerade verarbeitet. Sie wird an die synchrone Plug-in-Auflistung gesendet und in der Ausgabe Warteschlange abgelegt. Der leere Kreis stellt die Position in der Ausgabe Warteschlange dar, an der zukünftige Tablet Pen-Daten hinzugefügt werden.

Weitere Informationen zur Art und Weise, wie bestimmte Daten der Warteschlange hinzugefügt und verarbeitet werden, finden Sie unter [Plug-in-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md).

## <a name="the-stylusinput-apis"></a>Die StylusInput-APIs

Die StylusInput-APIs befinden sich hauptsächlich in den Namespaces " [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10)) " und " [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) ". Die StylusInput-APIs verweisen jedoch auch auf einige Klassen im [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) -Namespace, wie z. b. die [Tablet](/previous-versions/ms827783(v=msdn.10)) -Klasse, die [TabletPropertyDescriptionCollection](/previous-versions/ms827760(v=msdn.10)) -Auflistung und die [applicationgesten](/previous-versions/ms827547(v=msdn.10)) -und [systemgesten](/previous-versions/ms827134(v=msdn.10)) -Enumerationen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))
</dt> <dt>

[**GestureRecognizer**](gesturerecognizer-class.md)
</dt> <dt>

[**RealTimeStylus**](realtimestylus-class.md)
</dt> <dt>

[**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[Arbeiten mit den StylusInput-APIs](working-with-the-stylusinput-apis.md)
</dt> <dt>

[Das Cascaded RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md)
</dt> </dl>

 

 
