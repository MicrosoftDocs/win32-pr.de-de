---
description: Die Richtlinien in diesem Thema sollen Ihnen helfen, klare Fehlermeldungen zu schreiben, die leicht zu lokalisieren und für Kunden nützlich sind.
ms.assetid: 361833e4-b94f-4ef9-a8f5-adf543534a67
title: Richtlinien für Fehlermeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1787eabd43d660322577ac766880d76854c574e7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747736"
---
# <a name="error-message-guidelines"></a>Richtlinien für Fehlermeldungen

Eine Fehlermeldung ist Text, der angezeigt wird, um ein aufgetretene Problem zu beschreiben, das verhindert, dass der Benutzer oder das System eine Aufgabe abschließen kann. Das Problem kann zu Daten Beschädigungen oder-Verlusten führen. Andere Nachrichten Typen umfassen Bestätigungen, Warnungen und Benachrichtigungen. Die Richtlinien in diesem Thema sollen Ihnen helfen, klare Fehlermeldungen zu schreiben, die leicht zu lokalisieren und für Kunden nützlich sind.

Schlecht geschriebene Fehlermeldungen können eine Quelle der Frustration für Benutzer sein und die Kosten des technischen Supports erhöhen. Eine gut geschriebene Fehlermeldung enthält die folgenden Informationen für den Benutzer:

-   Was ist passiert und warum?
-   Was ist das Endergebnis für den Benutzer?
-   Was kann der Benutzer tun, um die erneute Ausführung zu verhindern?

Die Länge des Texts stellt kein Problem dar, solange der Entwickler die Puffergrößen ordnungsgemäß verarbeitet. Es ist wichtig, dass der Benutzer über alle erforderlichen Informationen verfügt, um das Problem zu beheben. Wenn eine Nachricht über mehrere Zielgruppen verfügt, müssen Sie möglicherweise separaten Text für Administratoren, Endbenutzer und Entwickler bereitstellen.

## <a name="best-practices"></a>Bewährte Methoden

Im folgenden finden Sie Möglichkeiten, die Fehlermeldungen zu verbessern:

-   Vermeiden Sie Fehlerbedingungen. Wenn Sie Vorhersagen können, dass ein Fehler auftritt, wenn ein Benutzer eine bestimmte Aktion ausführt, schreiben Sie den Code so um, dass der Benutzer den Fehler nicht verursachen kann.
-   Schreiben Sie für jede bekannte Fehlerursache eine separate Fehlermeldung. Verwenden Sie keine einzige, generische Meldung, um jeden möglichen Grund für den Fehler zu erläutern, es sei denn, Sie können die Ursache des Fehlers nicht ermitteln, wenn dieser auftritt.
-   Geben Sie das Problem eindeutig ein. wenn es für den Benutzer hilfreich sein wird, erklären Sie, was das Problem verursacht hat. Ersetzen Sie nach Möglichkeit die generischen Nachrichten aus den System Message-Table-Ressourcen durch eine ausführliche Meldung, die für das Problem spezifisch ist.
-   Stellen Sie dem Benutzer eine Lösung für das Problem bereit. Wenn die Lösung mehr als einen Schritt umfasst, finden Sie in einem Hilfethema ausführliche Informationen zur Aufgabe.
-   Zeigt nur den Namen des Produkts, der Komponente oder des Assistenten in der Titelleiste der Nachricht an. Dadurch kann der Benutzer bestimmen, wo das Problem liegt. Fassen Sie das Problem nicht in der Titelleiste zusammen, oder fügen Sie das Wort "Error" ein.
-   Verwenden Sie den technischen Fachjargon nicht, verwenden Sie die Terminologie, die Ihre Zielgruppe versteht. Verwenden Sie weder den Slang noch die Abkürzungen.
-   Verwenden Sie die entsprechenden Befehls Schaltflächen, wie z. b. OK, Abbrechen, ja, Nein, und versuchen Sie es erneut. Sie können Kombinationen dieser Schaltflächen verwenden. Die Schaltflächen Ja und Nein müssen immer in Kombination verwendet werden, und es muss immer eine Frage vorangestellt sein.
    -   Verwenden Sie die Schaltfläche **Abbrechen** , um einen Vorgang zu beenden und das Meldungs Feld zu schließen.
    -   Um ein Meldungs Feld zu schließen, verwenden Sie die Schaltfläche **Schließen** .
    -   Verwenden Sie die Schaltfläche **Details** , um weitere Informationen zur Fehlerursache bereitzustellen.
    -   Wenn Sie weitere Informationen zur Lösung für das Problem bereitstellen möchten, verwenden Sie die Schaltfläche **Hilfe** .
    -   Wenn eine Benutzeraktion in der Meldung enthalten ist, verwenden Sie die Schaltfläche **OK** , um das Meldungs Feld zu schließen.
    -   Die Schaltflächen **Ja** und **Nein** müssen in Kombination verwendet werden, und es muss immer eine Frage vorangestellt sein.
-   Wenn es sich bei dem Fehler um einen schwerwiegenden Fehler handelt, schreiben Sie ihn in das [Ereignisprotokoll](../eventlog/event-logging.md).

## <a name="style-considerations"></a>Überlegungen zum Stil

-   Verwenden Sie vollständige, aber einfache Sätze.
-   Verwenden Sie die aktuelle Spannung, um die Bedingungen zu beschreiben, die das Problem verursacht haben, oder einen Zustand, der noch vorhanden ist. In der Vergangenheit können Sie ein eindeutiges Ereignis beschreiben, das in der Vergangenheit aufgetreten ist.
-   Verwenden Sie nach Möglichkeit immer die aktive Sprachnachricht. Sie können die passive Stimme verwenden, um den Fehlerzustand zu beschreiben.
-   Vermeiden Sie Großbuchstaben und Ausrufezeichen.
-   Sorgen Sie dafür, dass der Benutzer selbst dann keinen Fehler hat, wenn das Problem das Ergebnis eines Benutzer Fehlers ist.
-   Nicht anthropomorphize. Dies bedeutet nicht, dass Programme oder Hardware sich vorstellen oder fühlen können.
-   Verwenden Sie keine Umgangs Wörter oder-Ausdrücke. Verwenden Sie keine Begriffe, die in bestimmten Kulturen möglicherweise anstößige sind.
-   Kombinieren Sie nicht mehrere Nomen, ohne eine Präposition oder Unterklausel hinzuzufügen, um die Bedeutung zu verdeutlichen. Beispielsweise sollte "Standort Server-LDAP-Dienst Verzeichnisserver" in "Verzeichnisserver für den LDAP-Dienst des Standort Servers" geändert werden.
-   Fügen Sie Deskriptoren vor einem Begriff ein, um die Bedeutung des Satzes zu verdeutlichen. Beispiel: "INFID angeben, wenn" erkennen "auf" Nein "festgelegt ist. sollte geändert werden, wenn die Option "erkennen" auf "Nein" festgelegt ist.
-   Vermeiden Sie das Wort "schlecht". Verwenden Sie ausführlichere Begriffe, um dem Benutzer mitzuteilen, was falsch ist. Vermeiden Sie z. b. Meldungen wie "Ungültige Größe". Legen Sie den Benutzer stattdessen fest, welche Kriterien beim Angeben einer Größe verwendet werden sollen.
-   Vermeiden Sie das Wort "bitte". Sie kann so interpretiert werden, dass eine erforderliche Aktion optional ist.
-   Platzieren Sie Wörter, die sich im Index befinden und für die zentrale Bedeutung am Anfang der Meldungs Zeichenfolge relevant sind.

 

 
