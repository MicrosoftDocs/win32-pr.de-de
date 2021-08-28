---
description: Plug-Ins für die RealTimeStylus-Klasse müssen die Schnittstelle IStylusSyncPlugin oder IStylusAsyncPlugin oder beides implementieren.
ms.assetid: 827ac817-e0e6-4750-9d48-b939ccd5e679
title: Plug-In-Daten und die RealTimeStylus-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0540d90f291acfef27a09df08ffff645c280d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480966"
---
# <a name="plug-in-data-and-the-realtimestylus-class"></a>Plug-In-Daten und die RealTimeStylus-Klasse

Plug-Ins für die [**RealTimeStylus-Klasse**](realtimestylus-class.md) müssen die [**Schnittstelle IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) oder [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) oder beides implementieren. Sie müssen zwar alle Plug-In-Schnittstellenmethoden implementieren, ihr Plug-In empfängt jedoch nur Aufrufe von Methoden, die in der [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest-](/previous-versions/ms574887(v=vs.100)) oder [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest-Eigenschaft](/previous-versions/ms574886(v=vs.100)) gekennzeichnet sind.

Die für die Schnittstellen definierten Methoden verwenden Objekte im [Namespace Microsoft.StylusInput.PluginData,](/previous-versions/ms823992(v=msdn.10)) um die Stiftdaten an die Plug-Ins zu übergeben. Die folgende Tabelle beschreibt die Datenobjekte, die Parameter in den Benachrichtigungsmethoden sind, und listet den [DataInterestMask-Wert](/previous-versions/ms824787(v=msdn.10)) auf, der der Benachrichtigung zugeordnet ist.



| Plug-In-Daten                                                                                          | DataInterestMask-Wert     | BESCHREIBUNG                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Customstylusdata](/previous-versions/ms824747(v=msdn.10))                     | **CustomStylusDataAdded**  | Benutzerdefinierte Anwendungsdaten, die ein Plug-In hinzufügt.<br/>                                                                                                                                                                                                 |
| [Errordata](/previous-versions/ms824740(v=msdn.10))                                   | **Fehler**                  | Fehlerinformationen, die das [**RealTimeStylus-Objekt**](realtimestylus-class.md) als Reaktion auf eine nicht behandelte Ausnahme in einem seiner Plug-Ins hinzufügt.<br/>                                                                                          |
| [Inairpacketsdata](/previous-versions/ms824592(v=msdn.10))                     | **InAirPackets**           | Paketinformationen für die Stiftbewegung, während sich der Stift in der Luft über dem Digitizer befindet.<br/>                                                                                                                                                         |
| [Packetsdata](/previous-versions/ms824590(v=msdn.10))                               | **Pakete**                | Paketinformationen für die Stiftbewegung, während der Stift den Digitizer berührt.<br/>                                                                                                                                                             |
| [Realtimestylusdisableddata](/previous-versions/ms824576(v=msdn.10)) | **RealTimeStylusDisabled** | Informationen, die das [**RealTimeStylus-Objekt**](realtimestylus-class.md) hinzufügt, wenn es deaktiviert wird.<br/>                                                                                                                                        |
| [RealTimeStylusEnabledData](/previous-versions/ms824229(v=msdn.10))   | **RealTimeStylusEnabled**  | Informationen, die das [**RealTimeStylus-Objekt**](realtimestylus-class.md) hinzufügt, wenn es aktiviert wird.<br/>                                                                                                                                         |
| [Stylusbuttondowndata](/previous-versions/ms824181(v=msdn.10))             | **Stylusbuttondown**       | Informationen zur jeweiligen Stiftschaltfläche, die gedrückt wird.<br/>                                                                                                                                                                        |
| [Stylusbuttonupdata](/previous-versions/ms824172(v=msdn.10))                 | **StylusButtonUp**         | Informationen zur jeweiligen Stiftschaltfläche, die freigegeben wird.<br/>                                                                                                                                                                       |
| [Stylusdowndata](/previous-versions/ms585582(v=vs.100))                                   | **StylusDown**             | Paketinformationen für einen Stift, während der Stift in Kontakt mit dem Digitizer gebracht wird.<br/>                                                                                                                                                      |
| [Stylusinrangedata](/previous-versions/ms824090(v=msdn.10))                   | **StylusInRange**          | Informationen zum jeweiligen Stift, der in den Eingabebereich des [**RealTimeStylus-Objekts**](realtimestylus-class.md) oder in den Erkennungsbereich des Digitizers über dem Eingabebereich des **RealTimeStylus-Objekts** eintritt.<br/> |
| [Stylusoutofrangedata](/previous-versions/ms824072(v=msdn.10))             | **StylusOutOfRange**       | Informationen zum jeweiligen Stift, der den Eingabebereich des [**RealTimeStylus-Objekts**](realtimestylus-class.md) verlässt oder den Erkennungsbereich des Digitizers über dem Eingabebereich des **RealTimeStylus-Objekts** verlässt.<br/>   |
| [Stylusupdata](/previous-versions/ms824057(v=msdn.10))                             | **StylusUp**               | Paketinformationen für einen Stift, wenn der Stift aus dem Digitizer entfernt wird.<br/>                                                                                                                                                                  |
| [Systemgesturedata](/previous-versions/ms824019(v=msdn.10))                   | **Systemgesture**          | Informationen, die das [**RealTimeStylus-Objekt**](realtimestylus-class.md) hinzufügt, wenn es eine Systemgeste erkennt.<br/>                                                                                                                                 |
| [TabletAddedData](/previous-versions/ms824010(v=msdn.10))                       | **Tabletadded**            | Informationen zum [](/previous-versions/ms827783(v=msdn.10)) Tablet-Objekt, das hinzugefügt wird.<br/>                                                                                                                                                |
| [Tabletremoveddata](/previous-versions/ms823997(v=msdn.10))                   | **Tabletremoved**          | Informationen zum [](/previous-versions/ms827783(v=msdn.10)) Tablet-Objekt, das entfernt wird.<br/>                                                                                                                                              |



 

