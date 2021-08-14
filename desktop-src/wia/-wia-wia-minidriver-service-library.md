---
description: Um die Treiberimplementierung so weit wie möglich zu vereinfachen, stellt Windows Image Acquisition (WIA) eine Minidriver-Dienstbibliothek zur Verfügung, die viele der administrativen Aufgaben ausführt, die für die WIA-Architektur erforderlich sind.
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: WIA Minidriver-Dienstbibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0008e19fbbdb31000535fa10f34bfacebfd6c6180964fa3e3fb18502f22a28d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207930"
---
# <a name="wia-minidriver-service-library"></a>WIA Minidriver-Dienstbibliothek

Um die Treiberimplementierung so weit wie möglich zu vereinfachen, stellt Windows Image Acquisition (WIA) eine Minidriver-Dienstbibliothek zur Verfügung, die viele der administrativen Aufgaben ausführt, die für die WIA-Architektur erforderlich sind. Die Dienstbibliothek stellt Hilfsfunktionen bereit, um die Struktur der [IWiaDrvItem-Schnittstellenobjekte des Geräts zu](https://msdn.microsoft.com/library/ms793976.aspx) verwalten.

Die grundlegenden Dienstbibliotheksfunktionen führen Hilfsfunktionen aus, die die meisten Gerätetreiber andernfalls implementieren müssten. Diese Funktionen lesen und schreiben Eigenschaften. Außerdem werden Treiberelementobjekte erstellt und Geräteinformationseigenschaften kopiert.

 

 



