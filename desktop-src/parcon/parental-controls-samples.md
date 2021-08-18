---
description: Beispiele für Jugendschutz
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: Beispiele für Jugendschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23111e42b670c30630b7ebd250c94ba2f148fcf4a81874fcc3c360db9b4bbd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971609"
---
# <a name="parental-controls-samples"></a>Beispiele für Jugendschutz

Beispielcode für Jugendschutz ist unter dem Pfad Windows <installation directory> \\ Samples Security \\ <version number> \\ \\ \\ ParentalControls verfügbar. Die Beispiele lauten wie folgt:

## <a name="utilities"></a>Hilfsprogramme

Hilfsfunktionen für grundlegende COM-Verwaltung, SID-Zeichenfolgenvorgänge und WMI-Lese- und -Schreibfunktionen. Alle anderen Beispiele hängen von diesem Projekt ab, sofern nicht anders angegeben.

## <a name="complianceapi"></a>ComplianceAPI

Befehlszeilengesteuerte Konsolenanwendung, die zeigt, wie sie die Kompatibilitäts-API verwendet, um eine wichtige Teilmenge von Einstellungen für einen Benutzer abzurufen.

## <a name="complianceapp"></a>ComplianceApp

Einfache Konsolenanwendung, die die Verwendung der Kompatibilitäts-API demonstriert, um die Protokollierung erforderlicher und spezifischer Einschränkungen zu überprüfen. Wenn Zeiteinschränkungen aktiviert sind, wartet die Anwendung auch auf die bevorstehenden Abmeldeereignisse.

## <a name="uiextensibility"></a>UIExtensibility

Befehlszeilengesteuerte Konsolenanwendung, die die Verwendung der WMI-APIs und des WPC-Schemas zum Auflisten, Abfragen, Hinzufügen, Ändern und Löschen von Verknüpfungseinträgen zur Erweiterbarkeit der Benutzeroberfläche demonstriert.

Beispielbefehlszeile für Beispiel:

"D: \\ WPC \\ Samples Security \\ \\ ParentalControls \\ \\ UIExtensibility debug \\ UIExtensibility" add /g:{FD59BB7F-54AB-11DB-9666-00E08161165F} /c:0 /n:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-101 /s:D :/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-103 /i:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-104 /d:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-106 /e:c: \\ windows \\Notepad.exe

Dabei ist UiExtRC eine einfache Ressourcen-DLL mit Zeichenfolgenressourcen für die IDs 101 und 103 und 24 x 24 Pixel 32 Bit mit Alphabitmaps für Ressourcen 104 und 106.

## <a name="webextensibility"></a>WebExtensibility

Eine befehlszeilengesteuerte Konsolenanwendung, die zeigt, wie sie die WMI-APIs und das WPC-Schema zum Auflisten, Hinzufügen und Löschen von Einträgen für HTTP-Anwendungen oder URL-Ausnahmen sowie zum Festlegen und Zurücksetzen einer Webinhaltsfilter-Überschreibung mit den Eigenschaften FilterID und FilterName verwendet.

Der Zugriff auf die schreibgeschützte HTTP-Anwendung und die URL-Ausnahmelisten wird nicht angezeigt, aber der Code zum Lesen der Listen wäre mit dem für den Lese-/Schreibfall identisch, mit Ausnahme der Änderung des WMI-Parameters.

 

 