Informationen dazu, wie das [**RealTimeStylus-Objekt**](realtimestylus-class.md) den Tablettstiftdatenstrom behandelt, finden Sie unter [Working with the RealTimeStylus Class (Arbeiten mit der RealTimeStylus-Klasse).](working-with-the-realtimestylus-class.md)

## <a name="data-interest"></a>Daten von Interesse

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) überprüft die [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest-](/previous-versions/ms574887(v=vs.100)) oder [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest-Eigenschaft](/previous-versions/ms574886(v=vs.100)) eines Plug-Ins, wenn das Plug-In der synchronen oder asynchronen Plug-In-Auflistung des **RealTimeStylus-Objekts** hinzugefügt wird. Aus diesem Grund sollten Sie die DataInterest-Eigenschaft verwenden, um alle Benachrichtigungen zu abonnieren, die von dieser Instanz Ihres Plug-Ins verwendet werden, jedoch selten, aber nicht für Benachrichtigungen, die diese Instanz Ihres Plug-Ins nie verwendet. Bei Benachrichtigungen, die ihr Plug-In nur gelegentlich verwendet, überprüfen Sie zuerst den Zustand Ihres Plug-Ins in der Benachrichtigungsmethode und geben zurück, wenn die Benachrichtigung nicht vom Plug-In im aktuellen Zustand verwendet wird.

Ein Plug-In empfängt nur Aufrufe von Methoden, die in der [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest-](/previous-versions/ms574887(v=vs.100)) oder [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest-Eigenschaft](/previous-versions/ms574886(v=vs.100)) des Plug-Ins gekennzeichnet sind. Weitere Informationen zu den möglichen Werten der **DataInterest-Eigenschaft** eines Plug-Ins finden Sie unter [DataInterestMask-Enumeration.](/previous-versions/ms824787(v=msdn.10))

## <a name="timing"></a>Zeitliche Steuerung

Daten werden im [**RealTimeStylus-Objekt**](realtimestylus-class.md) in die Warteschlange eingereiht, bevor sie an die Plug-Ins in der asynchronen Plug-In-Sammlung übergeben werden. In der folgenden Liste werden einige Situationen beschrieben, die Sie beim Entwerfen eines asynchronen Plug-Ins berücksichtigen müssen.

