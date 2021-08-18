---
description: Mit den StylusInput-APIs können Sie mit dem Datenstrom des Tablettstifts interagieren. Um mit dem Datenstrom zu interagieren, fügen Sie Ihrer Anwendung ein RealTimeStylus-Objekt und dem RealTimeStylus-Objekt Plug-Ins hinzu.
ms.assetid: 88bab0ab-df9f-4813-9a9f-9a137813f0b4
title: Architektur der StylusInput-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 961d6e3e94d47054afb28948685fce5fe1cafe9cbb0fa2f36e5a2d8508f28b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093158"
---
# <a name="architecture-of-the-stylusinput-apis"></a>Architektur der StylusInput-APIs

Mit den StylusInput-APIs können Sie mit dem Datenstrom des Tablettstifts interagieren. Um mit dem Datenstrom zu interagieren, fügen Sie Ihrer Anwendung ein [**RealTimeStylus-Objekt**](realtimestylus-class.md) und dem **RealTimeStylus-Objekt** Plug-Ins hinzu.

In den StylusInput-APIs werden zwei Plug-Ins bereitgestellt. Das [**DynamicRenderer-Objekt**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) implementiert die [**IStylusSyncPlugin-Schnittstelle.**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) Das **DynamicRenderer-Objekt** rendert die Ink in Echtzeit, während sie gezeichnet wird. Das [**GestureRecognizer-Objekt**](gesturerecognizer-class.md) implementiert die **Schnittstellen IStylusSyncPlugin** und [**IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) Das **GestureRecognizer-Objekt** erkennt Anwendungsgesten.

## <a name="definitions"></a>Definitionen

Die folgenden Begriffe werden in den Abschnitten verwendet, in denen die StylusInput-APIs beschrieben werden:

Synchrones Plug-In

Eine Klasse, die die [**IStylusSyncPlugin-Schnittstelle**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) implementiert. Synchrone Plug-Ins werden im Allgemeinen direkt vom [**RealTimeStylus-Objekt**](realtimestylus-class.md) aufgerufen.

Asynchrones Plug-In

Eine Klasse, die die [**IStylusAsyncPlugin-Schnittstelle**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) implementiert. Asynchrone Plug-Ins werden im Allgemeinen für den Benutzeroberflächenthread der Anwendung aufgerufen.

Synchrone Plug-In-Sammlung

Eine [StylusSyncPluginCollection-Sammlung,](/previous-versions/ms824788(v=msdn.10)) bei der es sich um eine geordnete Sammlung von [IStylusSyncPlugin-Objekten](/previous-versions/ms824751(v=msdn.10)) handelt. Eine synchrone Plug-In-Sammlung bezieht sich in der Regel auf die Sammlung, die der [SyncPluginCollection-Eigenschaft](/previous-versions/ms824833(v=msdn.10)) eines [RealTimeStylus-Objekts zugewiesen](/previous-versions/ms824830(v=msdn.10)) ist. Nur synchrone Plug-Ins können einer synchronen Plug-In-Auflistung hinzugefügt werden.

Asynchrone Plug-In-Auflistung

Eine [StylusAsyncPluginCollection-Auflistung,](/previous-versions/ms824808(v=msdn.10)) bei der es sich um eine geordnete Sammlung von [IStylusAsyncPlugin-Objekten](/previous-versions/ms824768(v=msdn.10)) handelt. Eine asynchrone Plug-In-Auflistung bezieht sich in der Regel auf die Sammlung, die der [AsyncPluginCollection-Eigenschaft](/previous-versions/ms824831(v=msdn.10)) eines [RealTimeStylus-Objekts zugewiesen](/previous-versions/ms824830(v=msdn.10)) ist. Einer asynchronen Plug-In-Auflistung können nur asynchrone Plug-Ins hinzugefügt werden.

## <a name="synchronous-and-asynchronous-plug-ins"></a>Synchrone und asynchrone Plug-Ins

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) ist für den Echtzeitzugriff auf den Datenstrom über einen Tablettstift konzipiert. Erstellen oder verwenden Sie synchrone Plug-Ins für Aufgaben, die Echtzeitzugriff auf den Datenstrom erfordern und berechnungsbasiertes Undemanding durchführen, z. B. für die Paketfilterung. Erstellen oder verwenden Sie asynchrone Plug-Ins für Aufgaben, die keinen Echtzeitzugriff auf den Datenstrom erfordern, z. B. zum Erstellen und Speichern von Strichen in einem [**InkDisp-Objekt.**](inkdisp-class.md)

Bestimmte Aufgaben können rechenintensiv sein, erfordern jedoch Echtzeitzugriff auf den Datenstrom, z. B. die Erkennung von Multistrokegesten. Um diese Anforderungen zu erfüllen, bieten die StylusInput-APIs ein kaskadiertes [**RealTimeStylus-Modell,**](realtimestylus-class.md) mit dem Sie zwei **RealTimeStylus-Objekte** verwenden können, die jeweils in einem eigenen Thread ausgeführt werden. Weitere Informationen zum kaskadierten **RealTimeStylus-Modell** finden Sie unter [Das kaskadierte RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md).

