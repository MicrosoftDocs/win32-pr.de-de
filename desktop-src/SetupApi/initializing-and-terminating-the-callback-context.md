---
description: Bevor die Standard Warteschlangen-Rückruf Routine verwendet werden kann, indem Sie entweder beim Ausführen eines Commits für eine Datei Warteschlange als Rückruf Routine angegeben wird, oder indem Sie Sie von einer benutzerdefinierten Rückruf Routine aus aufrufen, muss Sie initialisiert werden.
ms.assetid: e25a9787-a4a3-4d06-bf55-f6f7cfb23481
title: Initialisieren und Beenden des Rückruf Kontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03cb4c144cb9069d395ccd688e2a172680df8a12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351811"
---
# <a name="initializing-and-terminating-the-callback-context"></a>Initialisieren und Beenden des Rückruf Kontexts

Bevor die Standard Warteschlangen-Rückruf Routine verwendet werden kann, indem Sie entweder beim Ausführen eines Commits für eine Datei Warteschlange als Rückruf Routine angegeben wird, oder indem Sie Sie von einer benutzerdefinierten Rückruf Routine aus aufrufen, muss Sie initialisiert werden.

Die [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) -Funktion erstellt die Kontext Struktur, die von der Standard Warteschlangen-Rückruf Routine verwendet wird. Sie gibt einen void-Zeiger auf diese-Struktur zurück. Diese Struktur ist für den Vorgang der Standard Rückruf Routine unverzichtbar und muss an die Rückruf Routine übergeben werden. Hierzu können Sie entweder den void-Zeiger als Kontext in einem Aufruf von [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)angeben oder den void-Zeiger als Kontext Parameter angeben, wenn Sie [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) aus einer benutzerdefinierten Rückruf Routine aufrufen. Diese Kontext Struktur darf nicht geändert werden oder von der Setup Anwendung referenziert werden.

Die [**setupinitdefaultqueuecallbackex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) -Funktion initialisiert außerdem einen Kontext für die Standard Warteschlangen-Rückruf Routine. Sie gibt jedoch ein zweites Fenster an, mit dem eine vom Aufrufer angegebene Statusmeldung empfangen wird, wenn die Warteschlange eine Benachrichtigung sendet. Dies ermöglicht es Ihnen, die Standard Dialogfelder für Datenträger und Fehler zu verwenden und eine Statusanzeige z. b. in einem zweiten Fenster einzubetten, z. b. auf einer Seite des Installations-Assistenten.

Unabhängig davon, ob Sie den von der Standard Warteschlangen Rückruf-Routine verwendeten Kontext mit [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) oder [**setupinitdefaultqueuecallbackex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)initialisiert haben, rufen Sie [**setuptermdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) auf, um die beim Initialisieren der Kontext Struktur zugeordneten Ressourcen freizugeben.

 

 