-   Wenn das [**RealTimeStylus-Objekt**](realtimestylus-class.md) deaktiviert ist, empfängt das asynchrone Plug-In möglicherweise andere Benachrichtigungen in der Warteschlange, bevor die [RealTimeStylusDisabled-Methode](/previous-versions/ms824774(v=msdn.10)) aufgerufen wird. In diesem Fall auslösen Aufrufe des Plug-Ins an einige Methoden und Eigenschaften des **RealTimeStylus-Objekts** eine Ausnahme. Informationen, die für Ihr Plug-In relevant sind, sollten zwischengespeichert werden, wenn das **RealTimeStylus-Objekt** aktiviert ist.
-   Die [ClearStylusQueues-Methode](/previous-versions/ms825781(v=msdn.10)) des [**RealTimeStylus-Objekts**](realtimestylus-class.md) entfernt möglicherweise Informationen aus der Ausgabewarteschlange. Daher können asynchrone Plug-Ins nicht alle relevanten Benachrichtigungen empfangen.
-   Wenn ein [Tablet-Objekt](/previous-versions/ms827783(v=msdn.10)) entfernt wird, das für das [**RealTimeStylus-Objekt**](realtimestylus-class.md) verfügbar ist, empfängt das asynchrone Plug-In möglicherweise eine Tablettstiftbenachrichtigung in der Warteschlange für das Tablet, bevor die [TabletRemoved-Methode](/previous-versions/bb361092(v=vs.100)) aufgerufen wird. In diesem Fall funktioniert der Aufruf der [GetTabletPropertyDescriptionCollection-Methode](/previous-versions/ms825935(v=msdn.10)) des **RealTimeStylus-Objekts** nicht. Informationen, die für Ihr Plug-In relevant sind, sollten zwischengespeichert werden, wenn das **RealTimeStylus-Objekt** aktiviert ist oder wenn ein neues Tablet hinzugefügt wird.

Je nach Anwendung können Sie die Leistung verbessern, wenn Sie ein [**RealTimeStylus-Objekt**](realtimestylus-class.md) deaktivieren. Wenn die [Enabled-Eigenschaft](/previous-versions/ms824832(v=msdn.10)) des **RealTimeStylus-Objekts** auf **FALSE** festgelegt ist, werden Daten in den Eingabe- und Ausgabewarteschlangen verarbeitet, bis die Warteschlangen leer sind. Sie können die [ClearStylusQueues-Methode](/previous-versions/ms825781(v=msdn.10)) des **RealTimeStylus-Objekts** aufrufen, um die Warteschlangen zu löschen, bevor Sie das **RealTimeStylus-Objekt** deaktivieren.

## <a name="enabled-and-disabled-data"></a>Aktivierte und deaktivierte Daten

Wenn das [**RealTimeStylus-Objekt**](realtimestylus-class.md) aktiviert ist, empfängt jedes Plug-In einen Aufruf der [Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusEnabled-](/previous-versions/ms824758(v=msdn.10)) oder [Microsoft.StylusInput.IStylusAsyncPlugin.RealTimeStylusEnabled-Methode.](/previous-versions/ms824775(v=msdn.10)) Das in der Benachrichtigung **übergebene RealTimeStylusEnabledData-Objekt** enthält eine Auflistung der Kontextbezeichner für die verfügbaren Tablets zum Zeitpunkt der Aktivierung des **RealTimeStylus-Objekts.**

> [!Note]  
> Da die Plug-In-Daten für die asynchrone Plug-In-Sammlung des [**RealTimeStylus-Objekts**](realtimestylus-class.md) in die Warteschlange eingereiht werden, empfangen asynchrone Plug-Ins möglicherweise Daten, bevor sie einen Aufruf der [RealTimeStylusDisabled-Methode](/previous-versions/ms824774(v=msdn.10)) empfangen, aber nachdem das **RealTimeStylus-Objekt** deaktiviert wurde. Beachten Sie, dass einige der Methoden und Eigenschaften des **RealTimeStylus-Objekts** eine Ausnahme auslösen, wenn das **RealTimeStylus-Objekt** deaktiviert ist.

 

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) ruft die Methoden [Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) und [Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) für den Thread auf, aus dem das **RealTimeStylus-Objekt** aktiviert ist oder aus dem das synchrone Plug-In hinzugefügt wird.

Fügen Sie Plug-Ins im Allgemeinen hinzu, oder entfernen Sie sie, während das [**RealTimeStylus-Objekt**](realtimestylus-class.md) deaktiviert ist. Weitere Informationen zum Hinzufügen und Entfernen von Plug-Ins zum **RealTimeStylus-Objekt** finden Sie unter [Plug-Ins und die RealTimeStylus-Klasse.](plug-ins-and-the-realtimestylus-class.md)

## <a name="tablet-data"></a>Tablet-Daten

