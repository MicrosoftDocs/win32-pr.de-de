---
description: Ein Plug-In mit dynamischem Renderer ist ein Objekt, das die Tablettstiftdaten in Echtzeit anzeigt, während sie vom RealTimeStylus-Objekt verarbeitet werden.
ms.assetid: ac6d15f3-0917-4cc1-8c83-e34d3d063289
title: Dynamic-Renderer-Plug-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6426dfc9f1dae8561802d2cf6c5613fb786600504cc8600046c4df781239abf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092681"
---
# <a name="dynamic-renderer-plug-ins"></a>Dynamic-Renderer-Plug-Ins

Ein Plug-In mit dynamischem Renderer ist ein Objekt, das die Tablettstiftdaten in Echtzeit anzeigt, während sie vom [**RealTimeStylus-Objekt**](realtimestylus-class.md) verarbeitet werden. Später kann das Plug-In für dynamische Renderer oder ein Ink-Collector-Plug-In für Ereignisse wie eine Formularaktualisierung die Ink-Ink neu zeichnen.

## <a name="the-dynamicrenderer-object"></a>Das DynamicRenderer-Objekt

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) implementiert die [**IStylusSyncPlugin-Schnittstelle.**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) Das [**DynamicRenderer-Objekt**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) rendert die Ink-Ink in Echtzeit, während sie gezeichnet wird. Wenn die [**Refresh-Methode**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) aufgerufen wird, während das **DynamicRenderer-Objekt** aktiviert ist, zeichnet das **DynamicRenderer-Objekt** den aktuell erfassten Strich neu. Die [**Enabled-Eigenschaft**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_enabled) des **DynamicRenderer-Objekts** ist anfänglich auf **FALSE** festgelegt.

> [!Note]  
> Wenn Sie die [**Refresh-Methode**](/previous-versions/ms826370(v=msdn.10)) des [**DynamicRenderer-Objekts**](/previous-versions/ms826345(v=msdn.10)) innerhalb eines [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) Ereignishandlers in verwaltetem Code aufrufen, legen Sie die [**ClipRectangle-Eigenschaft**](/previous-versions/ms826346(v=msdn.10)) des **DynamicRenderer-Objekts** auf die [ClipRectangle-Eigenschaft](/dotnet/api/system.windows.forms.painteventargs.cliprectangle?view=netcore-3.1) des [PaintEventArgs-Objekts](/dotnet/api/system.windows.forms.painteventargs?view=netcore-3.1) fest.

 

Das [**DynamicRenderer-Objekt**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) kann Ink-Daten vorübergehend zwischenspeichern. Um dieses Feature in verwaltetem Code zu verwenden, legen Sie die [EnableDataCache-Eigenschaft](/previous-versions/ms826349(v=msdn.10)) auf **TRUE** fest. Wenn das [**DynamicRenderer-Objekt**](/previous-versions/ms826345(v=msdn.10)) einen Aufruf seiner [**IStylusSyncPlugin.StylusUp-Methode**](/previous-versions/ms826366(v=msdn.10)) empfängt, speichert es die Strichdaten zwischen und fügt der Eingabewarteschlange als Reaktion auf das [**StylusUpData-Objekt**](/previous-versions/ms824057(v=msdn.10)) für den Strich benutzerdefinierte Stiftdaten hinzu. Die [CustomDataId-Eigenschaft](/previous-versions/ms824749(v=msdn.10)) des [**CustomStylusData-Objekts**](/previous-versions/ms824747(v=msdn.10)) wird auf den [DynamicRendererCachedDataGuid-Wert](/previous-versions/ms824744(v=msdn.10)) festgelegt, und die Data-Eigenschaft des **CustomStylusData-Objekts** enthält ein DynamicRendererCachedData-Objekt. Rufen Sie die [ReleaseCachedData-Methode](/previous-versions/ms826371(v=msdn.10)) des **DynamicRenderer-Objekts** auf, nachdem der Strich gesammelt wurde und statisch gerendert werden kann. Wenn die [**Refresh-Methode**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) aufgerufen wird, während das **DynamicRenderer-Objekt** aktiviert ist, zeichnet das **DynamicRenderer-Objekt** alle zwischengespeicherten Striche neu. Wenn die [**DataCacheEnabled-Eigenschaft**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) auf **FALSE** festgelegt ist, werden die zwischengespeicherten Strichdaten gelöscht.

Das folgende Diagramm veranschaulicht, wie das [**DynamicRenderer-Objekt**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) Daten zu den Tablettstiftdaten hinzufügt, wenn die [**DataCacheEnabled-Eigenschaft**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) des **DynamicRenderer-Objekts** festgelegt wird.

