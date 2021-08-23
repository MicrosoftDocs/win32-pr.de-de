---
title: GUID-Erstellung und -Optimierungen
description: GUID-Erstellung und -Optimierungen
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dc1b0cc52312768759daca35824f8e7e515629131ac2c301a17d7ae99d6455
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731430"
---
# <a name="guid-creation-and-optimizations"></a>GUID-Erstellung und -Optimierungen

Da eine CLSID wie ein Schnittstellenbezeichner (IID) eine GUID ist, verfügt keine andere Klasse unabhängig davon, wer sie schreibt, über eine doppelte CLSID. Server-Implementierer erhalten CLSIDs in der Regel über die [**CoCreateGuid-Funktion.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) Diese Funktion erzeugt garantiert eindeutige CLSIDs, sodass Server-Implementierer auf der ganzen Welt ihre Software unabhängig entwickeln und bereitstellen können, ohne versehentliche Kollisionen mit Software zu haben, die von anderen geschrieben wurde.

Die Verwendung eindeutiger CLSIDs vermeidet die Möglichkeit von Namenskollisionen zwischen Klassen, da CLSIDs in keiner Weise mit den Namen verbunden sind, die in der zugrunde liegenden Implementierung verwendet werden. Beispielsweise können zwei verschiedene Anbieter Klassen mit dem Namen "StackClass" schreiben, aber jeder hat eine eindeutige CLSID und konnte daher nicht verwechselt werden.

COM muss häufig GUIDs (IIDs und CLSIDs) einigen beliebig großen Mengen anderer Werte zuordnen. Als Anwendungsentwickler können Sie solche Suchvorgänge beschleunigen und dadurch die Systemleistung verbessern, indem Sie die GUIDs für Ihre Anwendung als Block aus aufeinanderfolgenden Werten generieren.

Die effizienteste Methode zum Generieren eines Blocks von aufeinanderfolgenden GUIDs ist die Ausführung des Hilfsprogramms uuidgen mit den Schaltern -n und -x, die einen Block von UUIDs generieren, von denen jeder um eins erhöht wird.

Wenn Sie z. B. eingeben würden

**uuidgen -n5 -x**

Das Hilfsprogramm uuidgen generiert einen UUIDs-Block ähnlich dem folgenden:

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

Eine Methode zum Generieren und Nachverfolgen von GUIDs für ein gesamtes Projekt beginnt mit dem Generieren eines Blocks mit einer beliebig großen Anzahl von UUIDs, z. B. 500. Wenn Sie z. B. eingeben würden

**uuidgen -n500 -x > guids.txt**

Das Hilfsprogramm generiert 500 aufeinander folgende UUIDs und schreibt sie in die angegebene Textdatei. Sie können diese Datei dann in die Quellstruktur einchecken und ein einzelnes Repository für alle GUIDs bereitstellen, die in einem Projekt verwendet werden sollen. Da Benutzer GUIDs für ihre Teile des Projekts benötigen, können sie die Datei auschecken, wie viele GUIDs sie benötigen, sie als übernommen markieren und einen Hinweis darüber hinterlassen, wo sie sie im Code oder in der "Spezifikation" verwenden.

Zusätzlich zur Verbesserung der Systemleistung hat das Generieren von Blöcken aufeinanderfolgender GUIDs auf diese Weise die folgenden Vorteile:

-   Mit einer zentralen Datei, die alle GUIDs für eine Anwendung enthält, können Sie leicht nachverfolgen, welche GUIDs für was und welche Personen sie verwenden.
-   Ein Block von aufeinander folgenden GUIDs, die einer bestimmten Anwendung zugeordnet sind, hilft Entwicklern und Testern, interne GUIDs während des Debuggens zu erkennen, und erleichtert es, sie in der Systemregistrierung zu finden, da sie sequenziell gespeichert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Serveraufgaben](com-server-responsibilities.md)
</dt> </dl>

 

 




