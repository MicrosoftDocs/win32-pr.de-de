---
description: Plug-Ins für die RealTimeStylus-Klasse müssen die IStylusSyncPlugin-oder IStylusAsyncPlugin-Schnittstelle implementieren oder beides.
ms.assetid: 827ac817-e0e6-4750-9d48-b939ccd5e679
title: Plug-In-Daten und die RealTimeStylus-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372b3d297edbad6d339285f45e92118184fa2cfc
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104554183"
---
# <a name="plug-in-data-and-the-realtimestylus-class"></a>Plug-In-Daten und die RealTimeStylus-Klasse

Plug-Ins für die [**RealTimeStylus**](realtimestylus-class.md) -Klasse müssen die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -oder [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle implementieren oder beides. Obwohl Sie alle Plug-in-Schnittstellen Methoden implementieren müssen, empfängt Ihr Plug-in nur Aufrufe von Methoden, die in den Plug-ins " [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100)) " oder " [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms574886(v=vs.100)) " gekennzeichnet sind.

Die Methoden, die für die Schnittstellen definiert sind, verwenden Objekte im [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) -Namespace, um die Stift Daten an die Plug-ins zu übergeben. In der folgenden Tabelle werden die Datenobjekte beschrieben, die in den Benachrichtigungs Methoden Parameter sind, und der [datainteressanmask](/previous-versions/ms824787(v=msdn.10)) -Wert, der der Benachrichtigung zugeordnet ist, aufgeführt.



| Plug-in-Daten                                                                                          | Datainteressanmask-Wert     | BESCHREIBUNG                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CustomStylusData](/previous-versions/ms824747(v=msdn.10))                     | **CustomStylusDataAdded**  | Benutzerdefinierte Anwendungsdaten, die von einem Plug-in hinzugefügt werden.<br/>                                                                                                                                                                                                 |
| [ErrorData](/previous-versions/ms824740(v=msdn.10))                                   | **Fehler**                  | Fehlerinformationen, die vom [**RealTimeStylus**](realtimestylus-class.md) -Objekt als Reaktion auf eine nicht behandelte Ausnahme in einem seiner Plug-Ins hinzugefügt werden.<br/>                                                                                          |
| [Inairpackeundata](/previous-versions/ms824592(v=msdn.10))                     | **Inairpakete**           | Paketinformationen für Stift Bewegung, während sich der Tablettstift über dem Digitalisierer befindet.<br/>                                                                                                                                                         |
| [Packeestdata](/previous-versions/ms824590(v=msdn.10))                               | **Pakete**                | Paketinformationen für Stift Bewegung, während der Tablettstift den Digitalisierer berührt.<br/>                                                                                                                                                             |
| [RealTimeStylusDisabledData](/previous-versions/ms824576(v=msdn.10)) | **Realtimestylusdeaktiviert** | Informationen, die das [**RealTimeStylus**](realtimestylus-class.md) -Objekt hinzufügt, wenn es deaktiviert wird.<br/>                                                                                                                                        |
| [Realtimestylusenableddata](/previous-versions/ms824229(v=msdn.10))   | **RealTimeStylusEnabled**  | Informationen, die das [**RealTimeStylus**](realtimestylus-class.md) -Objekt hinzufügt, wenn es aktiviert wird.<br/>                                                                                                                                         |
| [StylusButtonDownData](/previous-versions/ms824181(v=msdn.10))             | **StylusButtonDown**       | Informationen über die jeweilige Tablettstiftschaltfläche, auf die geklickt wird.<br/>                                                                                                                                                                        |
| [StylusButtonUpData](/previous-versions/ms824172(v=msdn.10))                 | **StylusButtonUp**         | Informationen über die jeweilige Tablettstiftschaltfläche, die freigegeben wird.<br/>                                                                                                                                                                       |
| [StylusDownData](/previous-versions/ms585582(v=vs.100))                                   | **StylusDown**             | Paketinformationen für einen Tablettstift, der als Tablettstift dient, werden mit dem Digitalisierer kontaktiert.<br/>                                                                                                                                                      |
| [StylusInRangeData](/previous-versions/ms824090(v=msdn.10))                   | **StylusInRange**          | Informationen über den speziellen Tablettstift, der in den Eingabebereich des [**RealTimeStylus**](realtimestylus-class.md) -Objekts wechselt, oder den Erkennungsbereich des Digitalisierungsprogramms über dem Eingabebereich des **RealTimeStylus** -Objekts eingeben.<br/> |
| [Stylusouyfrangedata](/previous-versions/ms824072(v=msdn.10))             | **Stylusouyfrange**       | Informationen über den speziellen Tablettstift, der den Eingabebereich des [**RealTimeStylus**](realtimestylus-class.md) -Objekts verlässt oder den Erkennungsbereich des Digitalisierungsprogramms über dem Eingabebereich des **RealTimeStylus** -Objekts verlässt.<br/>   |
| [StylusUpData](/previous-versions/ms824057(v=msdn.10))                             | **StylusUp**               | Paketinformationen für einen Tablettstift, wenn der Tablettstift vom Digitalisierer entfernt wird.<br/>                                                                                                                                                                  |
| [SystemGestureData](/previous-versions/ms824019(v=msdn.10))                   | **System Bewegung**          | Informationen, die das [**RealTimeStylus**](realtimestylus-class.md) -Objekt hinzufügt, wenn eine System Bewegung erkannt wird.<br/>                                                                                                                                 |
| [Tabletaddecoddata](/previous-versions/ms824010(v=msdn.10))                       | **TabletAdded**            | Informationen über das [Tablet](/previous-versions/ms827783(v=msdn.10)) -Objekt, das hinzugefügt wird.<br/>                                                                                                                                                |
| [Tabletremuveddata](/previous-versions/ms823997(v=msdn.10))                   | **Tabletreverschohe**          | Informationen zum [Tablet](/previous-versions/ms827783(v=msdn.10)) -Objekt, das entfernt wird.<br/>                                                                                                                                              |



 

