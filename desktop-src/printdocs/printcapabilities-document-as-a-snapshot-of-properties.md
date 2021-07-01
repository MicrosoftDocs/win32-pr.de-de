---
title: Dokument als Momentaufnahme von Eigenschaften
description: Überprüfen Sie das PrintCapabilities-Dokument als Momentaufnahme der Eigenschaften. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399c82211c268a72ad2b67082c144c64e46a879
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118645"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a>PrintCapabilities-Dokument als Momentaufnahme von Eigenschaften

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Das von PrintCapabilities beschriebene Gerät verfügt möglicherweise über Eigenschaften, die vom Zustand oder der Konfiguration des Geräts abhängen. Während PrintCapabilities den vollständigen Konfigurationsraum eines Geräts darstellt, erzeugt der PrintCapabilities-Anbieter eine konfigurationsabhängige Instanz des PrintCapabilities-Dokuments, das als PrintCapabilities-Dokument bezeichnet wird. Dieses konfigurationsabhängige PrintCapabilities-Dokument vermeidet die Belastung des PrintCapabilities-Schemas durch die Komplexität der Darstellung mehrwertigen Daten. Noch wichtiger ist, dass alle Property- und ScoredProperty-Instanzen in einem PrintCapabilities-Dokument einwertig sein müssen, um einen Consumer des PrintCapabilities-Dokuments von der Belastung zu hindern, den entsprechenden Wert aus einer mehrwertigen Datendarstellung zu extrahieren. Anders ausgedrückt: Jede Property- und ScoredProperty-Instanz in einem PrintCapabilities-Dokument muss relativ zur Eingabekonfiguration einen festen Wert aufweisen. Jedes PrintCapabilities-Dokument kann als Momentaufnahme der Eigenschaften des Geräts betrachtet werden, wenn sich das Gerät in einem bestimmten Zustand befindet. Daher muss die zu verwendende Konfiguration bereitgestellt werden, bevor ein PrintCapabilities-Dokument erstellt werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



