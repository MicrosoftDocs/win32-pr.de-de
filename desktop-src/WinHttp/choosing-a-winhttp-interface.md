---
description: Bevor Sie mit der Entwicklung einer WinHTTP-Anwendung (Microsoft Windows HTTP Services) beginnen, müssen Sie zunächst entscheiden, ob Sie die C/C++-API oder die COM-Schnittstelle verwenden möchten.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Auswählen einer WinHTTP-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7772959bd76dc7a257abc180c915f99df988a7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472356"
---
# <a name="choosing-a-winhttp-interface"></a>Auswählen einer WinHTTP-Schnittstelle

Bevor Sie mit der Entwicklung einer WinHTTP-Anwendung (Microsoft Windows HTTP Services) beginnen, müssen Sie zunächst entscheiden, ob Sie die C/C++-API oder die COM-Schnittstelle verwenden möchten. In der folgenden Tabelle werden die Vor- und Nachteile der einzelnen Ansätze zusammengefasst.




|  | C/C++-API | COM-Schnittstelle | 
|--|-----------|---------------|
| Vorteile | <ul><li>Antworten können in Blöcken verarbeitet werden, was effizienter ist.</li><li>POST-Vorgänge können auch in Blöcken verarbeitet werden, wodurch die Verarbeitungszeit beschleunigt wird.</li><li>AutoProxy-Unterstützung.</li><li>Zugriff auf den vollständigen Featuresatz von WinHTTP.</li><li>Binärdaten können problemlos verarbeitet werden.</li></ul> | <ul><li>Das Erstellen einer Anwendung ist einfach und erfordert weniger Codezeilen als die C/C++-API.</li><li>Die -Schnittstelle kann von Skriptsprachen verwendet werden.</li></ul> | 
| Nachteile | <ul><li>Die Verarbeitung ist komplexer.</li><li>Die C/C++-API erfordert mehr Schritte als die COM-Schnittstelle, um die gleichen Aktionen auszuführen.</li><li>Das Einrichten einer Anforderung erfordert mehr Code.</li></ul> | <ul><li>Die COM-Schnittstelle bietet keinen Zugriff auf den vollständigen Featuresatz von WinHTTP.</li><li>Es ist schwierig, binäre Datentypen in einigen Skriptsprachen wie VBScript und JScript zu verarbeiten.</li><li>Die COM-Schnittstelle unterstützt AutoProxy nicht.</li><li>Anwendungen müssen das COM-APARTMENT_THREADED Modell verwenden.</li><li>Bevor eine Antwort verarbeitet werden kann, muss zuerst die gesamte Antwort empfangen und gepuffert werden.</li></ul> | 




 

 

 