Informationen dazu, wie das [**RealTimeStylus**](realtimestylus-class.md) -Objekt den Tablet Pen-Datenstrom verarbeitet, finden Sie unter [Arbeiten mit der RealTimeStylus-Klasse](working-with-the-realtimestylus-class.md).

## <a name="data-interest"></a>Daten Interesse

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt überprüft die Eigenschaft [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100)) oder [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms574886(v=vs.100)) eines Plug-ins, wenn das Plug-in zur synchronen oder asynchronen Plug-in-Auflistung des **RealTimeStylus** -Objekts hinzugefügt wird. Daher sollten Sie die DataInterest-Eigenschaft verwenden, um alle Benachrichtigungen zu abonnieren, die von dieser Instanz des Plug-ins verwendet werden, jedoch nur selten, aber nicht für eine der Benachrichtigungen, die von dieser Instanz des Plug-ins niemals verwendet werden. Bei Benachrichtigungen, die von Ihrem Plug-in nur gelegentlich verwendet werden, wird der Status des Plug-ins zuerst in der Benachrichtigungs Methode überprüft, und es wird zurückgegeben, wenn die Benachrichtigung von Ihrem Plug-in im aktuellen Zustand nicht verwendet wird.

Ein Plug-in empfängt nur Aufrufe von Methoden, die in der [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms574887(v=vs.100)) -oder [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms574886(v=vs.100)) -Eigenschaft des Plug-ins gekennzeichnet sind. Weitere Informationen zu den möglichen Werten für die **DataInterest** -Eigenschaft eines Plug-Ins finden Sie in der [datainteressanmask](/previous-versions/ms824787(v=msdn.10)) -Enumeration.

## <a name="timing"></a>Zeitliche Steuerung

Die Daten werden im [**RealTimeStylus**](realtimestylus-class.md) -Objekt in die Warteschlange eingereiht, bevor Sie an die Plug-ins in der asynchronen Plug-in-Auflistung übermittelt werden. In der folgenden Liste werden einige Situationen beschrieben, die beim Entwerfen eines asynchronen Plug-ins möglicherweise berücksichtigt werden müssen.