Wenn ein Tablet, das vom [**RealTimeStylus-Objekt**](realtimestylus-class.md) verwendet werden kann, dem Tablet-PC hinzugefügt oder daraus entfernt wird, während das **RealTimeStylus-Objekt** aktiviert ist, benachrichtigt das **RealTimeStylus-Objekt** seine Plug-Ins, dass ein [Tablet-Objekt](/previous-versions/ms827783(v=msdn.10)) hinzugefügt oder entfernt wurde. Jedes **RealTimeStylus-Objekt** verwaltet eine Liste eindeutiger Bezeichner für die Tablet-Objekte, mit denen es interagieren kann. Das **RealTimeStylus-Objekt** verfügt über zwei Methoden zum Übersetzen zwischen dem eindeutigen Bezeichner und dem Tablet-Objekt, den [Methoden GetTabletContextIdFromTablet](/previous-versions/ms825922(v=msdn.10)) und [GetTabletFromTabletContextId.](/previous-versions/ms825929(v=msdn.10))

> [!Note]  
> Informationen zu einem Tablet sind im [**RealTimeStylus-Objekt**](realtimestylus-class.md) nicht mehr verfügbar, nachdem das Tablet vom Tablet-PC entfernt wurde.

 

## <a name="tablet-pen-data"></a>Tablettstiftdaten

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) übergibt Informationen über den Tablettstift an seine Plug-Ins in einer Reihe von Benachrichtigungsmethoden. Informationen zum Tablettstift werden durch ein [Tablettstiftobjekt](/previous-versions/ms824824(v=msdn.10)) dargestellt. Dieses Objekt ist eine Momentaufnahme des Zustands des Tablettstifts zum Zeitpunkt der Datensammelung. Da Plug-Ins die Tablettstiftdaten als Teil des Tablettstiftdatenstroms empfangen, sollten die Plug-Ins die Informationen im Tablettstiftobjekt verwenden, anstatt den aktuellen Zustand eines bestimmten Tablettstifts über die [Cursor-Klasse](/previous-versions/ms839521(v=msdn.10)) zu überprüfen.

Jedes [Tablettstiftobjekt](/previous-versions/ms824824(v=msdn.10)) enthält den Tablet-Kontextbezeichner für das Tablet, das die Daten generiert hat.

## <a name="system-gesture-data"></a>Systemgestendaten

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) empfängt Daten zu Systemgesten, wenn sie vom Tablet PC erkannt werden. In der folgenden Tabelle wird die Reihenfolge beschrieben, in der die [SystemGestureData-Objekte](/previous-versions/ms824019(v=msdn.10)) im Datenstrom des Tablettstifts im Verhältnis zu anderen Tablettstiftdaten auftreten.




| <a href="/previous-versions/ms827134(v=msdn.10)">Systemgesture</a> | Objekte vor dem <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData-Objekt</a> | Objekte, die nach dem <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData-Objekt</a> stammen | 
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <strong>Tippen</strong> | Das <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData-Objekt.</a><br /> | Das [StylusUpData-Objekt.](/previous-versions/ms824057(v=msdn.10))<br /> | 
| <strong>DoubleTap</strong> | Das <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData-Objekt,</a> das <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData-Objekt</a> für die Tap-Systemgeste und die <strong></strong> [StylusUpData-Objekte.](/previous-versions/ms824057(v=msdn.10))<br /> | Das zweite <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData-Objekt.</a><br /> | 
| <strong>RightTap</strong> | Das <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData-Objekt</a> und das <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData-Objekt</a> für den <strong>HoldEnter-Member</strong> der <a href="/previous-versions/ms827134(v=msdn.10)">SystemGesure-Enumeration.</a><br /> | Das [StylusUpData-Objekt.](/previous-versions/ms824057(v=msdn.10))<br /> | 
| <strong>Ziehen</strong> | Das <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData-Objekt.</a><br /> | Das [StylusUpData-Objekt.](/previous-versions/ms824057(v=msdn.10))<br /> | 
| <strong>RightDrag</strong> | Das <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData-Objekt.</a><br /> | Das [StylusUpData-Objekt.](/previous-versions/ms824057(v=msdn.10))<br /> | 
| <strong>HoldEnter</strong> | Das <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData-Objekt.</a><br /> | Das [StylusUpData-Objekt.](/previous-versions/ms824057(v=msdn.10))<br /><blockquote>[!Note]<br />Diese Systemgeste wird nicht erkannt, wenn der Benutzer eine <strong>Drag-</strong> oder <strong>RightDrag-Systemgeste</strong> startet.</blockquote><br /> | 
| <strong>HoldLeave</strong> | Nicht implementiert.<br /> | Nicht implementiert.<br /> | 
| <strong>HoverEnter</strong> | Mehrere <a href="/previous-versions/ms824592(v=msdn.10)">InAirPacketsData-Objekte</a> mit niedriger durchschnittlicher Geschwindigkeit.<br /> | <blockquote>[!Note]<br />Es kann zu einer spürbaren Verzögerung kommen, bevor die <strong>HoverEnter-Systemgeste</strong> empfangen wird. Das <a href="realtimestylus-class.md"><strong>RealTimeStylus-Objekt</strong></a> empfängt diese Daten nur, wenn das <strong>RealTimeStylus-Objekt</strong> an das Fenster oder Steuerelement angefügt ist, das sich zum Zeitpunkt der Systemgeste direkt unter dem Stift befindet.</blockquote><br /> | 
| <strong>HoverLeave</strong> | Das <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData-Objekt</a> für die <strong>HoverEnter-Systemgeste</strong> und mehrere <a href="/previous-versions/ms824592(v=msdn.10)">InAirPacketsData-Objekte</a> mit ausreichender durchschnittlicher Geschwindigkeit.<br /> | <blockquote>[!Note]<br />Es kann zu einer spürbaren Verzögerung kommen, bevor die Systemgeste <strong>HoverLeave</strong> empfangen wird. Das <a href="realtimestylus-class.md"><strong>RealTimeStylus-Objekt</strong></a> empfängt diese Daten nur, wenn das <strong>RealTimeStylus-Objekt</strong> an das Fenster oder Steuerelement angefügt ist, das sich zum Zeitpunkt der Systemgeste direkt unter dem Stift befindet.</blockquote><br /> | 




 

