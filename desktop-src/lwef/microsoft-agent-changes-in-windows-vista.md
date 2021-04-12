---
title: Microsoft-Agent-Änderungen in Windows Vista
description: Microsoft-Agent-Änderungen in Windows Vista
ms.assetid: 2498e8d5-2274-477c-a807-77443c76afb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73af45553f876c413fbea906de2369e888f1483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206889"
---
# <a name="microsoft-agent-changes-in-windows-vista"></a>Microsoft-Agent-Änderungen in Windows Vista

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Mit Windows Vista werden einige Änderungen in Bezug auf die Interaktion von Sprach-und Spracherkennung mit Windows Vista eingeführt.

Der Microsoft-Agent unterstützt jetzt SAPI 5-Text-zu-Sprache-und sprach Erkennungs Komponenten. Die Eigenschaften "ttsmodeid" und "srmodeid" des agentobjekts werden weiterhin verwendet, um zu bestimmen, welche Stimme oder Erkennungsfunktion für den Agent ausgewählt ist, und um diese Auswahl zu ändern. SAPI 4-Modi werden als GUID-Zeichen folgen wie "{ca141fd0-ac7f-11d1-97a3-006008273000}" angezeigt, während SAPI 5-Token (äquivalent zu Modi) als reguläre Namen (z. b. "Microsoft Anna") angezeigt werden. Wie in früheren Versionen stellt der Agent eine Standardauswahl von TTS-und SR-Engines dar. Wenn SAPI 5-Engines installiert sind, werden diese immer für alle installierten SAPI 4-Engines bevorzugt. Die standardmäßige Text-to-Speech-Engine des Benutzers, wie in der Systemsteuerung angegeben, wird verwendet, wenn das Geschlecht mit dem des Zeichens übereinstimmt. andernfalls wird eine SAPI 5-Engine desselben Geschlechts ausgewählt, sofern eine verfügbar ist. Die direkt auf dem Zeichen angegebenen Modus-IDs werden ignoriert, wenn SAPI 5-Engines vorhanden sind. Die Standardauswahl kann überprüft werden, indem Sie die Eigenschaften ttsmodeid und srmodeid am Anfang des Skripts lesen.

Wie zuvor geben ttsmodeid und srmodeid eine leere Zeichenfolge zurück, wenn die Funktion für Text-zu-Sprache oder Spracherkennung nicht vorhanden ist. Eine bestimmte Stimme oder Erkennungsfunktion kann ausgewählt werden, indem Sie diese Eigenschaften auf die entsprechende Zeichenfolge im SAPI 4-Modus oder den Namen des SAPI 5-Tokens festlegen. Nachdem Sie einen bestimmten Modus oder ein bestimmtes Token festgelegt haben, können Sie die Eigenschaft auch wieder zurück lesen, um sicherzustellen, dass ihr Wert angenommen wurde. Dies bedeutet, dass der neue Modus oder das Token tatsächlich verfügbar war und erfolgreich ausgewählt wurde. Für Entwickler, die den Agent über das Internet bereitstellen, beachten Sie, dass viele Vista-Benutzer bereits mindestens eine SAPI 5-Stimme installiert haben. Daher sollten Sie das automatische Herunterladen von SAPI 4-Stimmen vermeiden, es sei denn, das Skript fordert Sie explizit an, da die heruntergeladene Stimme nicht verwendet wird.

SAPI 5-Text-zu-Sprache-Engines verwenden einen anderen Satz von Standards als SAPI 4 zum Kommentieren von Sprache mit Markup, z. b. zum Ändern der Tonhöhe oder der Sprech Rate. In SAPI 4 verwenden Sie Schrägstriche (z. b./Pit = 170/). In SAPI 5 verwenden Sie XML-Tags, z <PITCH MIDDLE="5"/> . b.. In Vista akzeptiert der-Agent beide Arten von Anmerkungen in den Zeichen folgen der "Wort"-Methoden Zeichenfolgen, die von SAPI 5-Engines ignoriert werden, und XML-Tags werden von SAPI 4-Engines ignoriert. Wie bei Schrägstrichen unterscheiden sich die Unterstützung für SAPI 5-XML-Tags von Hersteller zu Hersteller, und einige Anbieter unterstützen möglicherweise zusätzliche Tags. Weitere Informationen zu SAPI 5-XML-Tags finden Sie in der Spezifikation von SAPI 5.

Der-Agent umfasst nicht mehr die Unterstützung für mehrere Sprachen. Die vom-Agent verwendete Sprache wird immer als aktuelle Sprache des Benutzers angenommen, die beim Betriebssystem registriert ist. Die LanguageID-Eigenschaft des agentobjekts ist immer noch beschreibbar, aber ihr Wert wird vom-Agent auf Vista ignoriert. Wenn die Sprache des Benutzers z. b. auf US-Englisch (&H0409) festgelegt ist, und er ein Programm verwendet, das LanguageID auf Französisch (&H040C) festlegt, werden die Dialogfelder sprach Tipp Text und erweiterte Zeichen Optionen weiterhin in englischer Sprache angezeigt.

 

 




