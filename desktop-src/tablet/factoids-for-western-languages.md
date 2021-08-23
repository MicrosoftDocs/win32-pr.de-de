---
description: Westsprachen werden als Englisch (Vereinigtes Königreich), Englisch (USA), Französisch, Deutsch und Spanisch definiert.
ms.assetid: d4728506-7484-4c4c-a5ae-e98d699f7e76
title: Factoids für Westsprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e417c9662252213d761760a1486f9808a2d18bc3236073fe8c8d7746c396beb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936540"
---
# <a name="factoids-for-western-languages"></a>Factoids für Westsprachen

Westsprachen werden als Englisch (Vereinigtes Königreich), Englisch (USA), Französisch, Deutsch und Spanisch definiert. Die in der folgenden Tabelle gezeigten Formate in jedem Factoid sind spezifisch für die Erkennung der einzelnen Sprachen. Beispielsweise unterscheidet  sich das Telefon-Factoid in jeder Sprache. Darüber hinaus ist jedes Factoid spezifisch für eine bestimmte Erkennung. Beispielsweise kann das  Französische Telefon-Factoid nur mit der französischen Erkennung verwendet werden.

> [!Note]  
> Zusätzlich zu den folgenden Factoiden verwenden alle Sprachen die unter [Factoids Common Across Languages aufgeführten Factoids.](factoids-common-across-languages.md)

 



| Factoid              | Definition                                                                                                                                                                                                                                                                                                                                                                                                           | Beispiele                                                                                                                                                                                                                                                            |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Filename**         | Legt die Voreingenommenheit für einen Dateinamenspfad fest. Der Name darf keine Zeichen enthalten.<br/> / " < > \|<br/> Die Zeichen \* und ? sind in diesem Factoid enthalten, um die Suche zu ermöglichen. Außerdem werden erweiterte Zeichen in europäischen Sprachen unterstützt.<br/>                                                                                                                                                    | c:<br/> \\\\Verzeichnisname \\ Dateiname<br/> \\\\directory1 \\ directory2 \\ filename<br/> \\\\Verzeichnisname \\ \* .\*<br/> Dateiname.?<br/> myfile.doc<br/>                                                                                |
| **SystemDictionary** | Aktiviert nur das Systemwörterbuch. Dies ist nützlich, wenn eine Anwendung abfragt, ob sich ein Wort im Systemwörterbuch befindet. Legen Sie das Factoid auf **SystemDictionary** fest, und rufen Sie die [**IsStringSupported-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) auf.<br/>                                                                                                                                                 | Das Standardsprachmodell enthält Grammatik für die Sprache sowie das Systemwörterbuch. Diese Factoid-Voreingenommenheit der Erkennung in Richtung nur der Wörter, die im Systemwörterbuch auftreten. Jede Sprache verfügt über ein eigenes Systemwörterbuch.<br/>                   |
| **Wordlist**         | Aktiviert nur die Wortliste. Wenn das Factoid auf **WordList** festgelegt ist, aber dem [**InkRecognizerContext**](inkrecognizercontext-class.md) ([RecognizerContext](/previous-versions/ms552546(v=vs.100)) in verwaltetem Code) keine Wortliste zugewiesen ist, wird das Benutzerwörterbuch verwendet. Weitere Informationen zu Wortlisten und Wörterbüchern finden Sie unter [Verwenden von Anwendungswörterbüchern.](using-application-dictionaries.md)<br/> | Diese Factoid-Verzerrung bewegt die Erkennung dazu, nur Wörter in der Wortliste zurückzugeben. Damit der Benutzer beispielsweise eine Farbe in ein Formular eingeben kann, können Sie dieses Factoid und eine Wortliste verwenden, die "Grün", "Rot", "Blau", "Weiß" und andere Farben enthält.<br/> |



 

Die folgenden Kombinationen von Factoiden werden nur für Westsprachen unterstützt. Andere Kombinationen von Factoiden werden in dieser Version der ApIs (Application Programming Interfaces, Anwendungsprogrammierschnittstellen) der Tablet PC-Plattform nicht unterstützt. Diese Factoidkombinationen  verwenden einen logischen OR-Operator, daher kann die Eingabe mit jedem der Factoide im Ausdruck übereinstimmen.



| Factoid-Kombination     | Definition                                                                   |
|-------------------------|------------------------------------------------------------------------------|
| **WebWordList**         | Das  Web-Factoid oder die Wortliste.<br/>                             |
| **EmailWordList**       | Das **E-Mail-Factoid** oder die Wortliste.<br/>                           |
| **DateinameWebWordList** | Das **Filename-Factoid,** das **Web-Factoid** oder die Wortliste.<br/> |



 

In den folgenden Themen werden die Formate gezeigt, die für die einzelnen englischsprachigen Sprachen unterstützt werden.

-   [English (Worldwide) Factoids](english--worldwide--factoids.md)
-   [Englisch (USA) Factoids](english--united-states--factoids.md)
-   [Französische Factoids](french-factoids.md)
-   [Deutsche Factoids](german-factoids.md)
-   [Spanisch factoids](spanish-factoids.md)

 

