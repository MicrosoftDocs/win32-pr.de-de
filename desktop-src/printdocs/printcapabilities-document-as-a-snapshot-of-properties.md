---
title: Dokument als Momentaufnahme von Eigenschaften
description: Überprüfen Sie das PrintCapabilities-Dokument als Momentaufnahme von Eigenschaften. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a031334e820b140cb27f7c293741a84e0d8a89c6c9d1c47f89cf83a87a2d3cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033908"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a>PrintCapabilities-Dokument als Momentaufnahme von Eigenschaften

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Das von PrintCapabilities beschriebene Gerät kann Eigenschaften aufweisen, die vom Zustand oder der Konfiguration des Geräts abhängen. Während PrintCapabilities den vollständigen Konfigurationsraum eines Geräts darstellt, erzeugt der PrintCapabilities-Anbieter eine konfigurationsabhängige Instanz der PrintCapabilities-Datei, die als PrintCapabilities-Dokument bezeichnet wird. Dieses konfigurationsabhängige PrintCapabilities-Dokument vermeidet, dass das PrintCapabilities-Schema mit der Komplexität der Darstellung mehrwertigen Daten belastet wird. Noch wichtiger ist, dass alle Property- und ScoredProperty-Instanzen in einem PrintCapabilities-Dokument einwertig sein müssen, um einen Consumer des PrintCapabilities-Dokuments von der Belastung zu entlasten, den entsprechenden Wert aus einer mehrwertigen Datendarstellung zu extrahieren. Anders ausgedrückt: Jede Property- und ScoredProperty-Instanz in einem PrintCapabilities-Dokument muss relativ zur Eingabekonfiguration einen festen Wert haben. Jedes PrintCapabilities-Dokument kann als Momentaufnahme der Eigenschaften des Geräts gedacht werden, wenn sich das Gerät in einem bestimmten Zustand befindet. Daher muss die zu verwendende Konfiguration bereitgestellt werden, bevor ein PrintCapabilities-Dokument erstellt werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



