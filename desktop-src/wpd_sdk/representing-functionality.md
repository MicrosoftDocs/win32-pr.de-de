---
description: Darstellen von Funktionen
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: Darstellen von Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f969bcf6352cd4eef02c1580a93bebcbf769953e2ae658243b4499e6d1ca763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842702"
---
# <a name="representing-functionality"></a>Darstellen von Funktionen

Funktionale Objekte sind vorhanden, um Funktionsfunktionen eines Geräts zu identifizieren oder logisch zu gruppieren. Eine Anwendung kann z. B. erkennen, dass ein Gerät SMS unterstützt, indem es nach dem funktionalen SMS-Objekt sucht. Auf ähnliche Weise kann die Anwendung sehen, dass ein Gerät über Kamerafunktionen verfügt, indem nach dem Funktionsobjekt Still Image Capture gesucht wird.

Diese flexible Objektdarstellung ermöglicht eine einfache Unterstützung für Geräte mit Funktionen mit mehreren Funktionen. Treiber können einfach alle funktionalen Objekte verfügbar machen, die ihr Gerät darstellen. Dies ist präziser als die Verwendung herkömmlicher Geräteklassen. Die Objektdarstellung hilft auch dabei, überlappende funktionale Teile zu isolieren. Einige Smartphones verfügen beispielsweise über zwei Kameras oder vier Speicher.

Im Windows 7-Betriebssystem erweitern Dienste funktionale Objekte, indem sie umfangreiche Abfragen von Funktionen und eine abstrakte Gruppierung von Inhalten bereitstellen. Anwendungen können Dienste verwenden, um Gerätefunktionen zu ermitteln und effizienter mit Inhalten zu interagieren. Beispielsweise kann eine Anwendung sehen, dass ein Gerät die Funktionen zur Synchronisierung von Kontakten unterstützt, indem es nach einem Contacts-Dienstobjekt sucht und alle Kontakte als untergeordnete Objekte des Dienstobjekts finden kann, ohne die Speicherhierarchie rekursiv durchsuchen zu müssen.

Dienste ermöglichen es Anwendungen auch, benutzerdefiniertes Verhalten auf einem Gerät zu ermitteln und aufzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anwendungsübersicht**](application-overview.md)
</dt> </dl>

 

 



