---
description: Um die Treiber Implementierung so weit wie möglich zu vereinfachen, stellt die Windows-Abbild Erfassung (WIA) eine Minidriver-Dienst Bibliothek bereit, die viele der administrativen Aufgaben durchführt, die für die WIA-Architektur erforderlich sind
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: WIA-Mini Treiber-Dienst Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45856fb795810e4e447a226f1b92a28698f08cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357346"
---
# <a name="wia-minidriver-service-library"></a>WIA-Mini Treiber-Dienst Bibliothek

Um die Treiber Implementierung so weit wie möglich zu vereinfachen, stellt die Windows-Abbild Erfassung (WIA) eine Minidriver-Dienst Bibliothek bereit, die viele der administrativen Aufgaben durchführt, die für die WIA-Architektur erforderlich sind Die Dienst Bibliothek stellt Hilfsfunktionen bereit, um die Struktur von [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekten des Geräts zu verwalten.

Die grundlegenden Dienst Bibliotheksfunktionen führen Hilfsfunktionen aus, die von den meisten Gerätetreibern anderweitig implementiert werden müssen. Diese Funktionen lesen und Schreiben Eigenschaften. Außerdem erstellen Sie Treiber Element Objekte und kopieren Geräte Informations Eigenschaften.

 

 



