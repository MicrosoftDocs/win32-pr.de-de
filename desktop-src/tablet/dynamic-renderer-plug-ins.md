---
description: Ein Dynamic-Renderer-Plug-in ist ein Objekt, das die Tablet Pen-Daten in Echtzeit anzeigt, wie Sie vom RealTimeStylus-Objekt verarbeitet werden.
ms.assetid: ac6d15f3-0917-4cc1-8c83-e34d3d063289
title: Dynamic-Renderer-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c3f1a33c3cd7faef2e899bcb198ea64aa5bd76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563033"
---
# <a name="dynamic-renderer-plug-ins"></a>Dynamic-Renderer-Plug-ins

Ein Dynamic-Renderer-Plug-in ist ein Objekt, das die Tablet Pen-Daten in Echtzeit anzeigt, wie Sie vom [**RealTimeStylus**](realtimestylus-class.md) -Objekt verarbeitet werden. Für Ereignisse wie z. b. eine Formular Aktualisierung kann das Plug-in für dynamische Renderer bzw. ein frei Hand Sammler-Plug-in das frei Handzeichen neu zeichnen.

## <a name="the-dynamicrenderer-object"></a>Das DynamicRenderer-Objekt

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt implementiert die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -Schnittstelle. Das [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekt rendert die frei Hand Eingaben in Echtzeit, während Sie gezeichnet wird. Wenn die [**Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) -Methode aufgerufen wird, während das **DynamicRenderer** -Objekt aktiviert ist, zeichnet das **DynamicRenderer** -Objekt den aktuell erfassten Strich neu. Die [**aktivierte**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_enabled) Eigenschaft des **DynamicRenderer** -Objekts ist anfänglich auf **false** festgelegt.

> [!Note]  
> Wenn Sie die [**Refresh**](/previous-versions/ms826370(v=msdn.10)) -Methode des [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) -Objekts innerhalb eines [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) -Ereignis Handlers in verwaltetem Code aufrufen, legen Sie die [**clipRectangle**](/previous-versions/ms826346(v=msdn.10)) -Eigenschaft des **DynamicRenderer** -Objekts auf die [clipRectangle](/dotnet/api/system.windows.forms.painteventargs.cliprectangle?view=netcore-3.1) -Eigenschaft des [pinteventargs](/dotnet/api/system.windows.forms.painteventargs?view=netcore-3.1) -Objekts fest.

 

Das [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekt kann frei Hand Daten zwischenspeichern. Wenn Sie dieses Feature in verwaltetem Code verwenden möchten, legen Sie die [enabledatacache](/previous-versions/ms826349(v=msdn.10)) -Eigenschaft auf **true** fest. Wenn das [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) -Objekt einen Aufrufe der [**IStylusSyncPlugin. StylusUp**](/previous-versions/ms826366(v=msdn.10)) -Methode empfängt, speichert es die Strich Daten zwischen und fügt der Eingabe Warteschlange benutzerdefinierte Tablettstiftdaten als Reaktion auf das [**StylusUpData**](/previous-versions/ms824057(v=msdn.10)) -Objekt für den Strich hinzu. Die [CustomDataId](/previous-versions/ms824749(v=msdn.10)) -Eigenschaft des [**CustomStylusData**](/previous-versions/ms824747(v=msdn.10)) -Objekts wird auf den [DynamicRendererCachedDataGuid](/previous-versions/ms824744(v=msdn.10)) -Wert festgelegt, und die Dateneigenschaft des **CustomStylusData** -Objekts enthält ein dynamicrenderercacheddata-Objekt. Ruft die [releasecacheddata](/previous-versions/ms826371(v=msdn.10)) -Methode des **DynamicRenderer** -Objekts auf, sobald der Strich erfasst wurde und statisch gerendert werden kann. Wenn die [**Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) -Methode aufgerufen wird, während das **DynamicRenderer** -Objekt aktiviert ist, zeichnet das **DynamicRenderer** -Objekt alle Striche, die zwischengespeichert werden, neu. Wenn die [**datacacheaktivierte**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) -Eigenschaft auf **false** festgelegt ist, werden die zwischengespeicherten Strich Daten gelöscht.

Im folgenden Diagramm wird veranschaulicht, wie das [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekt den Tablettstift-Daten Daten hinzufügt, wenn die [**datacacheaktivierte**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) Eigenschaft des **DynamicRenderer** -Objekts festgelegt ist.

![Darstellung des DynamicRenderer-Datenflusses](images/75f4ee7b-160c-410e-bfae-dfc676a9829c.gif)

In diesem Diagramm stellt der Kreis mit dem Titel "SD" ein [**Stylus-**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) Objekt dar, und die Kreise mit dem Titel "P" stellen [**Pakete**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets) Objekte dar, die bereits der Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts hinzugefügt wurden und noch nicht an die asynchrone Plug-in-Auflistung gesendet wurden. Der Kreis mit dem Titel "su" stellt ein [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) -Objekt dar, das das **RealTimeStylus** -Objekt gerade verarbeitet. Sie wird an die synchrone Plug-in-Auflistung gesendet und dann in der Ausgabe Warteschlange abgelegt. Die Kreise mit dem Titel "Dr" stellen benutzerdefinierte Tablettstiftdaten dar, die der Eingabe Warteschlange durch das [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Plug-in als Antwort auf die mit "su" verknüpfte tablettstiftbenachrichtigung hinzugefügt werden. Die benutzerdefinierten Tablettstiftdaten, die "Dr" aufweisen, werden dann an die synchronen Plug-ins und dann an die Ausgabe Warteschlange weitergeleitet, bevor die nächsten Tablet Pen-Daten verarbeitet werden. Der leere Kreis stellt die Position in der Ausgabe Warteschlange dar, an der zukünftige Tablet Pen-Daten hinzugefügt werden. Auch im Diagramm dargestellt, ist das frei Hand Sammler-Plug-in, das die [**releasecacheddata**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-releasecacheddata) -Methode des **DynamicRenderer** -Objekts aufruft, um die zwischengespeicherten Strich Daten freizugeben, nachdem das Auflistungs-Plug-in den Strich verarbeitet hat.

### <a name="special-considerations"></a>Besondere Überlegungen

In der folgenden Liste werden andere Punkte beschrieben, die bei der Verwendung des [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekts zu berücksichtigen sind.

-   Sie sollten kein [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekt an mehr als ein [**RealTimeStylus**](realtimestylus-class.md) -Objekt anfügen. Wenn zwei **RealTimeStylus** -Objekte aktiviert sind, an die das **DynamicRenderer** -Objekt angefügt ist, geschieht Folgendes:

    -   Das [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekt löst eine Ausnahme als Reaktion auf den zweiten aufruflist der [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) -Methode aus.
    -   Das zweite zu aktivierende [**RealTimeStylus**](realtimestylus-class.md) -Objekt generiert ein [**Fehler**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) Objekt und benachrichtigt die übrigen Plug-ins in den Plug-in-Auflistungen des Fehlers.
    -   Das [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekt beendet das Rendering von Tablet Pen-Daten.

-   Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt löst eine Ausnahme aus, wenn die zugehörige [**AddCustomStylusDataToQueue**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addcustomstylusdatatoqueue) -Methode aufgerufen wird und der *GUID* -Parameter auf DynamicRendererCachedDataGuid Globally Unique Identifier (GUID) festgelegt ist.
-   Das [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekt wird als Component Object Model (com)-Wrapper implementiert, und Sie können seine [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -Schnittstellen Methoden nicht direkt aufzurufen. Weitere Informationen zum com-Vorgang und zum [**RealTimeStylus**](realtimestylus-class.md) -Objekt finden Sie unter [Implementierungs Hinweise für die StylusInput-APIs](implementation-notes-for-the-stylusinput-apis.md).

## <a name="custom-rendering"></a>Benutzerdefiniertes Rendering

Sie können ein eigenes Dynamic-Renderer-Plug-in erstellen, indem Sie ein [**synchrones**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown)Plug-in erstellen, das die Benachrichtigungen "StylusDown", " [**Pakete**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)" und " [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) " abonniert. Das Plug-in kann den Strich dann beim Zeichnen Rendering. Dies kann z. b. eine Möglichkeit zum Implementieren eines Auswahl Tools sein, das eine Freiform Auswahl oder ein Auswahlfeld verwendet.

 

 
