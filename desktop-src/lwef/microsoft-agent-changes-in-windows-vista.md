---
title: Microsoft Agent-Änderungen in Windows Vista
description: Microsoft Agent-Änderungen in Windows Vista
ms.assetid: 2498e8d5-2274-477c-a807-77443c76afb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440fb8afb7acb0118c1e48669089c083e935db5b
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102149"
---
# <a name="microsoft-agent-changes-in-windows-vista"></a>Microsoft Agent-Änderungen in Windows Vista

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Windows Vista führt einige Änderungen in der Interaktion von Sprache und Spracherkennung mit Windows Vista ein.

Microsoft Agent unterstützt jetzt SAPI 5 Text-to-Speech- und Spracherkennungskomponenten. Die TTSModeID- und SRModeID-Eigenschaften des Agent-Objekts werden weiterhin verwendet, um zu bestimmen, welche Stimme oder Erkennen für den Agent ausgewählt ist, und um diese Auswahl zu ändern. SAPI 4-Modi werden als GUID-Zeichenfolgen wie "{ca141fd0-ac7f-11d1-97a3-006008273000}" angezeigt, während SAPI 5-Token (äquivalent zu Modi) als reguläre Namen wie "Microsoft Anna" angezeigt werden. Wie in früheren Versionen wird der Agent eine Standardauswahl für TTS- und SR-Engines treffen. Wenn SAPI 5-Engines installiert sind, werden diese immer allen SAPI 4-Engines vorgezogen, die installiert werden können. Die standardmäßige Text-to-Speech-Engine des Benutzers, wie in der Systemsteuerung angegeben, wird verwendet, wenn das Geschlecht mit dem des Zeichens identisch ist. Andernfalls wird eine SAPI 5-Engine des gleichen Geschlechtes ausgewählt, wenn eines verfügbar ist. Direkt im Zeichen angegebene Modus-IDs werden ignoriert, wenn SAPI 5-Engines vorhanden sind. Die Standardauswahl kann überprüft werden, indem Die TTSModeID- und SRModeID-Eigenschaften am Anfang des Skripts gelesen werden.

Wie zuvor geben TTSModeID und SRModeID eine leere Zeichenfolge zurück, wenn die Spracherkennungs- oder Spracherkennungsfunktion nicht vorhanden ist. Sie können eine bestimmte Stimme oder Eine bestimmte Spracherkennung wählen, indem Sie diese Eigenschaften auf die entsprechende SAPI 4-Moduszeichenfolge oder den SAPI 5-Tokennamen festlegen. Nach dem Festlegen eines bestimmten Modus oder Tokens können Sie die Eigenschaft auch erneut lesen, um zu überprüfen, ob ihr Wert übernommen wurde. Dies bedeutet, dass der neue Modus oder das token tatsächlich verfügbar war und erfolgreich ausgewählt wurde. Für Entwickler, die den -Agent über das Web bereitstellen, beachten Sie, dass viele Vista-Benutzer bereits eine oder mehrere SAPI 5-Stimmen installiert haben. Daher sollten Sie das automatische Herunterladen von SAPI 4-Stimmen vermeiden, es sei denn, Ihr Skript fordert sie ausdrücklich an, da die heruntergeladene Stimme am Ende nicht verwendet wird.

SAPI 5-Text-to-Speech-Engines verwenden einen anderen Standardsatz als SAPI 4 zum Kommentieren von Sprache mit Markup, z. B. zum Ändern der Tonhöhe oder Rate der Sprache. In SAPI 4 verwenden Sie "Schrägstrich"-Befehle, z. B. /pit=170/. In SAPI 5 verwenden Sie XML-Tags wie \<PITCH MIDDLE="5"/> . In Vista akzeptiert der -Agent beide Arten von Anmerkungen in Speak-Methodenzeichenfolgen-Befehlen mit "Schrägstrich", die von SAPI 5-Engines ignoriert werden, und XML-Tags werden von SAPI 4-Engines ignoriert. Wie bei Schrägstrichtags variiert die Unterstützung für SAPI 5 XML-Tags von Hersteller zu Hersteller, und einige Anbieter unterstützen möglicherweise zusätzliche Tags. Weitere Informationen zu SAPI 5 XML-Tags finden Sie in der SAPI 5-Spezifikation.

Der Agent bietet keine Unterstützung für mehrere Sprachen mehr. Es wird immer davon ausgegangen, dass es sich bei der vom -Agent verwendeten Sprache um die aktuelle Sprache des Benutzers handelt, die beim Betriebssystem registriert ist. Die LanguageID-Eigenschaft des -Agent-Objekts kann weiterhin beschreibbar sein, ihr Wert wird jedoch vom -Agent unter Vista ignoriert. Wenn die Sprache des Benutzers z. B. auf US-Englisch (&H0409) festgelegt ist und er ein Programm verwendet, das die LanguageID auf Französisch (&H040C) setzt, werden der Sprachtipptext und die Dialogfelder erweiterte Zeichenoptionen weiterhin auf Englisch angezeigt.

 

 




