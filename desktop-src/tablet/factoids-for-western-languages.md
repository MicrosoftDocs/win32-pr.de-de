---
description: Westliche Sprachen sind als Englisch (Vereinigtes Königreich), Englisch (USA), Französisch, Deutsch und Spanisch definiert.
ms.assetid: d4728506-7484-4c4c-a5ae-e98d699f7e76
title: Faktoide für westliche Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de98cfce0203a2a3a94509d6586c1596390ca16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041773"
---
# <a name="factoids-for-western-languages"></a>Faktoide für westliche Sprachen

Westliche Sprachen sind als Englisch (Vereinigtes Königreich), Englisch (USA), Französisch, Deutsch und Spanisch definiert. Die Formate in den einzelnen Faktoids, die in der folgenden Tabelle aufgeführt sind, sind spezifisch für die Erkennung der einzelnen Sprachen. Beispielsweise ist das **Telefon** -Faktoid in jeder Sprache unterschiedlich. Außerdem ist jedes Faktoid für eine bestimmte Erkennung spezifisch. Beispielsweise kann das französische **Telefon** -Faktoid nur mit der französischen Erkennung verwendet werden.

> [!Note]  
> Zusätzlich zu den folgenden Faktoiden werden in allen Sprachen die in den [verschiedenen Sprachen allgemeinen Faktoids](factoids-common-across-languages.md)aufgeführten unterschiedlichen Sprachen verwendet.

 



| Faktoid              | Definition                                                                                                                                                                                                                                                                                                                                                                                                           | Beispiele                                                                                                                                                                                                                                                            |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Filename**         | Legt den Wert für einen Dateinamen Pfad fest. Der Name darf die Zeichen nicht enthalten.<br/> /" < > \|<br/> Die Zeichen \* und? sind in dieser Faktoid enthalten, um die Suche zu aktivieren. Außerdem werden erweiterte Zeichen in europäischen Sprachen unterstützt.<br/>                                                                                                                                                    | c:<br/> \\\\directeryname \\ Dateiname<br/> \\\\directory1 \\ directory2 \\ Dateiname<br/> \\\\Directoren Name \\ \* .\*<br/> Dateiname.?<br/> myfile.doc<br/>                                                                                |
| **System Dictionary** | Aktiviert nur das System Wörterbuch. Dies ist hilfreich, wenn eine Anwendung fragt, ob ein Wort im System Wörterbuch vorhanden ist. Legen Sie Factoid auf **SystemDictionary** fest, und nennen Sie die [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) -Methode.<br/>                                                                                                                                                 | Das Standard Sprachmodell umfasst Grammatik für die Sprache und das System Wörterbuch. Diese Faktoid Bias die Erkennung nur in Bezug auf die Wörter, die im System Wörterbuch vorkommen. Jede Sprache verfügt über ein eigenes System Wörterbuch.<br/>                   |
| **"WordList**         | Aktiviert nur die Wort Liste. Wenn die Faktoid auf **WordList** festgelegt ist, aber keine Word-Liste dem [**inkrecognizercontext**](inkrecognizercontext-class.md) ([erkenzercontext](/previous-versions/ms552546(v=vs.100)) in verwaltetem Code) zugewiesen ist, wird das Benutzerwörterbuch verwendet. Weitere Informationen zu Wortlisten und Wörterbüchern finden [Sie unter Verwenden von Anwendungs Wörterbüchern](using-application-dictionaries.md).<br/> | Diese Faktoid gibt die Erkennungsfunktion für das Zurückgeben von Wörtern in der Wort Liste an. Wenn Sie z. b. dem Benutzer ermöglichen möchten, eine Farbe in ein Formular einzugeben, können Sie diese Factoid und eine Wort Liste verwenden, die "grün", "rot", "blau", "weiß" und andere Farben enthält.<br/> |



 

Die folgenden Kombinationen von Faktoiden werden nur für westliche Sprachen unterstützt. Andere Kombinationen von Faktoiden werden in dieser Version der Tablet PC Platform Application Programming Interfaces (APIs) nicht unterstützt. Diese Faktoid-Kombinationen verwenden einen logischen **or** -Operator. Daher kann die Eingabe mit jeder der Faktoide im Ausdruck verglichen werden.



| Faktoid-Kombination     | Definition                                                                   |
|-------------------------|------------------------------------------------------------------------------|
| **Webwordlist**         | **Webfaktoid** oder Wort Liste.<br/>                             |
| **Emailwordlist**       | Die **e-Mail-** Faktoid oder die Wortliste.<br/>                           |
| **Dateinamewebwordlist** | Der **Dateiname** (Faktoid) oder das **webfaktoid** oder die Wort Liste.<br/> |



 

In den folgenden Themen werden die Formate gezeigt, die für jede westliche Sprache unterstützt werden.

-   [Englische (weltweit) Faktoide](english--worldwide--factoids.md)
-   [Englische (USA) Faktoide](english--united-states--factoids.md)
-   [Französische Faktoide](french-factoids.md)
-   [Deutsche Faktoide](german-factoids.md)
-   [Spanische Faktoide](spanish-factoids.md)

 

