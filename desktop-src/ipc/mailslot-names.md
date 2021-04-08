---
description: Benennen von postslots und Einfügen von Nachrichten in postslots.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Mailslotnamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03718a7e603fe891e00d82c2b0b06fab63f8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749688"
---
# <a name="mailslot-names"></a>Mailslotnamen

Wenn ein Prozess einen Mailslot erstellt, muss der Name des postslots folgende Form aufweisen.

\\\\.\\ \\ \[ *postslotpfadname* \\ \] 

Der Name des postslots erfordert die folgenden Elemente: zwei umgekehrte Schrägstriche, um den Namen zu beginnen, einen Zeitraum, einen umgekehrten Schrägstrich, der auf den Zeitraum folgt, das Wort "Mailslot" und einen nachfolgenden umgekehrten Schrägstrich. Bei Namen wird Groß-/Kleinschreibung nicht beachtet Einem postslotnamen kann ein Pfad vorangestellt werden, der aus den Namen eines oder mehrerer Verzeichnisse besteht, die durch umgekehrte Schrägstriche getrennt sind. Wenn ein Benutzer beispielsweise Nachrichten für das Subjekt der Steuern von Bob, Pete und Sue erwartet, kann der Benutzer mit der mailslotanwendung für jeden Absender einzelne Postfächer erstellen, wie hier gezeigt:<dl> \\\\.\\ postslot \\ steuert \\ BOSB- \_ Kommentare  
\\\\.\\ postslotsteuern zeigt Kommentare an. \\ \\ \_  
\\\\.\\ postslottaxen unterliegen \\ \\ \_ Kommentaren  
</dl>

Wenn eine Nachricht in einem postslot abgelegt werden soll, öffnet ein Prozess einen postslot anhand des Namens. Um in einen Mailslot auf dem lokalen Computer zu schreiben, kann ein Prozess einen Mailslot-Namen verwenden, der die gleiche Form hat, die zum Erstellen eines postslots verwendet wurde. Diese Situation ist jedoch relativ ungewöhnlich. Häufig verwenden Sie das folgende Formular, um in einen Mailslot auf einem bestimmten Remote Computer zu schreiben:

\\\\*Computername* \\ \\ \[ *postslotpfadname* \\ \] 

Verwenden Sie das folgende Formular, um eine Nachricht in jedem Mailslot in der angegebenen Domäne mit einem bestimmten Namen zu platzieren:

\\\\*Domain Name* \\ \\ \[ *postslotpfadname* \\ \] 

Verwenden Sie das folgende Format, um eine Nachricht in jedem postslot mit einem bestimmten Namen in der primären Domäne des Systems zu platzieren:

\\\\\*\\\\ \[ *postslotpfadname* \\ \] 

 

 