-   Wenn das [**RealTimeStylus**](realtimestylus-class.md) -Objekt deaktiviert ist, empfängt das asynchrone Plug-in möglicherweise andere Benachrichtigungen in der Warteschlange, bevor die zugehörige [realtimestylusdeaktiviert](/previous-versions/ms824774(v=msdn.10)) -Methode aufgerufen wird. In dieser Situation lösen Aufrufe vom Plug-in für einige der Methoden und Eigenschaften des **RealTimeStylus** -Objekts eine Ausnahme aus. Die für das Plug-in relevanten Informationen sollten zwischengespeichert werden, wenn das **RealTimeStylus** -Objekt aktiviert ist.
-   Die [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) -Methode des [**RealTimeStylus**](realtimestylus-class.md) -Objekts kann Informationen aus der Ausgabe Warteschlange entfernen. Daher können sich asynchrone Plug-ins nicht darauf verlassen, dass alle relevanten Benachrichtigungen empfangen werden.
-   Wenn ein [Tablet](/previous-versions/ms827783(v=msdn.10)) -Objekt entfernt wird, das für das [**RealTimeStylus**](realtimestylus-class.md) -Objekt verfügbar ist, empfängt das asynchrone Plug-in möglicherweise eine Warteschlangen Benachrichtigung für das Tablet, bevor die [tabletreverschote](/previous-versions/bb361092(v=vs.100)) -Methode aufgerufen wird. In dieser Situation funktioniert das Aufrufen der [GetTabletPropertyDescriptionCollection](/previous-versions/ms825935(v=msdn.10)) -Methode des **RealTimeStylus** -Objekts nicht. Die für das Plug-in relevanten Informationen sollten zwischengespeichert werden, wenn das **RealTimeStylus** -Objekt aktiviert ist, oder wenn ein neues Tablet hinzugefügt wird.

Abhängig von Ihrer Anwendung können Sie die Leistung bei der Deaktivierung eines [**RealTimeStylus**](realtimestylus-class.md) -Objekts verbessern. Wenn die [aktivierte](/previous-versions/ms824832(v=msdn.10)) Eigenschaft des **RealTimeStylus** -Objekts auf **false** festgelegt ist, werden Daten in den Eingabe-und Ausgabe Warteschlangen so lange verarbeitet, bis die Warteschlangen leer sind. Sie können die [ClearStylusQueues](/previous-versions/ms825781(v=msdn.10)) -Methode des **RealTimeStylus** -Objekts aufrufen, um die Warteschlangen vor der Deaktivierung des **RealTimeStylus** -Objekts zu löschen.

## <a name="enabled-and-disabled-data"></a>Aktivierte und deaktivierte Daten

Wenn das [**RealTimeStylus**](realtimestylus-class.md) -Objekt aktiviert ist, empfängt jedes Plug-in einen Aufrufen der [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) -Methode oder der [Microsoft. StylusInput. IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) -Methode. Das in der Benachrichtigung weiter gegebene **realtimestylusenableddata** -Objekt enthält eine Sammlung der Kontext Bezeichner für die verfügbaren Tablets zum Zeitpunkt der Aktivierung des **RealTimeStylus** -Objekts.

> [!Note]  
> Da die Plug-in-Daten für die asynchrone Plug-in-Auflistung des [**RealTimeStylus**](realtimestylus-class.md) -Objekts in die Warteschlange eingereiht werden, empfangen asynchrone Plug-ins möglicherweise Daten, bevor Sie einen Aufrufe **an die** zugehörige [realtimestylusdeaktivierte](/previous-versions/ms824774(v=msdn.10)) Methode erhalten. Beachten Sie, dass einige der Methoden und Eigenschaften des **RealTimeStylus** -Objekts eine Ausnahme auslösen, wenn das **RealTimeStylus** -Objekt deaktiviert ist.

 

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt ruft die Methoden [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) und [Microsoft. StylusInput. IStylusSyncPlugin. realtimestylusdeaktiviert](/previous-versions/ms824757(v=msdn.10)) für den Thread auf, von dem das **RealTimeStylus** -Objekt aktiviert wird oder das synchrone Plug-in hinzugefügt wird

Im Allgemeinen können Sie Plug-Ins hinzufügen oder entfernen, während das [**RealTimeStylus**](realtimestylus-class.md) -Objekt deaktiviert ist. Weitere Informationen zum Hinzufügen und Entfernen von Plug-Ins für das **RealTimeStylus** -Objekt finden Sie unter [Plug-ins und RealTimeStylus-Klasse](plug-ins-and-the-realtimestylus-class.md).

