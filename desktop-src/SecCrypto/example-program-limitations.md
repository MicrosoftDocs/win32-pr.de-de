---
description: Einschränkungen des Beispielprogramms
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Einschränkungen des Beispielprogramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0244f373264ed6886632979f00ace873949c1ab7e781262b4ef30dab2072f8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007438"
---
# <a name="example-program-limitations"></a>Einschränkungen des Beispielprogramms

Die Prinzipien der bewährten Programmierpraktiken werden in diesen Beispielprogrammen nicht immer befolgt, um präziseren, lesbareren Code bereitzustellen. Dies gilt insbesondere für:

-   Es werden nur eingeschränkte Fehlerantworten angezeigt. Working programs should always check returned error codes and perform appropriate actions when an error is encountered. (Arbeitsprogramme sollten immer zurückgegebene Fehlercodes überprüfen und entsprechende Aktionen ausführen, wenn ein Fehler auftritt.)
-   Es erfolgt nur eine eingeschränkte Arbeitsspeicher- und Ressourcenverwaltung. In funktionierenden Programmen sollten alle Schlüssel und [*Hashes*](../secgloss/h-gly.md) zerstört, der gesamte zugeordnete Arbeitsspeicher freigegeben, alle Dateien geschlossen und alle Handles freigegeben werden. Diese Beispielprogramme bieten nur eingeschränkte Demonstrationen der Verwendung von Funktionen, die diese Aufgaben ausführen. Diese Beispielprogramme führen bei Programmbeendigung aufgrund von Fehlern keine Arbeitsspeicher- oder Ressourcenverwaltungsaufgaben aus.

 

 
