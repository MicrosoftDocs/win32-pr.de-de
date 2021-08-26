---
description: Windows GDI+ ist das Subsystem des Windows XP-Betriebssystems oder Windows Server 2003, das für die Anzeige von Informationen auf Bildschirmen und Druckern verantwortlich ist. GDI+ ist eine API, die über eine Reihe von C++-Klassen verfügbar gemacht wird.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Übersicht über GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ca4eadf9eaf27cbe35103753a49c4bc25d2974ee1051481b0b52787a6602e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830760"
---
# <a name="overview-of-gdi"></a>Übersicht über GDI+

Windows GDI+ ist das Subsystem des Windows XP-Betriebssystems oder Windows Server 2003, das für die Anzeige von Informationen auf Bildschirmen und Druckern verantwortlich ist. GDI+ ist eine API, die über eine Reihe von C++-Klassen verfügbar gemacht wird.

Wie der Name schon sagt, ist GDI+ der Nachfolger von Windows Graphics Device Interface (GDI), der Grafikgeräteschnittstelle, die in früheren Versionen von Windows enthalten ist. Windows XP oder Windows Server 2003 unterstützt GDI aus Gründen der Kompatibilität mit vorhandenen Anwendungen. Programmierer neuer Anwendungen sollten jedoch GDI+ für alle ihre Grafikanforderungen verwenden, da GDI+ viele der Funktionen von GDI optimiert und zusätzliche Features bereitstellt.

Eine Grafikgeräteschnittstelle, z. B. GDI+, ermöglicht Es Anwendungsprogrammierern, Informationen auf einem Bildschirm oder Drucker anzuzeigen, ohne sich Gedanken über die Details eines bestimmten Anzeigegeräts machen zu müssen. Der Anwendungsprogrammierer ruft Methoden auf, die von GDI+ Klassen bereitgestellt werden, und diese Methoden rufen wiederum bestimmte Gerätetreiber auf. GDI+ isoliert die Anwendung von der Grafikhardware, und dies ist dieser Schutz, mit dem Entwickler geräteunabhängige Anwendungen erstellen können.

 

 