## <a name="tablet-data"></a>Tablet-Daten

Wenn ein Tablet, das vom [**RealTimeStylus**](realtimestylus-class.md) -Objekt verwendet werden kann, zum Tablet PC hinzugefügt oder daraus entfernt wird, während das **RealTimeStylus** -Objekt aktiviert ist, benachrichtigt das **RealTimeStylus** -Objekt die Plug-ins, dass ein [Tablet](/previous-versions/ms827783(v=msdn.10)) -Objekt hinzugefügt oder entfernt wurde. Jedes **RealTimeStylus** -Objekt verwaltet eine Liste eindeutiger Bezeichner für die Tablet-Objekte, mit denen er interagieren kann. Das **RealTimeStylus** -Objekt verfügt über zwei Methoden für die Übersetzung zwischen dem eindeutigen Bezeichner und dem Tablet-Objekt, der [GetTabletContextIdFromTablet](/previous-versions/ms825922(v=msdn.10)) -Methode und der [GetTabletFromTabletContextId](/previous-versions/ms825929(v=msdn.10)) -Methode.

> [!Note]  
> Informationen zu einem Tablet sind nicht mehr über das [**RealTimeStylus**](realtimestylus-class.md) -Objekt verfügbar, nachdem das Tablet vom Tablet PC entfernt wurde.

 

## <a name="tablet-pen-data"></a>Tablettstift Daten

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt übergibt Informationen über den Tablettstift an seine Plug-ins in einer Reihe von Benachrichtigungs Methoden. Informationen über den [Tablettstift](/previous-versions/ms824824(v=msdn.10)) werden durch ein tablettstiftobjekt dargestellt. Bei diesem Objekt handelt es sich um eine Momentaufnahme des Zustands des Tablettstifts zum Zeitpunkt, zu dem die Daten gesammelt wurden. Da Plug-ins die Tablet Pen-Daten als Teil des Tablet Pen-Datenstroms empfangen, sollten die Plug-ins die Informationen im tablettstiftobjekt verwenden, anstatt den aktuellen Zustand eines bestimmten Tablet Stifts durch die [Cursor](/previous-versions/ms839521(v=msdn.10)) Klasse zu überprüfen.

Jedes [](/previous-versions/ms824824(v=msdn.10)) tablettstiftobjekt enthält den Tablet-Kontext Bezeichner für das Tablet, von dem die Daten generiert wurden.

