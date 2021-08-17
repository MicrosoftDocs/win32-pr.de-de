---
description: Bevor die Standardmäßige Warteschlangenrückrufroutine verwendet werden kann, entweder durch Angabe als Rückrufroutine beim Committen einer Dateiwarteschlange oder durch Aufrufen über eine benutzerdefinierte Rückrufroutine, muss sie initialisiert werden.
ms.assetid: e25a9787-a4a3-4d06-bf55-f6f7cfb23481
title: Initialisieren und Beenden des Rückrufkontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67df0707f91a17369503fa17ecbeefef3eb6827be60285b0b778b07d98eba3a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965433"
---
# <a name="initializing-and-terminating-the-callback-context"></a>Initialisieren und Beenden des Rückrufkontexts

Bevor die Standardmäßige Warteschlangenrückrufroutine verwendet werden kann, entweder durch Angabe als Rückrufroutine beim Committen einer Dateiwarteschlange oder durch Aufrufen über eine benutzerdefinierte Rückrufroutine, muss sie initialisiert werden.

Die [**SetupInitDefaultQueueCallback-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) erstellt die Kontextstruktur, die von der standardmäßigen Warteschlangenrückrufroutine verwendet wird. Sie gibt einen void-Zeiger auf diese Struktur zurück. Diese Struktur ist wichtig für den Vorgang der Standardrückrufroutine und muss an die Rückrufroutine übergeben werden. Hierzu können Sie entweder den void-Zeiger als Kontext in einem Aufruf von [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)angeben oder indem Sie den void-Zeiger als Kontextparameter angeben, wenn [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) aus einer benutzerdefinierten Rückrufroutine aufruft. Diese Kontextstruktur darf von der Setupanwendung nicht geändert oder referenziert werden.

Die [**SetupInitDefaultQueueCallbackEx-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) initialisiert auch einen Kontext für die Standardmäßige Warteschlangenrückrufroutine, gibt jedoch ein zweites Fenster an, in dem jedes Mal, wenn die Warteschlange eine Benachrichtigung sendet, eine vom Aufrufer angegebene Statusmeldung empfangen wird. Auf diese Weise können Sie die Standarddialogfelder für Die Eingabeaufforderung und Fehler des Datenträgers verwenden und auch eine Statusleiste in ein zweites Fenster einbetten, z. B. auf einer Seite eines Installations-Assistenten.

Rufen Sie [**setupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) auf, um die beim Initialisieren der Kontextstruktur zugeordneten Ressourcen frei zu geben, unabhängig davon, ob Sie den Kontext initialisiert haben, der von der Standardmäßig-Warteschlangenrückrufroutine mit [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) oder [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)verwendet wird.

 

 



