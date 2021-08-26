---
description: Wenn ein neuer Thread von der CreateThread- oder CreateRemoteThread-Funktion erstellt wird, wird ein Handle für den Thread zurückgegeben.
ms.assetid: ff91fe27-9773-4185-bc1e-57e897be3821
title: Threadhandles und -bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6058388f450b4b44c371fc26b132ea785b22c29bc0a2fd86875f563371608512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031630"
---
# <a name="thread-handles-and-identifiers"></a>Threadhandles und -bezeichner

Wenn ein neuer Thread von der [**CreateThread-**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) oder [**CreateRemoteThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) erstellt wird, wird ein Handle für den Thread zurückgegeben. Standardmäßig verfügt dieses Handle über Vollzugriffsrechte und kann – je nach Überprüfung des Sicherheitszugriffs – in jeder der Funktionen verwendet werden, die ein Threadhandle akzeptieren. Dieses Handle kann von untergeordneten Prozessen geerbt werden, abhängig vom Vererbungsflag, das beim Erstellen angegeben wird. Das Handle kann von [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)dupliziert werden, wodurch Sie ein Threadhandle mit einer Teilmenge der Zugriffsrechte erstellen können. Das Handle ist bis zum Schließen gültig, auch nachdem der von ihm dargestellte Thread beendet wurde.

Die Funktionen [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) und [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) geben auch einen Bezeichner zurück, der den Thread im gesamten System eindeutig identifiziert. Ein Thread kann die [**GetCurrentThreadId-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) verwenden, um seinen eigenen Threadbezeichner abzurufen. Die Bezeichner sind von der Erstellung des Threads bis zum Beenden des Threads gültig. Beachten Sie, dass kein Threadbezeichner jemals 0 ist.

Wenn Sie über einen Threadbezeichner verfügen, können Sie das Threadhandle abrufen, indem Sie die [**OpenThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) aufrufen. **Mit OpenThread** können Sie die Zugriffsrechte des Handles angeben und angeben, ob es geerbt werden kann.

Ein Thread kann die [**GetCurrentThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) verwenden, um ein *Pseudohandle* für sein eigenes Threadobjekt abzurufen. Dieses Pseudohandle ist nur für den aufrufenden Prozess gültig. sie kann nicht für die Verwendung durch andere Prozesse geerbt oder dupliziert werden. Verwenden Sie die [**DuplicateHandle-Funktion,**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) um das echte Handle für den Thread mit einem Pseudohandle abzurufen.

Um die Threads eines Prozesses aufzuzählen, verwenden Sie die Funktionen [**Thread32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32first) und [**Thread32Next.**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32next)

 

 
