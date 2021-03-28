---
description: Windows GDI+ ist das Subsystem des Betriebssystems Windows XP oder Windows Server 2003, das für die Anzeige von Informationen auf Bildschirmen und Druckern zuständig ist. GDI+ ist eine API, die über einen Satz von C++-Klassen verfügbar gemacht wird.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Übersicht über GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6eb3885d33ad332ac61454525367788d7aed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994190"
---
# <a name="overview-of-gdi"></a>Übersicht über GDI+

Windows GDI+ ist das Subsystem des Betriebssystems Windows XP oder Windows Server 2003, das für die Anzeige von Informationen auf Bildschirmen und Druckern zuständig ist. GDI+ ist eine API, die über einen Satz von C++-Klassen verfügbar gemacht wird.

Wie der Name schon sagt, ist GDI+ der Nachfolger von Windows Graphics Device Interface (GDI), der Grafikgeräte Schnittstelle, die in früheren Versionen von Windows enthalten war. Windows XP oder Windows Server 2003 unterstützt GDI in Bezug auf die Kompatibilität mit vorhandenen Anwendungen, Programmierer neuer Anwendungen sollten GDI+ jedoch für alle Ihre Grafik Anforderungen verwenden, da GDI+ viele der Funktionen von GDI optimiert und außerdem zusätzliche Funktionen bereitstellt.

Eine Grafikgeräte Schnittstelle, wie z. b. GDI+, ermöglicht Anwendungs Programmierern, Informationen auf einem Bildschirm oder Drucker anzuzeigen, ohne sich um die Details eines bestimmten Anzeige Geräts kümmern zu müssen. Der Anwendungsprogrammierer führt Aufrufe an Methoden aus, die von GDI+-Klassen bereitgestellt werden, und diese Methoden führen wiederum die entsprechenden Aufrufe an bestimmte Gerätetreiber aus. GDI+ isoliert die Anwendung von der Grafikhardware. diese Isolierung ermöglicht es Entwicklern, geräteunabhängige Anwendungen zu erstellen.

 

 



