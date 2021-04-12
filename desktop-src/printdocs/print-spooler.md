---
description: Die primäre Komponente der Druck Schnittstelle ist der Druck Spooler.
ms.assetid: 36ffb001-78e2-4fa0-8241-3891493ac02d
title: Druckspooler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfcc6ea2e46c06b5e51032a4c43f46df7f07c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529174"
---
# <a name="print-spooler"></a>Druckspooler

Die primäre Komponente der Druck Schnittstelle ist der Druck Spooler. Der Druck Spooler ist eine ausführbare Datei, mit der der Druckprozess verwaltet wird. Die Druck Verwaltung umfasst das Abrufen des Speicher Orts des richtigen Druckertreibers, das Laden des Treibers, das spoaden von Funktionsaufrufen auf hoher Ebene in einen Druckauftrag, das Planen des Druckauftrags für das Drucken usw. Der Spooler wird beim Systemstart geladen und wird weiterhin ausgeführt, bis das Betriebssystem heruntergefahren wird.

Anwendungen, die drucken, erstellen einen Drucker Gerätekontext (DC). Wenn eine Anwendung einen Drucker-DC erstellt, führt der Spooler die erforderlichen Aufgaben aus, z. b. das Ermitteln des Speicher Orts des erforderlichen Druckertreibers und das anschließende Laden dieses Treibers. Der Druck Spooler bestimmt auch den Datentyp, der zum Aufzeichnen des Druckauftrags verwendet wird.

Der Druck Spooler unterstützt die folgenden Datentypen:

-   Erweiterte Metadatei (EMF).
-   ASCII-Text.
-   Rohdaten, die Drucker Datentypen wie z. b. PostScript, PCL und benutzerdefinierte Datentypen enthalten.

Benutzerdefinierte Datentypen können dem Spooler hinzugefügt werden, indem zusätzliche Druckertreiber und Druck Prozessoren installiert werden. Ein Druckauftrag ist ein Dokument, das intern gespeichert und mit einem der unterstützten Datentypen codiert wird, und ein Druckauftrag kann eine oder mehrere Seiten der Ausgabe enthalten. Der Druckauftrag kann aus mehreren Formularen bestehen. ein Auftrag kann beispielsweise aus einem Umschlag und drei Seiten mit einem A4-Papier bestehen. Ein Druckauftrag wird durch die Funktionen " [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) " und " [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) " definiert (oder in Klammern gesetzt).

Der Standard Datentyp für einen Druckauftrag ist die erweiterte Metadatei. Ein EMF-Datensatz ist eine kompakte Struktur, die zum Speichern von Textausgabe Befehlen, Rastergrafik Befehlen usw. verwendet wird. Wenn eine Anwendung [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)aufruft, erstellt der Spooler eine Spooldatei und eine Datendatei und beginnt damit, EMF-Einträge in der Spooldatei zu speichern. Jedes Mal, wenn die Anwendung eine der GDI-Zeichnungsfunktionen aufruft, werden ein oder mehrere neue EMF-Einträge erstellt und in der Spooldatei gespeichert. Die Spooldateien und Datendateien werden in einem Betriebssystem Verzeichnis erstellt. Der Spooler verwendet die Spooldatei zum Speichern von EMF-Datensätzen und verwendet die Datendatei, um den Typ des Formulars, den Datentyp für den Druckauftrag, den Ziel Drucker usw. aufzuzeichnen. Der Spooler löscht diese Dateien, wenn der Auftrag erfolgreich gedruckt wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Metadateien mit erweitertem Format](/windows/desktop/gdi/enhanced-format-metafiles)
</dt> </dl>

 

 
