---
description: Übersicht über Überlegungen zum Entwerfen einer Anwendung, die die Anwendungsprogrammierschnittstellen (APIs) stylusInput verwendet.
ms.assetid: cb68a6bb-dd38-4dfb-bbbb-b5d846e5aa0a
title: Entwurfsüberlegungen für die StylusInput-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabd97a5bad203dd23611acf3d6cb07bead1e1744a10b9ac39afe8a53e65597d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936630"
---
# <a name="design-considerations-for-the-stylusinput-api"></a>Entwurfsüberlegungen für die StylusInput-API

Im Folgenden finden Sie Entwurfsüberlegungen für die StylusInput-API.

-   Sie können die [**WindowInputRectangle-Eigenschaft**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) des [**RealTimeStylus-Objekts**](realtimestylus-class.md) und die [**ClipRectangle-Eigenschaft**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_cliprectangle) des [**DynamicRenderer-Objekts**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) aktualisieren, während der Stift unten ist. Dies kann nützlich sein, wenn Sie einen dynamischen Zeichnungsbereich verwenden möchten, während die Anwendung Ink sammelt.
-   Um die Wiederverwendung und Wartung von Plug-In-Code zu optimieren, sollten Plug-Ins die Anwendung nicht direkt aufrufen, sondern das [**CustomStylusData-Objekt**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-customstylusdataadded) [(CustomeStylusData-Objekt](/previous-versions/ms824747(v=msdn.10)) in verwaltetem Code) für die Kommunikation mit der Anwendung verwenden.
-   Die Plug-In-Auflistungen des [**RealTimeStylus-Objekts**](realtimestylus-class.md) werden geordnet. Die relative Position Ihrer Plug-Ins innerhalb dieser Auflistungen kann sehr wichtig sein. Beispielsweise sollte ein Plug-In, das Paketinformationen ändert, wahrscheinlich der synchronen Plug-In-Auflistung vor einem Plug-In mit dynamischem Renderer hinzugefügt werden.
-   Die Möglichkeit, dem Datenstrom des Tablettstifts benutzerdefinierte Tablettstiftdaten hinzuzufügen, sollte nur wenig verwendet werden. Verwenden Sie dieses Feature nur, wenn ein anderes Plug-In diese Informationen als Teil des Datenstroms empfangen muss. Vermeiden Sie außerdem das Hinzufügen benutzerdefinierter Stiftdaten als Reaktion auf andere benutzerdefinierte Stiftdaten, die in das Plug-In kommen, da dies eine Endlosschleife erzeugen kann.
-   Plug-In-Sammlungen können geändert werden, während das [**RealTimeStylus-Objekt**](realtimestylus-class.md) aktiviert ist. Dies kann jedoch die Vorhersage des Verhaltens Ihrer Anwendung erschweren. Wenn ein Plug-In hinzugefügt wird, während das **RealTimeStylus-Objekt** aktiviert ist, ruft das **RealTimeStylus-Objekt** microsoft.StylusInput.IStylusSyncPlugin des Plug-Ins auf. [**RealTimeStylusEnabled-Methode**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) (entweder die [Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusEnabled-](/previous-versions/ms824758(v=msdn.10)) oder [die Microsoft.StylusInput.IStylusAsyncPlugin.RealTimeStylusEnabled-Methode](/previous-versions/ms824775(v=msdn.10)) in verwaltetem Code). Wenn ein Plug-In entfernt wird, während das **RealTimeStylus-Objekt** aktiviert ist, ruft das **RealTimeStylus-Objekt** die [**RealTimeStylusDisabled-Methode**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) des Plug-Ins auf (entweder die [Microsoft.StylusInput.IStylusSyncPlugin.RealTimeStylusDisabled-](/previous-versions/ms824757(v=msdn.10)) oder [die Microsoft.StylusInput.IStylusAsyncPlugin.RealTimeStylusDisabled-Methode](/previous-versions/ms824774(v=msdn.10)) in verwaltetem Code). Dadurch kann das Plug-In seinen richtigen Zustand erhalten, ohne die [**Enabled-Eigenschaft**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_enabled) des **RealTimeStylus-Objekts überprüfen zu** müssen. Wenn ein Plug-In hinzugefügt wird, während das **RealTimeStylus-Objekt** aktiviert ist, enthalten die plug-in-Daten, die das Plug-In empfängt, möglicherweise nicht genügend Informationen, um den Kontext der ursprünglichen Daten angemessen zu erstellen. Das neu hinzugefügte Plug-In könnte z. B. beginnen, Paketdaten von einem Stift mit Strichmitte zu empfangen. Wenn ein Plug-In entfernt wird, während das **RealTimeStylus-Objekt** aktiviert ist, sind die vom Plug-In empfangenen Plug-In-Daten möglicherweise nicht ausreichend, um die Verarbeitung der Daten fertig zu stellen.
    > [!Note]  
    > Setzen Sie den internen Zustand eines Plug-Ins zurück, wenn entweder seine [**RealTimeStylusEnabled-**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) oder [**RealTimeStylusDisabled-Methode**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) aufgerufen wird.

     

-   Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) löst eine Ausnahme aus, wenn ein Plug-In die Plug-In-Auflistung ändert, an die es angefügt ist. Dies geschieht nur, wenn das Plug-In dies tut, während es vom **RealTimeStylus-Objekt** als Member dieser Auflistung aufgerufen wird.

 

 
