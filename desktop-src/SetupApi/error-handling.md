---
description: 'Es gibt drei Funktionen, die Dialogfelder generieren, um Fehler zu behandeln: SetupCopyError, SetupDeleteError und SetupRenameError.'
ms.assetid: fcb310e1-5db7-47f3-b3d6-d528eb17e19a
title: Fehlerbehandlung (Setup-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f3c69a4ab4943589d00354c401b1f35aa984b04552ecd03a1c4863fcf9134a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665990"
---
# <a name="error-handling-setup-api"></a>Fehlerbehandlung (Setup-API)

Es gibt drei Funktionen, die Dialogfelder generieren, um Fehler zu behandeln: [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)und [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).

Rückrufroutinen können diese Funktionen verwenden, um eine Benutzeroberfläche zur Handhabung von [**SPFILENOTIFY \_ COPYERROR-,**](spfilenotify-copyerror.md) [**SPFILENOTIFY \_ DELETEERROR-**](spfilenotify-deleteerror.md)und [**SPFILENOTIFY RENAMEERROR-Benachrichtigungen \_ zu**](spfilenotify-renameerror.md) generieren.

Jede dieser Fehlerbehandlungsfunktionen generiert ein Dialogfeld, in dem der Benutzer nach Informationen zum Fortfahren gefragt wird. Wie bei [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)können Sie das Layout und Verhalten des Dialogfelds ändern, indem Sie während des Funktionsaufrufs Flags angeben.

 

 