![Abbildung des dynamicrenderer-Datenflusses](images/75f4ee7b-160c-410e-bfae-dfc676a9829c.gif)

In diesem Diagramm stellt der Kreis mit dem Buchstaben "SD" ein [**StylusDown-Objekt**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) dar, und die Kreise mit dem Buchstaben "P" stellen [**Paketobjekte**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets) dar, die der Ausgabewarteschlange des [**RealTimeStylus-Objekts**](realtimestylus-class.md) bereits hinzugefügt und noch nicht an die asynchrone Plug-In-Sammlung gesendet wurden. Der Kreis mit dem Buchstaben "SU" stellt ein [**StylusUp-Objekt**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) dar, das das **RealTimeStylus-Objekt** gerade verarbeitet. Sie wird an die synchrone Plug-In-Sammlung gesendet und dann in der Ausgabewarteschlange platziert. Die Kreise mit dem Buchstaben "DR" stellen benutzerdefinierte Stiftdaten dar, die der Eingabewarteschlange durch das [**DynamicRenderer-Plug-In**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) als Reaktion auf die stiftende Benachrichtigung hinzugefügt werden, die "SU" zugeordnet ist. Die benutzerdefinierten Tablettstiftdaten mit dem Buchstaben "DR" werden dann an die synchronen Plug-Ins und dann an die Ausgabewarteschlange übergeben, bevor die nächsten Tablettstiftdaten verarbeitet werden. Der leere Kreis stellt die Position in der Ausgabewarteschlange dar, an der zukünftige Tablettstiftdaten hinzugefügt werden. Im Diagramm wird auch das Plug-In ink-collector dargestellt, das die [**ReleaseCachedData-Methode**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-releasecacheddata) des **DynamicRenderer-Objekts** aufruft, um die zwischengespeicherten Strichdaten freizugeben, nachdem das Plug-In für die Freihandsammlung den Strich verarbeitet hat.

### <a name="special-considerations"></a>Besondere Überlegungen

In der folgenden Liste werden andere Punkte beschrieben, die bei der Verwendung des [**DynamicRenderer-Objekts**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) zu berücksichtigen sind.

-   Sie sollten kein [**DynamicRenderer-Objekt**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) an mehr als ein [**RealTimeStylus-Objekt**](realtimestylus-class.md) anfügen. Sobald zwei **RealTimeStylus-Objekte,** an die das **DynamicRenderer-Objekt** angefügt ist, aktiviert sind, geschieht Folgendes.

    -   Das [**DynamicRenderer-Objekt**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) löst als Reaktion auf den zweiten Aufruf seiner [**RealTimeStylusEnabled-Methode**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) eine Ausnahme aus.
    -   Das zweite [**aktivierte RealTimeStylus-Objekt**](realtimestylus-class.md) generiert ein [**Error-Objekt**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) und benachrichtigt die verbleibenden Plug-Ins in seinen Plug-In-Auflistungen über den Fehler.
    -   Das [**DynamicRenderer-Objekt**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) beendet das Rendern von Tablettstiftdaten.

-   Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) löst eine Ausnahme aus, wenn die [**AddCustomStylusDataToQueue-Methode**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addcustomstylusdatatoqueue) aufgerufen wird, wobei der *guid-Parameter* auf den Globally Unique Identifier (GUID) DynamicRendererCachedDataGuid festgelegt ist.
-   Das [**DynamicRenderer-Objekt**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) wird als COM-Wrapper (Component Object Model) implementiert, und Sie können seine [**IStylusSyncPlugin-Schnittstellenmethoden**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) nicht direkt aufrufen. Weitere Informationen zum COM-Vorgang und zum [**RealTimeStylus-Objekt**](realtimestylus-class.md) finden Sie unter [Implementierungshinweise für die StylusInput-APIs.](implementation-notes-for-the-stylusinput-apis.md)

## <a name="custom-rendering"></a>Benutzerdefiniertes Rendering

Sie können ein eigenes Plug-In für dynamische Renderer erstellen, indem Sie ein synchrones Plug-In erstellen, das die [**Benachrichtigungen StylusDown,**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) [**Packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)und [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) abonniert. Das Plug-In kann dann den Strich rendern, während er gezeichnet wird. Dies kann eine Möglichkeit sein, ein Auswahltool zu implementieren, das z. B. eine Freiformauswahl oder ein Auswahlfeld verwendet.

 

 