## <a name="custom-stylus-data"></a>Benutzerdefinierte Stiftdaten

Benutzerdefinierte Stiftdaten können dem [**RealTimeStylus-Objekt**](realtimestylus-class.md) durch Aufrufen der [AddCustomStylusDataToQueue-Methode](/previous-versions/ms825761(v=msdn.10)) hinzugefügt werden. Benutzerdefinierte Stiftdaten können den Warteschlangen des **RealTimeStylus-Objekts** an einem von drei Stellen hinzugefügt werden.

-   Wenn der *Queue-Parameter* auf **Output** festgelegt ist, werden die benutzerdefinierten Daten der Ausgabewarteschlange des [**RealTimeStylus-Objekts**](realtimestylus-class.md) hinzugefügt, nachdem die Daten derzeit von der synchronen Plug-In-Sammlung verarbeitet werden.
-   Wenn der *queue-Parameter* auf **OutputImmediate** festgelegt ist, werden die benutzerdefinierten Daten der Ausgabewarteschlange des [**RealTimeStylus-Objekts**](realtimestylus-class.md) hinzugefügt, bevor die Daten derzeit von der synchronen Plug-In-Sammlung verarbeitet werden.
-   Wenn der *Queue-Parameter* auf **Eingabe** festgelegt ist, werden die benutzerdefinierten Daten der Eingabewarteschlange des [**RealTimeStylus-Objekts**](realtimestylus-class.md) hinzugefügt und an die synchrone Plug-In-Sammlung gesendet, bevor neue Daten aus dem Datenstrom des Tablettstifts stammen.

In jedem der vorherigen Fälle werden Daten, die von nachfolgenden Plug-Ins in der synchronen Plug-In-Sammlung hinzugefügt werden, nach den Daten hinzugefügt, die von vorherigen Plug-Ins hinzugefügt wurden.

> [!Note]  
> Wenn der Aufruf der [AddCustomStylusDataToQueue-Methode](/previous-versions/ms825761(v=msdn.10)) von einem synchronen Plug-In als Reaktion auf einen Aufruf einer ihrer [**IStylusSyncPlugin-Methoden**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) erfolgt, werden die benutzerdefinierten Stiftdaten dem Tablettstiftdatenstrom auf vorhersagbare Weise hinzugefügt. Andernfalls wird sie der Warteschlange in Bezug auf die aktuellen Stiftdaten hinzugefügt, die das [**RealTimeStylus-Objekt**](realtimestylus-class.md) verarbeitet, und nicht in Bezug auf die Daten, die das asynchrone Plug-In verarbeitet. Die AddCustomStylusDataToQueue-Methode löst eine Ausnahme aus, wenn das **RealTimeStylus-Objekt** deaktiviert ist.

 

