---
description: Wenn ein neuer Thread durch die Funktion "foratethread" oder "forateremotethread" erstellt wird, wird ein Handle für den Thread zurückgegeben.
ms.assetid: ff91fe27-9773-4185-bc1e-57e897be3821
title: Thread Handles und-Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501d449bdb34d158ad14e52409967d4ef17f62f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865055"
---
# <a name="thread-handles-and-identifiers"></a>Thread Handles und-Bezeichner

Wenn ein neuer Thread durch die Funktion " [**foratethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " oder " [**forateremotethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) " erstellt wird, wird ein Handle für den Thread zurückgegeben. Standardmäßig verfügt dieses Handle über vollständige Zugriffsrechte, und – unterliegt der Sicherheits Zugriffs Überprüfung – kann in allen Funktionen verwendet werden, die ein Thread handle akzeptieren. Dieses Handle kann von untergeordneten Prozessen geerbt werden, abhängig von dem Vererbungs Flag, das bei der Erstellung angegeben wird. Das Handle kann durch [**duplitorehandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)dupliziert werden, sodass Sie ein Thread Handle mit einer Teilmenge der Zugriffsrechte erstellen können. Das Handle ist bis zum Schließen gültig, auch nachdem der Thread, den es darstellt, beendet wurde.

Die Funktionen " [**foratethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " und " [**forateremotethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) " geben auch einen Bezeichner zurück, der den Thread im gesamten System eindeutig identifiziert. Ein Thread kann die [**GetCurrentThreadID**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) -Funktion verwenden, um einen eigenen Thread Bezeichner zu erhalten. Die Bezeichner sind ab dem Zeitpunkt gültig, zu dem der Thread erstellt wird, bis der Thread beendet wurde. Beachten Sie, dass der Thread Bezeichner niemals 0 sein wird.

Wenn Sie einen Thread Bezeichner haben, können Sie das Thread handle abrufen, indem Sie die [**openthread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) -Funktion aufrufen. Mit **openthread** können Sie die Zugriffsrechte des Handles angeben und angeben, ob es vererbt werden kann.

Ein Thread kann die [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) -Funktion verwenden, um ein *Pseudo handle* zum eigenen Thread Objekt abzurufen. Dieses Pseudo Handle ist nur für den aufrufenden Prozess gültig. Sie kann nicht für die Verwendung durch andere Prozesse geerbt oder dupliziert werden. Um das eigentliche Handle für den Thread mit einem Pseudo Handle zu erhalten, verwenden Sie die [**duplitorandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) -Funktion.

Um die Threads eines Prozesses aufzulisten, verwenden Sie die [**Thread32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32first) -Funktion und die [**Thread32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-thread32next) -Funktion.

 

 
