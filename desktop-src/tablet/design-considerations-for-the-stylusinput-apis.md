---
description: Übersicht über Überlegungen zum Entwerfen einer Anwendung, die die StylusInput-Anwendungs Programmierschnittstellen (Application Programming Interfaces, APIs) verwendet.
ms.assetid: cb68a6bb-dd38-4dfb-bbbb-b5d846e5aa0a
title: Entwurfs Überlegungen für die StylusInput-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff526d8e073f00156730d79ea2caf1a02c5e5af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348688"
---
# <a name="design-considerations-for-the-stylusinput-api"></a>Entwurfs Überlegungen für die StylusInput-API

Im folgenden finden Sie Entwurfs Überlegungen für die StylusInput-API.

-   Sie können die [**windowinputrechteck**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) -Eigenschaft des [**RealTimeStylus**](realtimestylus-class.md) -Objekts und die [**clipRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_cliprectangle) -Eigenschaft des [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Objekts aktualisieren, während der Stift nicht angezeigt wird. Dies kann hilfreich sein, wenn Sie einen dynamischen Zeichnungs Bereich haben möchten, während die Anwendung frei Hand Eingaben sammelt.
-   Um die Wiederverwendung und Wartung von Plug-in-Code zu optimieren, sollten Plug-ins keine Aufrufe direkt an die Anwendung senden, sondern das [**CustomStylusData**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-customstylusdataadded) ([customestylusdata](/previous-versions/ms824747(v=msdn.10)) -Objekt in verwaltetem Code) verwenden, um mit der Anwendung zu kommunizieren.
-   Die Plug-in-Auflistungen des [**RealTimeStylus**](realtimestylus-class.md) -Objekts sind geordnet. Die relative Position der Plug-ins in diesen Auflistungen kann sehr wichtig sein. Beispielsweise sollte ein Plug-in, das Paketinformationen ändert, wahrscheinlich der synchronen Plug-in-Sammlung vor einem Dynamic-Renderer-Plug-in hinzugefügt werden.
-   Die Möglichkeit, dem Datenstrom des Tablettstifts benutzerdefinierte Tablettstiftdaten hinzuzufügen, sollte sparsam verwendet werden. Verwenden Sie diese Funktion nur, wenn ein anderes Plug-in diese Informationen als Teil des Datenstroms empfangen muss. Vermeiden Sie außerdem das Hinzufügen von benutzerdefinierten Tablettstiftdaten als Reaktion auf andere benutzerdefinierte Tablettstiftdaten, die im Plug-in eingehen, da dadurch eine Endlosschleife erstellt werden kann.
-   Plug-in-Auflistungen können geändert werden, während das [**RealTimeStylus**](realtimestylus-class.md) -Objekt aktiviert ist. Dies kann jedoch die Vorhersage des Verhaltens ihrer Anwendung erschweren. Wenn ein Plug-in hinzugefügt wird, während das **RealTimeStylus** -Objekt aktiviert ist, ruft das **RealTimeStylus** -Objekt das Plug-in Microsoft. StylusInput. IStylusSyncPlugin auf. [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) -Methode (entweder die [Microsoft. StylusInput. IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) oder die [Microsoft. StylusInput. IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) -Methode in verwaltetem Code). Wenn ein Plug-in entfernt wird, während das **RealTimeStylus** -Objekt aktiviert ist, das **RealTimeStylus** -Objekt ruft die [**realtimestylusdeaktiviert**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) -Methode des Plug-Ins auf (entweder die [Microsoft. StylusInput. IStylusSyncPlugin. realtimestylusdeaktivierte](/previous-versions/ms824757(v=msdn.10)) Methode oder die [Microsoft. StylusInput. IStylusAsyncPlugin. realtimestylusdeaktiviert](/previous-versions/ms824774(v=msdn.10)) -Methode in verwaltetem Code). Dadurch kann das Plug-in seinen ordnungsgemäßen Zustand beibehalten, ohne die [**aktivierte**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_enabled) Eigenschaft des **RealTimeStylus** -Objekts überprüfen zu müssen. Wenn ein Plug-in hinzugefügt wird, während das **RealTimeStylus** -Objekt aktiviert ist, enthalten die Plug-in-Daten, die das Plug-in empfängt, möglicherweise nicht genügend Informationen, um den Kontext der anfänglichen Daten adäquat festzulegen. Beispielsweise könnte das neu hinzugefügte Plug-in mit dem Empfang von Paketdaten von einem Stift beginnen, der einen Mittel Strich ist. Ebenso kann ein Plug-in, das beim Aktivieren des **RealTimeStylus** -Objekts entfernt wurde, nicht ausreichen, um die Verarbeitung der Daten abzuschließen.
    > [!Note]  
    > Setzen Sie für die Gesamtstabilität den internen Zustand eines Plug-ins zurück, wenn entweder die zugehörige [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) -Methode oder die [**realtimestylusdeaktivierte**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) -Methode aufgerufen wird.

     

-   Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt löst eine Ausnahme aus, wenn ein Plug-in die Plug-in-Sammlung ändert, an die es angefügt ist. Dies geschieht nur, wenn das Plug-in Dies bewirkt, während es vom **RealTimeStylus** -Objekt als Member dieser Auflistung aufgerufen wird.

 

 
