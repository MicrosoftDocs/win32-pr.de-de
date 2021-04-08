---
description: Darstellen von Funktionen
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: Darstellen von Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101614592224a1a5ac079b1f9c3dc89cea9afefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866504"
---
# <a name="representing-functionality"></a>Darstellen von Funktionen

Funktionale Objekte sind vorhanden, um Funktions Funktionen eines Geräts zu identifizieren oder logisch zu gruppieren. Beispielsweise kann eine Anwendung sehen, dass ein Gerät SMS unterstützt, indem er nach dem SMS-Funktions Objekt sucht. Ebenso kann die Anwendung sehen, dass ein Gerät über Kamerafunktionen verfügt, indem es nach dem noch funktionalen Objekt der Bild Erfassung sucht.

Diese flexible Objektdarstellung ermöglicht die einfache Unterstützung von Geräten mit Funktionen mit mehreren Funktionen. Treiber können einfach alle funktionalen Objekte verfügbar machen, die Ihr Gerät darstellen, was präziser als die Verwendung herkömmlicher Geräteklassen ist. Die Objektdarstellung hilft auch dabei, überlappende funktionale Teile zu isolieren. einige Telefone können z. b. über zwei Kameras oder vier Storages verfügen.

Im Betriebssystem Windows 7 erweitern Dienste funktionale Objekte durch die Bereitstellung umfangreicher Abfragen von Funktionen und eine abstrakte Gruppierung von Inhalten. Anwendungen können-Dienste verwenden, um Gerätefunktionen zu ermitteln und effizienter mit Inhalten zu interagieren. Beispielsweise kann eine Anwendung sehen, dass ein Gerät die Funktionen zum Synchronisieren von Kontakten unterstützt, indem es nach einem Contact Service-Objekt sucht und alle Kontakte als untergeordnete Objekte des Dienst Objekts findet, ohne dass die Speicher Hierarchie rekursiv durchsucht werden muss.

Dienste ermöglichen Anwendungen auch das ermitteln und Aufrufen von benutzerdefiniertem Verhalten auf einem Gerät.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anwendungs Übersicht**](application-overview.md)
</dt> </dl>

 

 



