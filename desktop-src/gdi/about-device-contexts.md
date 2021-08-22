---
description: Die Geräteunabhängigkeit ist eines der wichtigsten Features von Microsoft Windows.
ms.assetid: f2a4c4cf-55e9-4129-8067-256552af49d2
title: Informationen zu Gerätekontexten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9439e3091b3138917e24ab4a49ff89c21a1e1b53480d4a138bd2bbad3288fcd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105875"
---
# <a name="about-device-contexts"></a>Informationen zu Gerätekontexten

Die Geräteunabhängigkeit ist eines der wichtigsten Features von Microsoft Windows. Anwendungen können Ausgaben auf einer Vielzahl von Geräten zeichnen und drucken. Die Software, die diese Geräteunabhängigkeit unterstützt, ist in zwei Dynamic Link-Bibliotheken enthalten. Die erste , Gdi.dll, wird als Grafikgeräteschnittstelle (GDI) bezeichnet. die zweite wird als Gerätetreiber bezeichnet. Der Name des zweiten hängt von dem Gerät ab, auf dem die Anwendung die Ausgabe zeichnet. Wenn die Anwendung beispielsweise die Ausgabe im Clientbereich ihres Fensters auf einer VGA-Anzeige zeichnet, wird diese Bibliothek Vga.dll; Wenn die Anwendung die Ausgabe auf einem Fx-80-Drucker druckt, wird diese Bibliothek Epson9.dll.

Eine Anwendung muss GDI anleiten, einen bestimmten Gerätetreiber zu laden und das Gerät nach dem Laden für Zeichnungsvorgänge vorzubereiten (z. B. auswählen einer Linienfarbe und -breite, eines Pinselmusters und einer Farbe, einer Schriftart, eines Ausschneidebereichs und so weiter). Diese Aufgaben werden durch Erstellen und Verwalten eines Gerätekontexts (DC) ausgeführt. Ein DC ist eine -Struktur, die eine Reihe von grafischen Objekten und deren zugeordnete Attribute sowie die Grafikmodi definiert, die sich auf die Ausgabe auswirken. Zu den Grafikobjekten gehören ein Stift für die Linienzeichnung, ein Pinsel zum Zeichnen und Füllen, eine Bitmap zum Kopieren oder Scrollen von Teilen des Bildschirms, eine Palette zum Definieren der Verfügbaren Farben, ein Bereich zum Ausschneiden und andere Vorgänge sowie ein Pfad für Zeichnungs- und Zeichnungsvorgänge. Im Gegensatz zu den meisten Strukturen hat eine Anwendung nie direkten Zugriff auf den Domänencontroller. stattdessen wird die Struktur indirekt durch Aufrufen verschiedener Funktionen verwendet.

Diese Übersicht enthält Informationen zu den folgenden Themen:

-   [Grafische Objekte](graphic-objects.md)
-   [Grafikmodi](graphic-modes.md)
-   [Gerätekontexttypen](device-context-types.md)
-   [Gerätekontextvorgänge](device-context-operations.md)
-   [ICM-aktivierte Gerätekontextfunktionen](icm-enabled-device-context-functions.md)

Ein wichtiges Konzept ist das Layout eines Domänencontrollers oder Fensters, das die Reihenfolge beschreibt, in der GDI-Objekte und Text (von links nach rechts oder von rechts nach links) angezeigt werden. Weitere Informationen finden Sie unter "Fensterlayout [](../winmsg/window-features.md) und -spiegelung" in Fensterfeatures und den [**Funktionen GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout) und [**SetLayout.**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout)

 

 
