---
description: Benennen von Mailslots und Setzen von Nachrichten in mailslots.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Maillot-Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f96cc5300b3472abe7d6e824266bd0abd0e7b668e38f9f3462eee3cbf3dfb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716900"
---
# <a name="mailslot-names"></a>Maillot-Namen

Wenn ein Prozess einen Mailslot erstellt, muss der Maillotname das folgende Format aufweisen.

\\\\.\\ maillot \\ \[ *path* \\ \] *name*

Ein maillot-Name erfordert die folgenden Elemente: zwei umgekehrte Schrägstriche, um den Namen zu beginnen, einen Punkt, einen umgekehrten Schrägstrich nach dem Punkt, das Wort "mailslot" und einen nachgestellten umgekehrten Schrägstrich. Bei Namen wird die Groß-/Kleinschreibung nicht beachtet. Einem maillot-Namen kann ein Pfad vorangestellt werden, der aus den Namen eines oder mehrerer Verzeichnisse besteht, getrennt durch umgekehrte Schrägstriche. Wenn ein Benutzer beispielsweise Nachrichten zum Thema Steuern von Bob, Pete und Sue erwartet, kann die maillot-Anwendung des Benutzers es dem Benutzer ermöglichen, einzelne Mailslots für jeden Absender zu erstellen, wie hier gezeigt:<dl> \\\\.\\ mailslot \\ tax \\ bobs \_ comments  
\\\\.\\ mailslot \\ tax \\ petes \_ comments  
\\\\.\\ mailslot \\ tax \\ sues \_ comments  
</dl>

Um eine Nachricht in ein Maillot zu stellen, öffnet ein Prozess einen Mailslot anhand des Namens. Zum Schreiben in ein Maillot auf dem lokalen Computer kann ein Prozess einen maillot-Namen verwenden, der das gleiche Formular hat, das zum Erstellen eines Mailslots verwendet wird. Diese Situation ist jedoch relativ ungewöhnlich. Häufiger würden Sie das folgende Formular verwenden, um auf einem bestimmten Remotecomputer in ein Maillot zu schreiben:

\\\\*ComputerName* \\ maillot \\ \[ *path* \\ \] *name*

Verwenden Sie das folgende Formular, um eine Nachricht in jedem Maillot in der angegebenen Domäne mit einem bestimmten Namen zu senden:

\\\\*DomainName* \\ maillot \\ \[ *path* \\ \] *name*

Verwenden Sie das folgende Format, um eine Nachricht in jedem Maillot mit einem bestimmten Namen in der primären Domäne des Systems zu senden:

\\\\\*\\maillot \\ \[ *path* \\ \] *name*

 

 



