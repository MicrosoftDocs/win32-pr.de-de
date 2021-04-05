---
description: Wpdapisample-Anwendung
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: Wpdapisample-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c384d542c9b93ac733c91ee249938d744e40ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751184"
---
# <a name="wpdapisample-application"></a>Wpdapisample-Anwendung

Die Beispielanwendung wpdapisample ist eine Desktop Anwendung für die Befehlszeile, die es Ihnen ermöglicht, verbundene Geräte aufzulisten, Geräte zu durchsuchen, Objekte für Eigenschaften und Attribute abzufragen, Objekte zu senden und abzurufen usw. Beim Start öffnet die Anwendung ein Befehlsfenster, in dem die Aufgaben aufgelistet sind, die Sie ausführen können.

Die Beispielanwendung wpdapisample umfasst die folgenden Dateien:



| **File**               | **Beschreibung**                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Contentenumeration. cpp" | Enthält Funktionen, die alle-Objekte auf einem Gerät auflisten.                                                                                                                                            |
| Contentproperties. cpp  | Enthält Funktionen, die Objekteigenschaften lesen und schreiben und Bulk-Eigenschaften festgelegte/Get-Anforderungen machen.                                                                                                         |
| Contenttransfer. cpp    | Enthält Funktionen, die Inhalte auf das oder vom Gerät übertragen, Objekttyp Anforderungen lesen und einen Ordner auf dem Gerät erstellen.                                                                         |
| Devicecapabili. cpp | Enthält Funktionen zum Auflisten der funktionalen Objekttypen auf dem Gerät, zum Auflisten der von jedem funktionalen Objekttyp unterstützten Inhaltstypen und zum Anzeigen von renderingobjektprofilen.                             |
| Deviceenumeration. cpp  | Listet die anzeigen Amen, Hersteller und Beschreibungen aller verbundenen Geräte auf.                                                                                                                       |
| Deviceevents. cpp       | Enthält Funktionen, die Geräte Ereignisse und ihre Parameter protokollieren, wenn Ereignisse ausgelöst werden.                                                                                                                 |
| stdafx.cpp             | Schließt die Standard Dateien ein.                                                                                                                                                                              |
| Wpdapisample. cpp       | Hostet die **\_ Tmain** -Start Funktion, die die lokale **domenu** -Funktion aufruft, die eine Liste der verfügbaren Geräte und Tasks anzeigt und die Funktion aufruft, die für die Menü Auswahl des Benutzers geeignet ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel](sample.md)
</dt> </dl>

 

 