Weitere Informationen zum Verwenden und Erstellen von Plug-Ins finden Sie unter Arbeiten mit den [StylusInput-APIs.](working-with-the-stylusinput-apis.md)

## <a name="the-tablet-pen-data-stream"></a>Der Tablettstift-Datenstrom

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) verfügt über zwei interne Warteschlangen, die die Tablettstiftdaten, die Eingabewarteschlange und die Ausgabewarteschlange, tragen. Die Stiftdaten werden in Instanzen der Klassen im [Microsoft.StylusInput.PluginData-Namespace](/previous-versions/ms823992(v=msdn.10)) konvertiert. In der folgenden Liste wird beschrieben, wie das **RealTimeStylus-Objekt** die Tablettstiftdaten behandelt:

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) sucht zuerst in der Eingabewarteschlange nach Plug-In-Datenobjekten und anschließend aus dem Datenstrom des Tablettstifts.

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) sendet ein Plug-In-Datenobjekt an die Objekte in seiner synchronen Plug-In-Auflistung. Jedes synchrone Plug-In kann der Eingabe- oder Ausgabewarteschlange Daten hinzufügen.

Nachdem das Plug-In-Datenobjekt an alle Member der synchronen Plug-In-Sammlung gesendet wurde, wird das Plug-In-Datenobjekt in der Ausgabewarteschlange des [**RealTimeStylus-Objekts**](realtimestylus-class.md) platziert.

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) sucht dann nach dem nächsten zu verarbeitenden Plug-In-Datenobjekt.

Während die Ausgabewarteschlange des [**RealTimeStylus-Objekts**](realtimestylus-class.md) Daten enthält, sendet das **RealTimeStylus-Objekt** ein Plug-In-Datenobjekt aus seiner Ausgabewarteschlange an die Objekte in seiner asynchronen Plug-In-Auflistung. Jedes asynchrone Plug-In kann der Eingabe- oder Ausgabewarteschlange Daten hinzufügen. Da die asynchronen Plug-Ins jedoch im UI-Thread ausgeführt werden, werden die Daten der Warteschlange in Bezug auf die aktuellen Stiftdaten hinzugefügt, die das **RealTimeStylus-Objekt** verarbeitet, und nicht in Bezug auf die Daten, die das asynchrone Plug-In verarbeitet.

Das folgende Diagramm veranschaulicht den Fluss von Tablettstiftdaten durch das [**RealTimeStylus-Objekt**](realtimestylus-class.md) und seine Plug-In-Sammlungen.

![Fluss von Tablettstiftdaten durch das Realtimestylus-Objekt und seine Plug-In-Sammlungen](images/5a698bc9-833b-4b24-9fa2-70be0ca61032.gif)

In diesem Diagramm stellen die Kreise mit den Bezeichnungen "A" und "B" Tablettstiftdaten dar, die der Ausgabewarteschlange des [**RealTimeStylus-Objekts**](realtimestylus-class.md) bereits hinzugefügt wurden und noch nicht an die asynchrone Plug-In-Sammlung gesendet wurden. Der Kreis mit der Bezeichnung "C" stellt die Tablettstiftdaten dar, die das **RealTimeStylus-Objekt** derzeit verarbeitet. Sie wird an die synchrone Plug-In-Sammlung gesendet und in der Ausgabewarteschlange platziert. Der leere Kreis stellt die Position in der Ausgabewarteschlange dar, an der zukünftige Tablettstiftdaten hinzugefügt werden.

Weitere Informationen dazu, wie bestimmte Daten der Warteschlange hinzugefügt und verarbeitet werden, finden Sie unter [Plug-In-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md).

## <a name="the-stylusinput-apis"></a>Die StylusInput-APIs

Die StylusInput-APIs befinden sich hauptsächlich in den [Namespaces Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)) und [Microsoft.StylusInput.PluginData.](/previous-versions/ms823992(v=msdn.10)) Die StylusInput-APIs verweisen jedoch auch auf einige Klassen im [Microsoft.Ink-Namespace, z.](/previous-versions/ms826516(v=msdn.10)) B. die [Tablet-Klasse,](/previous-versions/ms827783(v=msdn.10)) die [TabletPropertyDescriptionCollection-Auflistung](/previous-versions/ms827760(v=msdn.10)) und die [ApplicationGesture-](/previous-versions/ms827547(v=msdn.10)) und [SystemGesture-Enumerationen.](/previous-versions/ms827134(v=msdn.10))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))
</dt> <dt>

[**GestureRecognizer**](gesturerecognizer-class.md)
</dt> <dt>

[**Realtimestylus**](realtimestylus-class.md)
</dt> <dt>

[**Istylusasyncplugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**Istylussyncplugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[Arbeiten mit den StylusInput-APIs](working-with-the-stylusinput-apis.md)
</dt> <dt>

[Das kaskadierte RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md)
</dt> </dl>

 

 
