---
description: Das RealTimeStylus-Objekt erfasst inhärent keine Ink-Objekte. Um den RealTimeStylus zum Erfassen von Ink zu verwenden, erstellen Sie ein Ink-Collector-Plug-In.
ms.assetid: 9a29525d-714a-431e-bb6f-4705d658537b
title: Ink-Collection-Plug-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64966e2d088e9145fa4a0c0b29a7f7cc787b8435a3e4a609e75eae27b4e25524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967209"
---
# <a name="ink-collection-plug-ins"></a>Ink-Collection-Plug-Ins

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) erfasst inhärent keine Ink-Objekte. Um den **RealTimeStylus zum** Erfassen von Ink zu verwenden, erstellen Sie ein Ink-Collector-Plug-In.

Im Folgenden finden Sie ein minimales Szenario für die Verwendung des [**RealTimeStylus-Objekts**](realtimestylus-class.md) in einem Formular, das Ink sammelt.

1.  Erstellen Sie ein Formular, das die [**IStylusAsyncPlugin-Schnittstelle**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) implementiert.
2.  Erstellen Sie [**ein RealTimeStylus-Objekt,**](realtimestylus-class.md) und fügen Sie es an ein Steuerelement im Formular an.
3.  Legen Sie das Interesse an den Benachrichtigungen StylusDown, Packets und StylusUp in der [DataInterest-Eigenschaft des Formulars](/previous-versions/ms574886(v=vs.100)) fest.
4.  Fügen Sie in den [**Methoden "StylusDown",**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) [**"Packets"**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)und [**"StylusUp"**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) des Formulars Code hinzu, um den Stiftdown, die Pakete und die Stift-Up-Benachrichtigungen zu verarbeiten, die vom [**RealTimeStylus-Objekt**](realtimestylus-class.md) des Formulars gesendet werden. Dieser Code sollte die Stiftdaten speichern und die Striche erstellen und speichern.

Ein Beispiel für eine solche Anwendung finden Sie im [RealTimeStylus Ink Collection Sample Sample (Beispiel für die Sammlung von RealTimeStylus-Ink-Daten).](realtimestylus-ink-collection-sample.md)

> [!Note]  
> Wenn ein [DisplaySettingsChanged-Ereignis](/dotnet/api/microsoft.win32.systemevents.displaysettingschanged?view=dotnet-plat-ext-3.1) auftritt, rufen Sie die [**ModifyDrawingAttributes-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) der gesammelten Striche in einem DisplaySettingsChanged-Ereignishandler auf, um die [Eigenschaften Width](/previous-versions/ms582112(v=vs.100)) und [Height](/previous-versions/ms582106(v=vs.100)) neu zu berechnen. Dies ist erforderlich, um mögliche dpi-Änderungen (Dots per Inch) zu berücksichtigen, die sich aus dem DisplaySettingsChanged-Ereignis ergeben.

 

## <a name="ink-collection-and-recognizers"></a>Ink-Sammlung und -Recognizers

Weder die Ink-Analyse noch die Handschrifterkennung ist eine Funktion des [**RealTimeStylus-Objekts.**](realtimestylus-class.md) Wenn das Ink-Collector-Plug-In Ins sammelt, können Sie die Ink-Klasse in [ein RecognizerContext-](/previous-versions/ms552546(v=vs.100)) oder [Divider-Objekt](/previous-versions/ms583616(v=vs.100)) kopieren, wenn Sie die Ink-Klasse erkennen möchten. Weitere Informationen zur Erkennung und Ink-Analyse finden Sie unter [About Handwriting Recognition](about-handwriting-recognition.md) or [The Divider Object](the-divider-object.md).

## <a name="static-rendering"></a>Statisches Rendering

Fügen Sie ein [DynamicRenderer-Objekt](/previous-versions/ms575176(v=vs.100)) an das [**RealTimeStylus-Objekt**](realtimestylus-class.md) an, um Ink während der Datensammelung zu rendern. Verwenden Sie zum Rendern von Ink nach dem Sammeln ein [Renderer-Objekt,](/previous-versions/ms552630(v=vs.100)) um die Striche auf das entsprechende [Graphics-Objekt zu](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1) zeichnen. Weitere Informationen zum DynamicRenderer-Objekt finden Sie unter [Dynamic-Renderer Plug-Ins](dynamic-renderer-plug-ins.md). Ein Beispiel für statisches und dynamisches Rendering finden Sie unter [RealTimeStylus Ink Collection Sample](realtimestylus-ink-collection-sample.md).

 

 
