---
description: 'Es gibt drei Funktionen, die Dialogfelder generieren, um Fehler zu behandeln: "setupcopyerror", "setupdeleteerror" und "setuprenameerror".'
ms.assetid: fcb310e1-5db7-47f3-b3d6-d528eb17e19a
title: Fehlerbehandlung (Setup-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb1347a3bec800200c2b6bda81e3f1eeeb866de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348219"
---
# <a name="error-handling-setup-api"></a>Fehlerbehandlung (Setup-API)

Es gibt drei Funktionen, die Dialogfelder generieren, um Fehler zu behandeln: " [**setupcopyerror**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora)", " [**setupdeleteerror**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)" und " [**setuprenameerror**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)".

Rückruf Routinen können diese Funktionen verwenden, um eine Benutzeroberfläche zu generieren, um [**spfilenotify \_ copyError**](spfilenotify-copyerror.md), [**spfilenotify \_ deleteerror**](spfilenotify-deleteerror.md)und [**spfilenotify \_ renameerror**](spfilenotify-renameerror.md) -Benachrichtigungen zu verarbeiten.

Jede dieser Fehler Behandlungs Funktionen generiert ein Dialogfeld, in dem der Benutzer aufgefordert wird, Informationen zum Fortfahren zu finden. Wie bei [**setuppromptfordisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)können Sie das Layout und Verhalten des Dialog Felds ändern, indem Sie während des Funktions Aufrufes Flags angeben.

 

 