## <a name="system-gesture-data"></a>System Gesten Daten

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt empfängt Daten über System Gesten, da diese vom Tablet PC erkannt werden. In der folgenden Tabelle wird die Reihenfolge beschrieben, in der die [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) -Objekte im Datenstrom des Tablet-Stifts in Bezug auf andere Tablet Pen-Daten vorkommen.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><a href="/previous-versions/ms827134(v=msdn.10)">System Bewegung</a></th>
<th>Objekte, die dem <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> -Objekt vorangestellt sind</th>
<th>Objekte, die nach dem <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> -Objekt stehen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Tippen</strong></td>
<td>Das <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> -Objekt.<br/></td>
<td>Das [StylusUpData](/previous-versions/ms824057(v=msdn.10)) -Objekt.<br/></td>
</tr>
<tr class="even">
<td><strong>Double Tap</strong></td>
<td>Das <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> -Objekt, das <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> -Objekt für die <strong>Tap</strong> -System Geste und die [StylusUpData](/previous-versions/ms824057(v=msdn.10)) -Objekte.<br/></td>
<td>Das zweite <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> -Objekt.<br/></td>
</tr>
<tr class="odd">
<td><strong>RightTap</strong></td>
<td>Das <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> -Objekt und das <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> -Objekt für den zurück <strong>Haltungs Member</strong> der <a href="/previous-versions/ms827134(v=msdn.10)">systemgesure</a> -Enumeration.<br/></td>
<td>Das [StylusUpData](/previous-versions/ms824057(v=msdn.10)) -Objekt.<br/></td>
</tr>
<tr class="even">
<td><strong>Hinein</strong></td>
<td>Das <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> -Objekt.<br/></td>
<td>Das [StylusUpData](/previous-versions/ms824057(v=msdn.10)) -Objekt.<br/></td>
</tr>
<tr class="odd">
<td><strong>RightDrag</strong></td>
<td>Das <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> -Objekt.<br/></td>
<td>Das [StylusUpData](/previous-versions/ms824057(v=msdn.10)) -Objekt.<br/></td>
</tr>
<tr class="even">
<td><strong>Holdenter</strong></td>
<td>Das <a href="/previous-versions/ms824107(v=msdn.10)">StylusDownData</a> -Objekt.<br/></td>
<td>Das [StylusUpData](/previous-versions/ms824057(v=msdn.10)) -Objekt.<br/>
<blockquote>
[!Note]<br />
Diese System Geste wird nicht erkannt, wenn der Benutzer eine <strong>Drag</strong> -oder <strong>RightDrag</strong> -System Bewegung startet.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>Holdleave</strong></td>
<td>Nicht implementiert.<br/></td>
<td>Nicht implementiert.<br/></td>
</tr>
<tr class="even">
<td><strong>HoverEnter</strong></td>
<td>Mehrere <a href="/previous-versions/ms824592(v=msdn.10)">inairpackezdata</a> -Objekte mit niedriger durchschnittlicher Geschwindigkeit.<br/></td>
<td><blockquote>
[!Note]<br />
Möglicherweise gibt es eine merkliche Verzögerung, bevor die <strong>HoverEnter</strong> -System Geste empfangen wird. Das <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> -Objekt empfängt diese Daten nur, wenn das <strong>RealTimeStylus</strong> -Objekt an das Fenster oder Steuerelement angefügt ist, das zum Zeitpunkt der System Bewegung direkt unter dem Stift liegt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>HoverLeave</strong></td>
<td>Das <a href="/previous-versions/ms824019(v=msdn.10)">SystemGestureData</a> -Objekt für die <strong>HoverEnter</strong> -System Bewegung und mehrere <a href="/previous-versions/ms824592(v=msdn.10)">inairpackezdata</a> -Objekte mit ausreichender durchschnittlicher Geschwindigkeit.<br/></td>
<td><blockquote>
[!Note]<br />
Möglicherweise gibt es eine merkliche Verzögerung, bevor die <strong>HoverLeave</strong> -System Geste empfangen wird. Das <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> -Objekt empfängt diese Daten nur, wenn das <strong>RealTimeStylus</strong> -Objekt an das Fenster oder Steuerelement angefügt ist, das zum Zeitpunkt der System Bewegung direkt unter dem Stift liegt.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="custom-stylus-data"></a>Benutzerdefinierte Tablettstiftdaten

Benutzerdefinierte Tablettstiftdaten können dem [**RealTimeStylus**](realtimestylus-class.md) -Objekt hinzugefügt werden, indem die [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) -Methode aufgerufen wird. Benutzerdefinierte Tablettstiftdaten können den Warteschlangen des **RealTimeStylus** -Objekts an einem von drei Stellen hinzugefügt werden.

-   Wenn der *Queue* -Parameter auf **Output** festgelegt ist, werden die benutzerdefinierten Daten der Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts hinzugefügt, nachdem die Daten derzeit von der synchronen Plug-in-Auflistung verarbeitet wurden.
-   Wenn der *Queue* -Parameter auf **outputimvermittler** festgelegt ist, werden die benutzerdefinierten Daten der Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts hinzugefügt, bevor die Daten verarbeitet werden, die derzeit von der synchronen Plug-in-Auflistung verarbeitet werden.
-   Wenn der *Queue* -Parameter auf **Input** festgelegt ist, werden die benutzerdefinierten Daten der Eingabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts hinzugefügt und an die synchrone Plug-in-Auflistung gesendet, bevor neue Daten aus dem Datenstrom des Tablettstifts eingegeben werden.

In jedem der vorangegangenen Fälle werden Daten, die von nachfolgenden Plug-ins in der synchronen Plug-in-Sammlung hinzugefügt wurden, nach den durch vorangehenden Plug-Ins hinzugefügten Daten hinzugefügt.

