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

Funktionale Objekte sind vorhanden, um Featurefunktionen eines Geräts zu identifizieren oder logisch zu gruppieren. Beispielsweise kann eine Anwendung sehen, dass ein Gerät SMS unterstützt, indem sie nach dem Funktionsobjekt SMS sucht. Auf ähnliche Weise kann die Anwendung erkennen, dass ein Gerät über Kamerafunktionen verfügt, indem sie nach dem Funktionalen Objekt Still Image Capture sucht.

Diese flexible Objektdarstellung ermöglicht eine einfache Unterstützung für Geräte mit Funktionen mit mehreren Funktionen. Treiber können einfach alle funktionalen Objekte verfügbar machen, die ihr Gerät darstellen. Dies ist präziser als die Verwendung herkömmlicher Geräteklassen. Die Objektdarstellung hilft auch dabei, überlappende funktionale Teile zu isolieren. Einige Telefone können z. B. zwei Kameras oder vier Speicher haben.

Im Windows 7 erweitern Dienste funktionale Objekte, indem sie umfangreiche Abfragen von Funktionen und eine abstrakte Gruppierung von Inhalten bereitstellen. Anwendungen können Dienste verwenden, um Gerätefunktionen zu entdecken und effizienter mit Inhalten zu interagieren. Beispielsweise kann eine Anwendung sehen, dass ein Gerät die Funktionen zur Synchronisierung von Kontakten unterstützt, indem nach einem Contacts-Dienstobjekt gesucht wird, und alle Kontakte als untergeordnete Objekte des Dienstobjekts finden, ohne die Speicherhierarchie rekursiv durchsuchen zu müssen.

Mit Diensten können Anwendungen auch benutzerdefiniertes Verhalten auf einem Gerät erkennen und aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anwendungsübersicht**](application-overview.md)
</dt> </dl>

 

 



