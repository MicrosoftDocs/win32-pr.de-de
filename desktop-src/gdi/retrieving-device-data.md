---
description: 'Anwendungen können die folgenden Funktionen verwenden, um Gerätedaten mit einem Gerätekontext abzurufen: GetDeviceCaps und devicecapabili.'
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: Abrufen von Gerätedaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fa4054170f9b66d73e3494928db312eb8aa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978305"
---
# <a name="retrieving-device-data"></a>Abrufen von Gerätedaten

Anwendungen können die folgenden Funktionen verwenden, um Gerätedaten mit einem Gerätekontext abzurufen: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) und [**devicecapabili.**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)

[**Getabvicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) Ruft allgemeine Gerätedaten für die folgenden Geräte ab:

-   Raster anzeigen
-   Punkt-Matrix-Drucker
-   Ink-Jet-Drucker
-   Laser Drucker
-   Vektor Plottern
-   Raster Kameras

Die Daten umfassen die unterstützten Funktionen des Geräts, einschließlich der Geräte Auflösung (für Video-anzeigen), des Farb Formats (bei Video-und Farbdruckern), der Anzahl von Grafikobjekten, Raster Funktionen, Kurven Zeichnung, Zeilen Zeichnung, Polygon Zeichnung und Text Zeichnung. Eine Anwendung ruft diese Daten ab, indem Sie ein Handle bereitstellt, das den entsprechenden Gerätekontext identifiziert, sowie einen Index, der den Typ der Daten angibt, die von der Funktion abgerufen werden sollen.

Die Funktion [**devicecapabiliruft**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) spezifische Daten für Drucker ab, einschließlich der Anzahl der verfügbaren Papierbehälter, der Duplex Funktionen des Druckers, der vom Drucker unterstützten Auflösungen, der maximalen und der minimalen unterstützten Papiergröße usw. Eine Anwendung ruft diese Daten durch Bereitstellen von Zeichen folgen ab, die ein Druckergerät und einen Port angeben, sowie einen Index, der den Typ der Daten angibt, die von der Funktion abgerufen werden sollen.

 

 
