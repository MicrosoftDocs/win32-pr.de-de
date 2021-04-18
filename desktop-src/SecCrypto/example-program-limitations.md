---
description: Einschränkungen für das Beispielprogramm
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Einschränkungen für das Beispielprogramm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1fde65fa1870ac3ed118bd7c9f95c6add5192f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347715"
---
# <a name="example-program-limitations"></a>Einschränkungen für das Beispielprogramm

Grundsätze von guten Programmierpraktiken sind nicht immer in diesen Beispielprogrammen befolgt, um präziseren, besser lesbaren Code bereitzustellen. Dies gilt insbesondere für:

-   Nur eingeschränkte Fehler Antworten werden angezeigt. Bei funktionierenden Programmen sollten immer zurückgegebene Fehlercodes überprüft und geeignete Aktionen durchgeführt werden, wenn ein Fehler auftritt.
-   Nur eingeschränkte Arbeitsspeicher-und Ressourcenverwaltung erfolgt. In Arbeitsprogrammen sollten alle Schlüssel und [*Hashes*](../secgloss/h-gly.md) zerstört werden, der gesamte zugeordnete Arbeitsspeicher muss freigegeben werden, alle Dateien sollten geschlossen werden, und alle Handles sollten freigegeben werden. Diese Beispiel Programme bieten nur eine begrenzte Demonstration der Verwendung von Funktionen, die diese Aufgaben ausführen. Diese Beispiel Programme führen keine Arbeitsspeicher-oder Ressourcen Verwaltungsaufgaben aus, wenn die Programm Beendigung aufgrund von Fehlern auftritt.

 

 
