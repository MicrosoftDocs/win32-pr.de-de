---
description: Wpdservicesapisample-Anwendung
ms.assetid: 857753f7-bca1-4f4a-a8f9-0b2232e2f0dc
title: Wpdservicesapisample-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cbf6c6e4647744ae45f43b5d4139cbf7f9dc55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347379"
---
# <a name="wpdservicesapisample-application"></a>Wpdservicesapisample-Anwendung

Ein Geräte Dienst ist eine Erweiterung eines funktionalen Objekts: Zusätzlich zur logischen Gruppierung von Gerätefunktionen bietet ein Geräte Dienst Anwendungen die Möglichkeit, diese Funktionen Programm gesteuert zu ermitteln.

Die Beispielanwendung wpdservicesapisample ist eine Befehlszeilen-Desktop Anwendung, mit der Sie kontaktdienste auf Geräten untersuchen können, die mit Ihrem Computer verbunden sind. Sie können diese Dienste durchsuchen, indem Sie unterstützt: Formate, Ereignisse, Methoden und abstrakte Dienste auflisten. Sie können diese Anwendung auch verwenden, um die Eigenschaften für einen bestimmten Kontakt Dienst abzurufen und Methoden aufzurufen, die von diesem Dienst unterstützt werden.

Wenn Sie noch kein Gerät haben, das Kontakte Dienste unterstützt, können Sie wpdservicesapisample weiterhin ausführen, wenn Sie zunächst den wpdservicesampledriver installieren, der im Windows-Treiberkit enthalten ist.

Die Beispielanwendung wpdservicesapisample umfasst die folgenden Dateien:



| **File**                | **Beschreibung**                                                                                                                                                                                           |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Contentenumeration. cpp"  | Enthält Methoden, die den Inhalt eines bestimmten Contacts-Dienstanbieter aufzählen.                                                                                                                                  |
| Contentproperties. cpp   | Enthält Methoden, die Eigenschaften für einen bestimmten Kontakt Dienst lesen und schreiben.                                                                                                                              |
| Servicecapabili. cpp | Enthält die Methoden, mit denen die unterstützten Formate, Ereignisse und abstrakten Dienste abgerufen werden, die von einem bestimmten Kontakt Dienst unterstützt werden.                                                                   |
| Serviceenumeration. cpp  | Enthält die Hilfsfunktionen, die Geräteinformationen abrufen, z. b. den Geräte freundlichen Namen oder die unterstützten kontaktdienste.                                                                       |
| Servicemethods. cpp      | Enthält die Methoden, die Methoden abrufen und aufrufen, die von einem bestimmten Kontakt Dienst unterstützt werden.                                                                                                              |
| stdafx.cpp              | Schließt die Standard Dateien ein.                                                                                                                                                                              |
| Wpdserviceapisample. cpp | Hostet die **\_ Tmain** -Start Funktion, die die lokale **domenu** -Funktion aufruft, die eine Liste der verfügbaren Geräte und Tasks anzeigt und die Funktion aufruft, die für die Menü Auswahl des Benutzers geeignet ist. |



 


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiele](sample.md)
</dt> </dl>

 

 