> [!Note]  
> Wenn der Aufrufe der [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) -Methode von einem synchronen Plug-in als Reaktion auf einen-Rückruf einer der [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -Methoden durchgeführt wird, werden die benutzerdefinierten Tablettstiftdaten in einer vorhersagbaren Weise dem Tablet Pen-Datenstrom hinzugefügt. Andernfalls wird Sie der Warteschlange in Bezug auf die aktuellen Stift Daten hinzugefügt, die das [**RealTimeStylus**](realtimestylus-class.md) -Objekt verarbeitet, und nicht in Bezug auf die Daten, die das asynchrone Plug-in verarbeitet. Die AddCustomStylusDataToQueue-Methode löst eine Ausnahme aus, wenn das **RealTimeStylus** -Objekt deaktiviert ist.

 

Benutzerdefinierte Tablettstiftdaten werden der Warteschlange als [CustomStylusData](/previous-versions/ms824747(v=msdn.10)) -Objekt hinzugefügt, und Plug-ins empfangen diese Daten über die [Microsoft. StylusInput. IStylusSyncPlugin. CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) -oder [Microsoft. StylusInput. IStylusAsyncPlugin. CustomStylusDataAdded](/previous-versions/ms824770(v=msdn.10)) -Methode.

Der [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) und die [**GestureRecognizer**](gesturerecognizer-class.md) -Objekte können der Warteschlange benutzerdefinierte Tablettstiftdaten hinzufügen. Weitere Informationen zu **DynamicRenderer** und den **GestureRecognizer** -Objekten finden Sie unter [Dynamic-Renderer-Plug-ins](dynamic-renderer-plug-ins.md) und [Erkennungs-Plug-ins](recognizer-plug-ins.md).

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt ruft die [Microsoft. StylusInput. IStylusSyncPlugin. CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) -Methode für den Thread auf, von dem der Aufruf der [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) -Methode empfangen wird.

Im folgenden Diagramm wird veranschaulicht, wie benutzerdefinierte Tablettstiftdaten der Ausgabe Warteschlange hinzugefügt werden, wobei der Parameter *Queue* auf **Output** festgelegt ist.

![Darstellung des benutzerdefinierten Tablettstiftdaten Flusses in der Ausgabe Warteschlange ](images/27bc3672-41bc-432e-bf41-18e4ccec78f5.gif)

In diesem Diagramm stellen die Kreise "A" und "B" Tablet Pen-Daten dar, die bereits der Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts hinzugefügt wurden und noch nicht an die asynchrone Plug-in-Auflistung gesendet wurden. Der Kreis mit dem Titel "C" stellt die Tablettstiftdaten dar, die das **RealTimeStylus** -Objekt gerade verarbeitet. Sie wird an die synchrone Plug-in-Auflistung gesendet und in der Ausgabe Warteschlange abgelegt. Die mit "1", "2" und "3" nummerierten Kreise stellen benutzerdefinierte Tablettstiftdaten dar, die der Ausgabe Warteschlange jeweils durch das erste, zweite und dritte synchrone Plug-in hinzugefügt wurden, und zwar als Antwort auf die Tablet Pen-Daten, die durch "C" dargestellt werden. Die Plug-ins haben die benutzerdefinierten Tablettstiftdaten hinzugefügt, wobei der *Queue* -Parameter auf **StylusQueues** festgelegt wurde. Der leere Kreis stellt die Position in der Ausgabe Warteschlange dar, an der zukünftige Tablet Pen-Daten hinzugefügt werden.

Das folgende Diagramm veranschaulicht das Hinzufügen von benutzerdefinierten Tablettstiftdaten zur Ausgabe Warteschlange, wobei der *Queue* -Parameter auf **outputimvermittler** festgelegt ist.

![Diagramm, das den benutzerdefinierten Tablettstiftdaten Fluss in der Ausgabe Warteschlange anzeigt.](images/bcf45325-5557-47a2-af43-142c7684e482.gif)

In diesem Diagramm stellen die Kreise "A" und "B" Tablet Pen-Daten dar, die bereits der Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts hinzugefügt wurden und noch nicht an die asynchrone Plug-in-Auflistung gesendet wurden. Der Kreis mit dem Titel "C" stellt die Tablettstiftdaten dar, die das **RealTimeStylus** -Objekt gerade verarbeitet. Sie wird an die synchrone Plug-in-Auflistung gesendet und in der Ausgabe Warteschlange abgelegt. Die mit "1", "2" und "3" nummerierten Kreise stellen benutzerdefinierte Tablettstiftdaten dar, die der Ausgabe Warteschlange jeweils durch das erste, zweite und dritte synchrone Plug-in hinzugefügt wurden, und zwar als Antwort auf die Tablet Pen-Daten, die durch "C" dargestellt werden. Die Plug-ins haben die benutzerdefinierten Tablettstiftdaten hinzugefügt, wobei der *Queue* -Parameter auf **outputimvermittler** festgelegt wurde. Der leere Kreis stellt die Position in der Ausgabe Warteschlange dar, an der zukünftige Tablet Pen-Daten hinzugefügt werden.

Das folgende Diagramm veranschaulicht das Hinzufügen von benutzerdefinierten Tablettstiftdaten zur Eingabe Warteschlange.

![Darstellung des benutzerdefinierten Tablettstiftdaten Flusses in der Ausgabe Warteschlange](images/5dd2cfcc-1086-49b0-a0d5-9276c13c7f61.gif)

In diesem Diagramm stellen die Kreise "A" und "B" Tablet Pen-Daten dar, die bereits der Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts hinzugefügt wurden und noch nicht an die asynchrone Plug-in-Auflistung gesendet wurden. Der Kreis mit dem Titel "C" stellt die Tablettstiftdaten dar, die das **RealTimeStylus** -Objekt gerade verarbeitet. Sie wird an die synchrone Plug-in-Auflistung gesendet und in der Ausgabe Warteschlange abgelegt. Die mit "1", "2" und "3" nummerierten Kreise stellen benutzerdefinierte Tablettstiftdaten dar, die der Eingabe Warteschlange jeweils durch das erste, zweite und dritte synchrone Plug-in hinzugefügt wurden, und zwar als Antwort auf die Tablet Pen-Daten, die durch "C" dargestellt werden. Die Plug-ins haben die benutzerdefinierten Tablettstiftdaten hinzugefügt, wobei der *Queue* -Parameter auf **Input** festgelegt wurde. Die mit "1" nummerierten benutzerdefinierten Tablettstiftdaten werden dann an die synchronen Plug-ins und dann an die Ausgabe Warteschlange weitergeleitet, bevor die benutzerdefinierten Tablettstiftdaten "2" und "3" nummeriert werden, die beide vor der Verarbeitung der nächsten Tablet Pen-Daten verarbeitet werden. Der leere Kreis stellt die Position in der Ausgabe Warteschlange dar, an der zukünftige Tablet Pen-Daten hinzugefügt werden.

## <a name="error-data"></a>Fehler Daten

Wenn ein Plug-in eine Ausnahme auslöst, wird der normale Datenfluss unterbrochen. Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt generiert ein [ErrorData](/previous-versions/ms824740(v=msdn.10)) -Objekt und ruft Folgendes auf:

-   Die [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) -oder [Microsoft. StylusInput. IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) -Methode des Plug-ins, das die Ausnahme ausgelöst hat.
-   Die [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) -oder [Microsoft. StylusInput. IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) -Methode der restlichen Plug-ins in dieser Auflistung.

Wenn das Plug-in, das die Ausnahme ausgelöst hat, ein synchrones Plug-in ist, wird das [ErrorData](/previous-versions/ms824740(v=msdn.10)) -Objekt der Ausgabe Warteschlange hinzugefügt. Anschließend nimmt das [**RealTimeStylus**](realtimestylus-class.md) -Objekt die normale Verarbeitung der ursprünglichen Daten wieder auf.

Das folgende Diagramm veranschaulicht das Hinzufügen von Fehler Daten zu den Tablettstift-Daten.

![benutzerdefinierter Tablettstiftdaten Fluss in die Ausgabe Warteschlange mit dem Hinzufügen von Fehler Daten](images/c2f79abe-aeb5-498f-b389-1fad9bf01a13.gif)

In diesem Diagramm stellen die Kreise "A" und "B" Tablet Pen-Daten dar, die bereits der Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts hinzugefügt wurden und noch nicht an die asynchrone Plug-in-Auflistung gesendet wurden. Der Kreis mit dem Titel "C" stellt die Tablettstiftdaten dar, die das **RealTimeStylus** -Objekt gerade verarbeitet. Der Kreis mit dem Wert "e" stellt ein [ErrorData](/previous-versions/ms824740(v=msdn.10)) -Objekt dar, das vom **RealTimeStylus** -Objekt generiert wird, wenn das zweite synchrone Plug-in (synchrones Plug-in 2) eine Ausnahme auslöst, während es "C" verarbeitet. Das **RealTimeStylus** -Objekt hält seine Verarbeitung von "C" an und übergibt "e" an das Plug-in, das die Ausnahme und alle nachfolgenden Plug-ins generiert hat. Das **RealTimeStylus** -Objekt fügt dann "e" in die Ausgabe Warteschlange ein und setzt die Verarbeitung von "C" fort, das an die restlichen Plug-ins in der synchronen Plug-in-Auflistung und in der Ausgabe Warteschlange nach "e" platziert wird. Der leere Kreis stellt die Position in der Ausgabe Warteschlange dar, an der zukünftige Tablet Pen-Daten hinzugefügt werden.

Wenn ein Plug-in eine Ausnahme von der Fehler Methode auslöst, fängt das [**RealTimeStylus**](realtimestylus-class.md) -Objekt die Ausnahme ab, generiert jedoch kein neues [ErrorData](/previous-versions/ms824740(v=msdn.10)) -Objekt. Dadurch wird die Rekursion verhindert.

Die Fehler Daten werden der Ausgabe Warteschlange hinzugefügt, nachdem alle benutzerdefinierten Tablettstiftdaten, die an der **outputimvermittler** -Position vor der Ausnahme, die die Fehler Daten erstellt hat, und vor benutzerdefinierten Tablettstiftdaten, die an der **outputimvermittler** -Position hinzugefügt wurden, von nachfolgenden Plug-ins in der synchronen Plug-in-Auflistung

Im folgenden Diagramm wird veranschaulicht, wie die Fehler Daten der Ausgabe Warteschlange in Bezug auf benutzerdefinierte Daten, die der **outputimvermittler** -Warteschlange hinzugefügt werden, hinzugefügt werden.

![der Ausgabe Warteschlange hinzugefügte Fehler Daten in Bezug auf benutzerdefinierte Daten, die der outputimvermittler-Warteschlange hinzugefügt werden](images/b00320c4-6fe7-439d-9855-e5f131feeb69.gif)

In diesem Diagramm stellen die Kreise "A" und "B" Tablet Pen-Daten dar, die bereits der Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts hinzugefügt wurden und noch nicht an die asynchrone Plug-in-Auflistung gesendet wurden. Der Kreis mit dem Titel "C" stellt die Tablettstiftdaten dar, die das **RealTimeStylus** -Objekt gerade verarbeitet. Die mit "1", "2" und "3" nummerierten Kreise werden durch das erste, zweite und dritte synchrone Plug-ins der **outputimvermittler** -Warteschlange als Reaktion auf die Daten hinzugefügt, die durch den Kreis mit dem Wert "C" dargestellt werden. Der Kreis "e" stellt Fehler Daten dar, die als Reaktion auf eine Ausnahme generiert werden, die durch das zweite Plug-in ausgelöst wurde, nachdem das zweite Plug-in der Ausgabe Warteschlange an der Position " **outputimvermittlung** " benutzerdefinierte Daten hinzugefügt hat.

Wenn ein beliebiges synchrones Plug-in der Eingabe Warteschlange benutzerdefinierte Tablettstiftdaten als Antwort auf die Fehler Daten hinzufügt, werden die Daten unmittelbar vor den Fehler Daten hinzugefügt. Wenn ein beliebiges synchrones Plug-in der Ausgabe Warteschlange an der **Ausgabe** Position als Antwort auf die Fehler Daten benutzerdefinierte Tablettstiftdaten hinzufügt, werden die Daten unmittelbar nach den Fehler Daten hinzugefügt.

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt ruft die [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) -Methode für den Thread auf, von dem die Ausnahme ausgelöst wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft. Ink. Tablet](/previous-versions/ms827783(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. datainteressanmask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Arbeiten mit der RealTimeStylus-Klasse](working-with-the-realtimestylus-class.md)
</dt> </dl>

 

 
