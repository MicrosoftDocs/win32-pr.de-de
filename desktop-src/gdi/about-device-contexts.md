---
description: Die Geräteunabhängigkeit ist eines der wichtigsten Features von Microsoft Windows.
ms.assetid: f2a4c4cf-55e9-4129-8067-256552af49d2
title: Informationen zu Geräte Kontexten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b686ec8b48492658f19531cb42161c043f178d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130360"
---
# <a name="about-device-contexts"></a>Informationen zu Geräte Kontexten

Die Geräteunabhängigkeit ist eines der wichtigsten Features von Microsoft Windows. Anwendungen können die Ausgabe auf einer Vielzahl von Geräten zeichnen und drucken. Die Software, die diese Geräteunabhängigkeit unterstützt, ist in zwei Dynamic-Link-Bibliotheken enthalten. Der erste, Gdi.dll, wird als Grafikgeräte Schnittstelle (Graphics Device Interface, GDI) bezeichnet. die zweite wird als Gerätetreiber bezeichnet. Der Name der zweiten hängt von dem Gerät ab, auf dem die Anwendung die Ausgabe zeichnet. Wenn die Anwendung z. b. die Ausgabe im Client Bereich des Fensters auf einer VGA-Anzeige zeichnet, wird diese Bibliothek Vga.dll. Wenn die Anwendung die Ausgabe auf einem Epson FX-80-Drucker ausgibt, wird diese Bibliothek Epson9.dll.

Eine Anwendung muss GDI darüber informieren, dass ein bestimmter Gerätetreiber geladen und der Treiber geladen wird, um das Gerät auf Zeichnungsvorgänge vorzubereiten (z. b. das Auswählen einer Linien Farbe und-Breite, eines Pinsel Musters und einer Farbe, einer Schriftart Schriftart, eines Clippingbereichs usw.). Diese Aufgaben werden durch das Erstellen und Verwalten eines Geräte Kontexts (DC) erreicht. Ein Domänen Controller ist eine Struktur, die eine Reihe von Grafikobjekten und deren zugeordneten Attributen definiert, sowie die Grafikmodi, die die Ausgabe beeinflussen. Die Grafik Objekte enthalten einen Stift für das Zeichnen von Zeilen, einen Pinsel zum Zeichnen und Auffüllen, eine Bitmap zum Kopieren oder Scrollen von Teilen des Bildschirms, eine Palette zum Definieren des Satzes verfügbarer Farben, eine Region für das Abschneiden und andere Vorgänge sowie einen Pfad für Zeichnungs-und Zeichnungsvorgänge. Im Gegensatz zu den meisten Strukturen hat eine Anwendung keinen direkten Zugriff auf den DC. Stattdessen wird die Struktur indirekt durch Aufrufen verschiedener Funktionen betrieben.

Diese Übersicht enthält Informationen zu den folgenden Themen:

-   [Grafik Objekte](graphic-objects.md)
-   [Grafikmodi](graphic-modes.md)
-   [Gerätekontext Typen](device-context-types.md)
-   [Gerätekontext Vorgänge](device-context-operations.md)
-   [ICM-aktivierte Gerätekontext Funktionen](icm-enabled-device-context-functions.md)

Ein wichtiges Konzept ist das Layout eines DC oder Fensters, in dem die Reihenfolge beschrieben wird, in der GDI-Objekte und Text angezeigt werden (von links nach rechts oder von rechts nach links). Weitere Informationen finden Sie unter "Fenster Layout und Spiegelung" [**in den Funktionen "Window"**](../winmsg/window-features.md) und " [**getLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout) " und " [**setLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout) ".

 

 
