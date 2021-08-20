---
description: Die Hauptkomponente der Druckschnittstelle ist der Druckspooler.
ms.assetid: 36ffb001-78e2-4fa0-8241-3891493ac02d
title: Druckspooler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52bac19b44ebed5762abdb00b9ea044cf775a7a7ca8193c641709ad2c39436dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033928"
---
# <a name="print-spooler"></a>Druckspooler

Die Hauptkomponente der Druckschnittstelle ist der Druckspooler. Der Druckspooler ist eine ausführbare Datei, die den Druckvorgang verwaltet. Die Verwaltung des Drucks umfasst das Abrufen des Speicherorts des richtigen Druckertreibers, das Laden des Treibers, das Spoolen von allgemeinen Funktionsaufrufen in einen Druckauftrag, das Planen des Druckauftrags für den Druckvorgang und so weiter. Der Spooler wird beim Systemstart geladen und wird so lange ausgeführt, bis das Betriebssystem heruntergefahren wird.

Anwendungen, die drucken, erstellen einen Druckergerätekontext (DC). Wenn eine Anwendung einen Druckerdomänencontroller erstellt, führt der Spooler die erforderlichen Aufgaben aus, z. B. das Bestimmen des Speicherorts des erforderlichen Druckertreibers und das anschließende Laden dieses Treibers. Der Druckspooler bestimmt auch den Datentyp, der zum Aufzeichnen des Druckauftrags verwendet wird.

Der Druckspooler unterstützt die folgenden Datentypen:

-   Erweiterte Metadatei (EMF).
-   ASCII-Text.
-   Rohdaten, einschließlich Druckerdatentypen wie PostScript, PCL und benutzerdefinierte Datentypen.

Benutzerdefinierte Datentypen können dem Spooler hinzugefügt werden, indem zusätzliche Druckertreiber und Druckprozessoren installiert werden. Ein Druckauftrag ist ein intern gespeichertes und mit einem der unterstützten Datentypen codiertes Dokument, und ein Druckauftrag kann eine oder mehrere Seiten der Ausgabe enthalten. Der Druckauftrag kann aus mehreren Formularen bestehen. Beispielsweise kann ein Auftrag aus einem Umschlag und drei Seiten A4-Papier bestehen. Ein Druckauftrag wird durch die Funktionen [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) und EndDoc definiert (oder in [**Klammern**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) gesetzt).

Der Standarddatentyp für einen Druckauftrag ist die erweiterte Metadatei. Ein EMF-Datensatz ist eine kompakte Struktur zum Speichern von Textausgabebefehlen, Rastergrafikbefehlen und so weiter. Wenn eine Anwendung [**StartDoc aufruft,**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)erstellt der Spooler eine Spooldatei und eine Datendatei und beginnt mit dem Speichern von EMF-Datensätzen in der Spooldatei. Jedes Mal, wenn die Anwendung eine der GDI-Zeichnungsfunktionen aufruft, werden mindestens ein neuer EMF-Datensatz erstellt und in der Spooldatei gespeichert. Die Spool- und Datendateien werden in einem Betriebssystemverzeichnis erstellt. Der Spooler verwendet die Spooldatei zum Speichern von EMF-Datensätzen und die Datendatei, um den Formulartyp, den Datentyp für den Druckauftrag, den Zieldrucker und so weiter aufzuzeichnen. Der Spooler löscht diese Dateien, wenn der Auftrag erfolgreich gedruckt wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweitertes Format von Metadateien](/windows/desktop/gdi/enhanced-format-metafiles)
</dt> </dl>

 

 
