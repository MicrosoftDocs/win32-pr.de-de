---
description: Eines der wichtigsten Features der Funktionen in der GDI-Druck-API ist die Unterstützung der Geräteunabhängigkeit.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: Informationen zur GDI-Druck-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3aa7ea0ecfdd96237fb330868ddf2d9619aa24ee0d2f27a940c789a581a6c8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951010"
---
# <a name="about-the-gdi-print-api"></a>Informationen zur GDI-Druck-API

Eines der wichtigsten Features der Funktionen in der GDI-Druck-API ist die Unterstützung der Geräteunabhängigkeit. Anstatt gerätespezifische Befehle zum Zeichnen der Ausgabe auf einem bestimmten Drucker oder Plotter auszugeben, ruft eine Anwendung funktionen auf hoher Ebene über die Grafikgeräteschnittstelle (Graphics Device Interface, GDI) auf. Um z. B. ein Bitmapbild zu drucken, kann eine Anwendung die [**BitBlt-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) aufrufen und die Koordinaten für die Bitmap sowie Handles zur Identifizierung der Quell- und Zielgerätekontexte (DCs) angeben. Der Aufruf von **BitBlt** wird dann von einem Druckertreiber in unformatierte Gerätebefehle konvertiert. Ein Gerätetreiber ist eine Dll (Dynamic Link Library), die die Gerätetreiberschnittstelle (DDI) unterstützt. Ein Gerätetreiber generiert unformatierte Gerätebefehle, wenn er Aufrufe von DDI-Funktionen verarbeitet, die von der Grafik-Engine durchgeführt werden. Die Befehle werden vom Drucker verarbeitet, wenn das Bild gedruckt wird. Syntax, Anzahl und Typ dieser Befehle variieren von Gerät zu Gerät.

Diese Übersicht enthält Informationen zu den folgenden Themen.

<dl>

[Standarddruckschnittstelle](default-printing-interface.md)  
[Druckergerätekontexte](printer-output.md)  
[Drucker-Escapen](printer-escapes.md)  
[WYSIWYG– Anzeige und Ausgabe](wysiwyg-display-and-output.md)  
[DEVMODE pro Benutzer](per-user-devmode.md)  
</dl>

 

 
