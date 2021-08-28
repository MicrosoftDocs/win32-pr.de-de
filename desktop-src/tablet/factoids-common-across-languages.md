---
description: Eine Reihe von Factoids beschreiben Eingaben, die allen Spracherkennungen gemeinsam sind und nicht über unterschiedliche Formate für verschiedene Sprachen verfügen müssen. In der folgenden Tabelle sind die in allen Sprachen üblichen Factoids aufgeführt.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Häufig in verschiedenen Sprachen vorkommende Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407a82c72367d0123414f72b083b1d3416cfc958
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473876"
---
# <a name="factoids-common-across-languages"></a>Häufig in verschiedenen Sprachen vorkommende Factoids

Eine Reihe von Factoids beschreiben Eingaben, die allen Spracherkennungen gemeinsam sind und nicht über unterschiedliche Formate für verschiedene Sprachen verfügen müssen. In der folgenden Tabelle sind die in allen Sprachen üblichen Factoids aufgeführt.




| Factoid | Definition | Beispiele | 
|---------|------------|----------|
| <strong>Ziffer</strong> | Legt die Voreingenommenheit für eine einzelne Ziffer fest. Die Erkennung ist dazu voreingenommen, nur einstellige Ziffern zurückzugeben, wenn dieses Factoid festgelegt ist.<br /> | 0-9<br /> | 
| <strong>E-Mail</strong> | Legt die Voreingenommenheit für eine E-Mail-Adresse fest.<br /> | someone@example.com<br /> | 
| <strong>Web</strong> | Legt Voreingenommenheit für verschiedene URL-Formate fest.<br /><blockquote>[!Note]<br />Die Standardeinstellungen für die <strong></strong> Erkennung umfassen das Web-Factoid. Aus diesem Grund bemerken Sie möglicherweise keinen <strong></strong> großen Unterschied zwischen dem Web-Factoid und der Standardeinstellung. Das <strong>Web-Factoid</strong> trägt jedoch dazu bei, Leerzeichen zwischen Wörtern in einer URL zu entfernen.</blockquote><br /> | http: \\ microsoft.net<br /> https://microsoft.us/<br /> https: \\ www.microsoft.au \<br />https://microsoft.com<br /> www.microsoft_world.com<br /> www.microsoft.us \<br /> http: \\www.microsoft.com\myfile.htm<br /> http: \\www.microsoft.com\myfile.html<br /> http: \\ www.microsoft.com\myfile.asp<br /> http: \\ www.microsoft.uk<br /> http: \\ www.microsoft.info<br /> www.microsoft.biz<br /> | 
| <strong>Standard</strong> | Gibt die Erkennung auf die Standardeinstellungen zurück.<br /> | Die Standardeinstellung für Factoids für Westsprachen umfasst das Systemwörterbuch, das Benutzerwörterbuch, verschiedene Interpunktionen und die <strong>Web-</strong> und Zahlen-Factoide. <strong></strong><br /> Die Standardeinstellung für Factoids für ostasiatische Sprachen enthält alle zeichen, die von der Erkennung unterstützt werden.<br /> | 
| <strong>None</strong> | Deaktiviert alle Factoids, Wörterbücher und das Sprachmodell.<br /> | Dieses Factoid sollte nur verwendet werden, wenn die Erkennung keine Grammatikregeln oder Wörterbücher verwenden soll, einschließlich des Systemwörterbuchs. Dieses Factoid eignet sich für die Eingabe zufälliger Zeichenfolgen wie z.B. Produktcodes. Verwenden Sie das Coerce-Flag nicht mit diesem Factoid.<br /> | 




 

 

 