Benutzerdefinierte Stiftdaten werden der Warteschlange als [CustomStylusData-Objekt](/previous-versions/ms824747(v=msdn.10)) hinzugefügt, und Plug-Ins empfangen diese Daten über ihre [Microsoft.StylusInput.IStylusSyncPlugin.CustomStylusDataAdded-](/previous-versions/ms824753(v=msdn.10)) oder [Microsoft.StylusInput.IStylusAsyncPlugin.CustomStylusDataAdded-Methode.](/previous-versions/ms824770(v=msdn.10))

Die [**Objekte DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) und [**GestureRecognizer**](gesturerecognizer-class.md) können der Warteschlange benutzerdefinierte Stiftdaten hinzufügen. Weitere Informationen zu **dynamicRenderer-** und **GestureRecognizer-Objekten** finden Sie unter [Dynamic-Renderer-Plug-Ins](dynamic-renderer-plug-ins.md) und [Erkennungs-Plug-Ins.](recognizer-plug-ins.md)

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) ruft die [Microsoft.StylusInput.IStylusSyncPlugin.CustomStylusDataAdded-Methode](/previous-versions/ms824753(v=msdn.10)) für den Thread auf, von dem der Aufruf der [AddCustomStylusDataToQueue-Methode](/previous-versions/ms825761(v=msdn.10)) empfangen wird.

Das folgende Diagramm veranschaulicht das Hinzufügen von benutzerdefinierten Stiftdaten zur Ausgabewarteschlange, wobei der *Warteschlangenparameter* auf **Ausgabe** festgelegt ist.

![Abbildung, die den Datenfluss benutzerdefinierter Stifte in die Ausgabewarteschlange zeigt ](images/27bc3672-41bc-432e-bf41-18e4ccec78f5.gif)

In diesem Diagramm stellen die Kreise mit den Buchstaben "A" und "B" Tablettstiftdaten dar, die der Ausgabewarteschlange des [**RealTimeStylus-Objekts**](realtimestylus-class.md) bereits hinzugefügt und noch nicht an die asynchrone Plug-In-Sammlung gesendet wurden. Der Kreis mit dem Buchstaben "C" stellt die Tablettstiftdaten dar, die das **RealTimeStylus-Objekt** gerade verarbeitet. Sie wird an die synchrone Plug-In-Sammlung gesendet und in der Ausgabewarteschlange platziert. Die Kreise mit der Nummer "1", "2" und "3" stellen benutzerdefinierte Tablettstiftdaten dar, die der Ausgabewarteschlange durch die ersten, zweiten und dritten synchronen Plug-Ins als Reaktion auf die Tablettstiftdaten hinzugefügt wurden, die durch "C" dargestellt werden. Die Plug-Ins haben die benutzerdefinierten Stiftdaten hinzugefügt, wobei der *Warteschlangenparameter* auf **StylusQueues** festgelegt ist. Der leere Kreis stellt die Position in der Ausgabewarteschlange dar, an der zukünftige Tablettstiftdaten hinzugefügt werden.

Das folgende Diagramm veranschaulicht das Hinzufügen von benutzerdefinierten Stiftdaten zur Ausgabewarteschlange, wobei der *queue-Parameter* auf **OutputImmediate** festgelegt ist.

![Diagramm, das den datenfluss des benutzerdefinierten Stifts an die Ausgabewarteschlange zeigt.](images/bcf45325-5557-47a2-af43-142c7684e482.gif)

In diesem Diagramm stellen die Kreise mit den Buchstaben "A" und "B" Tablettstiftdaten dar, die der Ausgabewarteschlange des [**RealTimeStylus-Objekts**](realtimestylus-class.md) bereits hinzugefügt und noch nicht an die asynchrone Plug-In-Sammlung gesendet wurden. Der Kreis mit dem Buchstaben "C" stellt die Tablettstiftdaten dar, die das **RealTimeStylus-Objekt** gerade verarbeitet. Sie wird an die synchrone Plug-In-Sammlung gesendet und in der Ausgabewarteschlange platziert. Die Kreise mit der Nummer "1", "2" und "3" stellen benutzerdefinierte Tablettstiftdaten dar, die der Ausgabewarteschlange durch die ersten, zweiten und dritten synchronen Plug-Ins als Reaktion auf die Tablettstiftdaten hinzugefügt wurden, die durch "C" dargestellt werden. Die Plug-Ins haben die benutzerdefinierten Stiftdaten hinzugefügt, wobei der *Warteschlangenparameter* auf **OutputImmediate** festgelegt ist. Der leere Kreis stellt die Position in der Ausgabewarteschlange dar, an der zukünftige Tablettstiftdaten hinzugefügt werden.

