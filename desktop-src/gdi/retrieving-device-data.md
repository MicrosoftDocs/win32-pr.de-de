---
description: 'Anwendungen können die folgenden Funktionen verwenden, um Gerätedaten mithilfe eines Gerätekontexts abzurufen: GetDeviceCaps und DeviceCapabilities.'
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: Abrufen von Gerätedaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf956a04c733883cb5fb374e4e75dc4e93e8029f9968deb90cc113cef460864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717990"
---
# <a name="retrieving-device-data"></a>Abrufen von Gerätedaten

Anwendungen können die folgenden Funktionen verwenden, um Gerätedaten mithilfe eines Gerätekontexts abzurufen: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) und [**DeviceCapabilities.**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)

[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) ruft allgemeine Gerätedaten für die folgenden Geräte ab:

-   Rasteranzeigen
-   Dot-Matrixdrucker
-   Ink-Jet-Drucker
-   Drucker von Druckern
-   Vektorplotter
-   Rasterkameras

Die Daten umfassen die unterstützten Funktionen des Geräts, einschließlich Geräteauflösung (für Videoanzeigen), Farbformat (für Videoanzeigen und Farbdrucker), Anzahl von Grafikobjekten, Rasterfunktionen, Kurvenzeichnung, Linienzeichnung, Polygonzeichnung und Textzeichnung. Eine Anwendung ruft diese Daten ab, indem sie ein Handle angibt, das den entsprechenden Gerätekontext identifiziert, sowie einen Index, der den Typ der Daten angibt, die die Funktion abrufen soll.

Die [**DeviceCapabilities-Funktion**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) ruft druckerspezifische Daten ab, z. B. die Anzahl der verfügbaren Papierbehälter, die Duplexfunktionen des Druckers, die vom Drucker unterstützten Auflösungen, die maximale und minimale unterstützte Papiergröße usw. Eine Anwendung ruft diese Daten ab, indem Zeichenfolgen angegeben werden, die ein Druckergerät und einen Port angeben, sowie einen Index, der den Typ der Daten angibt, die die Funktion abrufen soll.

 

 
