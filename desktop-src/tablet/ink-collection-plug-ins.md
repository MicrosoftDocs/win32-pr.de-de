---
description: Das RealTimeStylus-Objekt sammelt nicht von Hand frei Hand Eingaben. Wenn Sie den RealTimeStylus zum Sammeln von frei Hand Eingaben verwenden möchten, erstellen Sie ein frei Hand Sammler-Plug-in.
ms.assetid: 9a29525d-714a-431e-bb6f-4705d658537b
title: Ink-Collection-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc060adf172938612e8f16f9a694e4ee3e1a7b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862099"
---
# <a name="ink-collection-plug-ins"></a>Ink-Collection-Plug-ins

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt sammelt nicht von Hand frei Hand Eingaben. Wenn Sie den **RealTimeStylus** zum Sammeln von frei Hand Eingaben verwenden möchten, erstellen Sie ein frei Hand Sammler-Plug-in.

Im folgenden finden Sie ein minimales Szenario für die Verwendung des [**RealTimeStylus**](realtimestylus-class.md) -Objekts in einem Formular, das frei Hand Eingaben sammelt.

1.  Erstellen Sie ein Formular, das die [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle implementiert.
2.  Erstellen Sie ein [**RealTimeStylus**](realtimestylus-class.md) -Objekt, und fügen Sie es an ein Steuerelement im Formular an.
3.  Legen Sie Interesse an den StylusDown-, Paketen-und StylusUp-Benachrichtigungen in der [DataInterest](/previous-versions/ms574886(v=vs.100)) -Eigenschaft des Formulars fest.
4.  Fügen Sie in den [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown)-,- [**Paketen**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)-und [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) -Methoden des Formulars Code hinzu, um die tablettstiftdown-, Pakete-und tablettstiftbenachrichtigungen zu verarbeiten, die aus dem [**RealTimeStylus**](realtimestylus-class.md) -Objekt des Formulars gesendet werden. In diesem Code sollten die Stift Daten gespeichert und die Striche erstellt und gespeichert werden.

Ein Beispiel für eine solche Anwendung finden Sie im Beispiel zum Beispiel für eine [RealTimeStylus Ink Collection](realtimestylus-ink-collection-sample.md) .

> [!Note]  
> Wenn ein [displaysettingschangi-Ereignis](/dotnet/api/microsoft.win32.systemevents.displaysettingschanged?view=dotnet-plat-ext-3.1) auftritt, wird [**die ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) -Methode der gesammelten Striche in einem displaysettingschge-Ereignishandler aufgerufen, um die [Width](/previous-versions/ms582112(v=vs.100)) -und [height](/previous-versions/ms582106(v=vs.100)) -Eigenschaften neu zu berechnen. Dies ist erforderlich, um mögliche dpi-Änderungen (dpi, dpi, dpi) zu berücksichtigen, die sich aus dem displaysettingschge-Ereignis ergeben.

 

## <a name="ink-collection-and-recognizers"></a>Frei Hand Erfassung und-Erkennung

Weder die Ink-Analyse noch die Handschrifterkennung ist eine Funktion des [**RealTimeStylus**](realtimestylus-class.md) -Objekts. Wenn das frei Hand Sammler-Plug-in frei Hand Eingaben sammelt, oder wenn Sie die frei Hand Eingaben erkennen möchten, können Sie die frei Hand Eingaben in ein [Erkennungs Kontext](/previous-versions/ms552546(v=vs.100)) -oder unter [Teiler](/previous-versions/ms583616(v=vs.100)) -Objekt kopieren. Weitere Informationen zu Erkennungs-und Handschrift Analysen finden Sie unter Informationen [zur Handschrifterkennung](about-handwriting-recognition.md) oder [zum Divider-Objekt](the-divider-object.md).

## <a name="static-rendering"></a>Statisches Rendering

Um frei Hand Eingaben zu renderarbeiten, während diese gesammelt werden, fügen Sie ein [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) -Objekt an das [**RealTimeStylus**](realtimestylus-class.md) -Objekt an. Um frei Hand Eingaben zu Renderern, nachdem Sie gesammelt wurden, verwenden Sie ein [Rendererobjekt](/previous-versions/ms552630(v=vs.100)) , um die Striche in das entsprechende [Grafik](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1) Objekt zu zeichnen. Weitere Informationen zum DynamicRenderer-Objekt finden Sie unter [Dynamic-Renderer-Plug-ins](dynamic-renderer-plug-ins.md). Ein Beispiel für statisches und dynamisches Rendering finden Sie unter [Beispiel für eine RealTimeStylus Ink Collection](realtimestylus-ink-collection-sample.md).

 

 