Das folgende Diagramm veranschaulicht das Hinzufügen von benutzerdefinierten Stiftdaten zur Eingabewarteschlange.

![Abbildung, die den Datenfluss benutzerdefinierter Stifte in die Ausgabewarteschlange zeigt](images/5dd2cfcc-1086-49b0-a0d5-9276c13c7f61.gif)

In diesem Diagramm stellen die Kreise mit den Buchstaben "A" und "B" Tablettstiftdaten dar, die der Ausgabewarteschlange des [**RealTimeStylus-Objekts**](realtimestylus-class.md) bereits hinzugefügt und noch nicht an die asynchrone Plug-In-Sammlung gesendet wurden. Der Kreis mit dem Buchstaben "C" stellt die Tablettstiftdaten dar, die das **RealTimeStylus-Objekt** gerade verarbeitet. Sie wird an die synchrone Plug-In-Sammlung gesendet und in der Ausgabewarteschlange platziert. Die Kreise mit der Nummer "1", "2" und "3" stellen benutzerdefinierte Tablettstiftdaten dar, die der Eingabewarteschlange durch die ersten, zweiten und dritten synchronen Plug-Ins als Reaktion auf die Tablettstiftdaten hinzugefügt wurden, die durch "C" dargestellt werden. Die Plug-Ins haben die benutzerdefinierten Stiftdaten hinzugefügt, wobei der *Warteschlangenparameter* auf **Eingabe** festgelegt ist. Die benutzerdefinierten Tablettstiftdaten mit der Nummer "1" werden dann an die synchronen Plug-Ins und dann an die Ausgabewarteschlange vor den benutzerdefinierten Tablettstiftdaten mit der Nummer "2" und "3" übergeben, die beide vor der Verarbeitung der nächsten Tablettstiftdaten verarbeitet werden. Der leere Kreis stellt die Position in der Ausgabewarteschlange dar, an der zukünftige Tablettstiftdaten hinzugefügt werden.

## <a name="error-data"></a>Fehlerdaten

Wenn ein Plug-In eine Ausnahme auslöst, wird der normale Datenfluss unterbrochen. Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) generiert ein [ErrorData-Objekt](/previous-versions/ms824740(v=msdn.10)) und ruft Folgendes auf:

-   Die [Microsoft.StylusInput.IStylusSyncPlugin.Error-](/previous-versions/ms824754(v=msdn.10)) oder [Microsoft.StylusInput.IStylusAsyncPlugin.Error-Methode](/previous-versions/ms824771(v=msdn.10)) des Plug-Ins, das die Ausnahme ausgelöst hat.
-   Die [Microsoft.StylusInput.IStylusSyncPlugin.Error-](/previous-versions/ms824754(v=msdn.10)) oder [Microsoft.StylusInput.IStylusAsyncPlugin.Error-Methode](/previous-versions/ms824771(v=msdn.10)) der verbleibenden Plug-Ins in dieser Sammlung.

Wenn das Plug-In, das die Ausnahme ausgelöst hat, ein synchrones Plug-In ist, wird das [ErrorData-Objekt](/previous-versions/ms824740(v=msdn.10)) der Ausgabewarteschlange hinzugefügt. Anschließend setzt das [**RealTimeStylus-Objekt**](realtimestylus-class.md) die normale Verarbeitung der ursprünglichen Daten fort.

Das folgende Diagramm veranschaulicht das Hinzufügen von Fehlerdaten zu den Tablettstiftdaten.

![Benutzerdefinierter Stiftdatenfluss in die Ausgabewarteschlange mit dem Hinzufügen von Fehlerdaten](images/c2f79abe-aeb5-498f-b389-1fad9bf01a13.gif)

