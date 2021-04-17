---
description: Netzwerkmonitor oder Ihre Parser-DLL kann die Daten formatieren, die im Detailbereich der Netzwerkmonitor-Benutzeroberfläche angezeigt werden.
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: Formatieren von angezeigten Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017946dab9db443cf7083109dd75ccee1f6d278a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525145"
---
# <a name="formatting-displayed-data"></a>Formatieren von angezeigten Daten

Netzwerkmonitor oder Ihre Parser-DLL kann die Daten formatieren, die im Detailbereich der Netzwerkmonitor-Benutzeroberfläche angezeigt werden.

Netzwerkmonitor stellt einen generischen Formatierer bereit, der die grundlegenden Dienste bereitstellt, die zum Anzeigen der meisten Datentypen in einem Protokoll erforderlich sind. Der generische Formatierer unterstützt jedoch nicht alle Datentypen. Beispielsweise unterstützt das generische Formatierer Folgendes nicht:

-   Mehrere Adresstypen.
-   Quell-und Zielanzeige Name.
-   Objekt Bezeichner.
-   Große ganzzahlige Datentypen.
-   Datentypen mit geringer Ganzzahl mit variabler Länge.

Im folgenden Beispiel werden zwei formatierte Zeichen folgen für die Eigenschaft Berechtigungs-ID identifiziert.

-   Die erste Codezeile zeigt die Ausgabe des generischen Formatierers. Die Ausgabe basiert auf dem Datentyp.
-   Die zweite Codezeile zeigt die Ausgabe eines benutzerdefinierten Formatierers mit einer Zeichenfolge für die Eigenschafts Daten.

``` syntax
Privilege ID (PID) = 0x0029
Privilege ID   (PID) = 0x0029   The Process has privileges
```

> [!Note]  
> Verwenden Sie nach Möglichkeit den generischen Formatierer, um Ihre Daten anzuzeigen, da Sie die Größe Ihrer Parser-DLL steuern können und bessere plattformübergreifende Funktionen für Ihre Parser-DLL bereitstellen.

 

 

 



