---
description: Ein Literalzeichen ist eine Zeichenfolge, die einen Wert in einer Abfrage Anweisung darstellt. Sie verwenden Literale zum Vergleichen von Spaltenwerten oder zum Angeben von Suchbegriffen. Windows Search unterstützt die folgenden Arten von Literalen.
ms.assetid: cc526174-3c91-402d-b7d0-69fc9a61c3f9
title: Literale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e066f62a39bc46ec2ff7bf44c187d33f3832ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348351"
---
# <a name="literals"></a>Literale

Ein Literalzeichen ist eine Zeichenfolge, die einen Wert in einer Abfrage Anweisung darstellt. Sie verwenden Literale zum Vergleichen von Spaltenwerten oder zum Angeben von Suchbegriffen. Windows Search unterstützt die folgenden Arten von Literalen.


-   **Zeichen folgen Literale** können eine beliebige Länge aufweisen und können ANSI-oder Unicode-Zeichen enthalten. Zeichen folgen Literale müssen in einfache Anführungszeichen (') eingeschlossen werden. Wenn Sie ein einzelnes Anführungszeichen in ein Zeichenfolgenliteralzeichen einschließen möchten, verwenden Sie zwei einfache Anführungszeichen (' '). Stellen Sie eine leere Zeichenfolge als zwei aufeinanderfolgende einfache Anführungszeichen (' ') dar.
-   **Numerische Literale** können die Ziffern 0-9, einen Punkt und den Buchstaben e (oder e) enthalten. Numerische Literale stellen Zahlen dar, einschließlich positiver und negativer ganze Zahlen, Dezimalzahlen und Währungswerte. Numerische Literale können mithilfe wissenschaftlicher Schreibweise (z. b. 2.3 e-05) definiert werden. Schließen Sie kein numerisches Literalformat in einfache Anführungszeichen ein, oder es wird als Zeichenfolgenliteralzeichen interpretiert und mithilfe von Zeichen folgen Vergleichs Techniken verglichen. Währungswerte dürfen keine Währungssymbole enthalten.
-   **Hexadezimale Literale** können die Ziffern 0-9 und die Buchstaben a-f und a-f enthalten. Ein hexadezimales wahrsten stellt eine Ganzzahl ohne Vorzeichen dar, die in hexadezimal Notation angegeben ist Hexadezimale Literale müssen mit "0x" beginnen.
    > [!Note]  
    > Der SQL-92-Standard erfordert, dass hexadezimale Literale in einfache Anführungszeichen eingeschlossen werden. die Windows-Suche unterstützt diese Notation jedoch nicht.

     

-   **Boolesche Literale** stellen logische Werte dar und können entweder " **true** " oder " **false**" sein. Schließen Sie kein boolesches wahrsten in einfache Anführungszeichen ein, oder es wird als Zeichenfolgenliteralzeichen interpretiert.
-   **Datums Literale** stellen bestimmte Datumsangaben, Zeitstempel oder relative Zeiten dar und sind in einfache Anführungszeichen eingeschlossen. Sie müssen Datumsangaben in der Form Jahr/Monat/Tag Stunden: Minuten: Sekunden oder Jahr-Monat-Tag Stunden: Minuten: Sekunden festlegen, wobei Monat, Tag und Jahr Ziffern sind. Geben Sie das Jahr mit einem vierstelligen Wert an, z. b. 2004. Uhrzeitwerte müssen im Format Stunden: Minuten: Sekunden angegeben werden. Die relative Zeit Syntax basiert auf der [DateAdd-Funktion](-search-sql-dateadd.md).

 

 