In diesem Diagramm stellen die Kreise mit den Buchstaben "A" und "B" Tablettstiftdaten dar, die der Ausgabewarteschlange des [**RealTimeStylus-Objekts**](realtimestylus-class.md) bereits hinzugefügt und noch nicht an die asynchrone Plug-In-Sammlung gesendet wurden. Der Kreis mit dem Buchstaben "C" stellt die Tablettstiftdaten dar, die das **RealTimeStylus-Objekt** gerade verarbeitet. Der Kreis mit dem Buchstaben "e" stellt ein Vom **RealTimeStylus-Objekt** generiertes [ErrorData-Objekt](/previous-versions/ms824740(v=msdn.10)) dar, wenn das zweite synchrone Plug-In, synchrones Plug-In 2, eine Ausnahme auslöst, während "C" verarbeitet wird. Das **RealTimeStylus-Objekt** hält dann die Verarbeitung von "C" an und übergibt "e" an das Plug-In, das die Ausnahme und alle nachfolgenden Plug-Ins generiert hat. Das **RealTimeStylus-Objekt** fügt dann "e" in die Ausgabewarteschlange ein und setzt die Verarbeitung von "C" fort, das an die verbleibenden Plug-Ins in der synchronen Plug-In-Sammlung übergeben und nach "e" in der Ausgabewarteschlange platziert wird. Der leere Kreis stellt die Position in der Ausgabewarteschlange dar, an der zukünftige Tablettstiftdaten hinzugefügt werden.

Wenn ein Plug-In eine Ausnahme von seiner Error-Methode auslöst, fängt das [**RealTimeStylus-Objekt**](realtimestylus-class.md) die Ausnahme ab, generiert jedoch kein neues [ErrorData-Objekt.](/previous-versions/ms824740(v=msdn.10)) Dadurch soll eine Rekursion verhindert werden.

Die Fehlerdaten werden der Ausgabewarteschlange nach benutzerdefinierten Stiftdaten hinzugefügt, die an der **Position OutputImmediate** vor der Ausnahme hinzugefügt werden, die die Fehlerdaten erstellt hat, und vor benutzerdefinierten Stiftdaten, die durch nachfolgende Plug-Ins in der synchronen Plug-In-Sammlung an der **Position OutputImmediate** hinzugefügt werden.

Das folgende Diagramm veranschaulicht, wie die Fehlerdaten der Ausgabewarteschlange in Bezug auf benutzerdefinierte Daten hinzugefügt werden, die der **OutputImmediate-Warteschlange** hinzugefügt werden.

![Fehlerdaten, die der Ausgabewarteschlange in Bezug auf benutzerdefinierte Daten hinzugefügt wurden, die der outputimmediate-Warteschlange hinzugefügt wurden.](images/b00320c4-6fe7-439d-9855-e5f131feeb69.gif)

In diesem Diagramm stellen die Kreise mit den Buchstaben "A" und "B" Tablettstiftdaten dar, die der Ausgabewarteschlange des [**RealTimeStylus-Objekts**](realtimestylus-class.md) bereits hinzugefügt und noch nicht an die asynchrone Plug-In-Sammlung gesendet wurden. Der Kreis mit dem Buchstaben "C" stellt die Tablettstiftdaten dar, die das **RealTimeStylus-Objekt** gerade verarbeitet. Die Kreise mit der Nummer "1", "2" und "3" werden durch die ersten, zweiten und dritten synchronen Plug-Ins der **OutputImmediate-Warteschlange** als Reaktion auf die Daten hinzugefügt, die durch den Kreis mit dem Buchstaben "C" dargestellt werden. Der Kreis mit dem Buchstaben "e" stellt Fehlerdaten dar, die als Reaktion auf eine Ausnahme generiert wurden, die vom zweiten Plug-In ausgelöst wurde, nachdem das zweite Plug-In der Ausgabewarteschlange an der Position **OutputImmediate** benutzerdefinierte Daten hinzugefügt hat.

Wenn ein synchrones Plug-In der Eingabewarteschlange als Reaktion auf die Fehlerdaten benutzerdefinierte Stiftdaten hinzufügt, werden die Daten unmittelbar vor den Fehlerdaten hinzugefügt. Wenn eines der synchronen Plug-Ins der Ausgabewarteschlange als Reaktion auf die Fehlerdaten benutzerdefinierte Stiftdaten an der **Ausgabeposition** hinzufügt, werden die Daten unmittelbar nach den Fehlerdaten hinzugefügt.

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) ruft die [Microsoft.StylusInput.IStylusSyncPlugin.Error-Methode](/previous-versions/ms824754(v=msdn.10)) für den Thread auf, von dem die Ausnahme ausgelöst wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft.Ink.Tablet](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft.stylusinput.plugindata](/previous-versions/ms823992(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.DataInterestMask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Arbeiten mit der RealTimeStylus-Klasse](working-with-the-realtimestylus-class.md)
</dt> </dl>

 

 
