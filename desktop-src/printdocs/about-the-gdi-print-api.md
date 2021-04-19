---
description: Eines der wichtigsten Features der Funktionen in der GDI-Druck-API ist die Unterstützung der Geräteunabhängigkeit.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: Informationen zur GDI-Druck-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6e8a34552a1198ebe618f463003fe28ded6aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364151"
---
# <a name="about-the-gdi-print-api"></a>Informationen zur GDI-Druck-API

Eines der wichtigsten Features der Funktionen in der GDI-Druck-API ist die Unterstützung der Geräteunabhängigkeit. Anstatt gerätespezifische Befehle auszugeben, um die Ausgabe auf einem bestimmten Drucker oder einem anderen zu zeichnen, ruft eine Anwendung Funktionen auf hoher Ebene von der Graphics Device Interface (GDI) auf. Um z. b. ein Bitmap-Bild auszugeben, kann eine Anwendung die [**BitBLT**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) -Funktion aufzurufen und die Koordinaten für die Bitmap sowie Handles zur Identifizierung der Quell-und Zielgeräte Kontexte (DCS) bereitstellen. Der **BitBLT** -Aufrufe wird dann von einem Druckertreiber in unformatierte Geräte Befehle konvertiert. Ein Gerätetreiber ist eine Dynamic Link Library (dll), die die Gerätetreiber Schnittstelle (DDI) unterstützt. Ein Gerätetreiber generiert Rohgeräte Befehle, wenn er Aufrufe an von der Grafik-Engine vorgenommene DDI-Funktionen verarbeitet. Die Befehle werden vom Drucker beim Drucken des Bilds verarbeitet. Syntax, Zahl und Typ dieser Befehle variieren von Gerät zu Gerät.

Diese Übersicht enthält Informationen zu den folgenden Themen.

<dl>

[Standarddruck Schnittstelle](default-printing-interface.md)  
[Drucker Geräte Kontexte](printer-output.md)  
[Drucker Escapezeichen](printer-escapes.md)  
[WYSIWYG-Anzeige und-Ausgabe](wysiwyg-display-and-output.md)  
[DEVMODE pro Benutzer](per-user-devmode.md)  
</dl>

 

 
