---
description: WpdApiSample-Anwendung
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: WpdApiSample-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef1741f2cad07e28bee514cf6109cdbbf7347966e1a8184a88a11936cbccdcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963469"
---
# <a name="wpdapisample-application"></a>WpdApiSample-Anwendung

Die WpdApiSample-Beispielanwendung ist eine Befehlszeilendesktopanwendung, mit der Sie verbundene Geräte aufzählen, Geräte untersuchen, Objekte nach Eigenschaften und Attributen abfragen, Objekte senden und abrufen können usw. Beim Start öffnet die Anwendung ein Befehlsfenster, in dem die Aufgaben aufgeführt sind, die Sie ausführen können.

Die WpdApiSample-Beispielanwendung enthält die folgenden Dateien:



| **File**               | **Beschreibung**                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentEnumeration.cpp | Enthält Funktionen, die alle Objekte auf einem Gerät aufzählen.                                                                                                                                            |
| ContentProperties.cpp  | Enthält Funktionen, mit denen Objekteigenschaften gelesen und geschrieben und Massenanforderungen für Eigenschaftensatz-/Get-Anforderungen gestellt werden.                                                                                                         |
| ContentTransfer.cpp    | Enthält Funktionen, die Inhalte an das gerät oder vom Gerät übertragen, Objekttypanforderungen lesen und einen Ordner auf dem Gerät erstellen.                                                                         |
| DeviceCapabilities.cpp | Enthält Funktionen zum Auflisten der Funktionsobjekttypen auf dem Gerät, zum Auflisten der von den einzelnen funktionalen Objekttypen unterstützten Inhaltstypen und zum Anzeigen von Renderingobjektprofilen.                             |
| DeviceEnumeration.cpp  | Listet die Anzeigenamen, Hersteller und Beschreibungen aller verbundenen Geräte auf.                                                                                                                       |
| DeviceEvents.cpp       | Enthält Funktionen, die Geräteereignisse und deren Parameter protokollieren, wenn Ereignisse ausgelöst werden.                                                                                                                 |
| stdafx.cpp             | Enthält die Standarddateien.                                                                                                                                                                              |
| WpdApiSample.cpp       | Hostet die **\_ tmain-Startfunktion,** die die lokale **DoMenu-Funktion** aufruft, die eine Liste der verfügbaren Geräte und Aufgaben anzeigt und die für die Menüauswahl des Benutzers geeignete Funktion aufruft. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel](sample.md)
</dt> </dl>

 

 



