---
description: Wenn ein neuer Prozess von der Funktion "forateprocess" erstellt wird, werden die Handles des neuen Prozesses und des zugehörigen primären Threads zurückgegeben.
ms.assetid: cf6b80de-de02-4222-a414-e940ffaed8fe
title: Prozess Handles und Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a1ec0acb6535f8f64b9f4bd0815392d61fccbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345448"
---
# <a name="process-handles-and-identifiers"></a>Prozess Handles und Bezeichner

Wenn ein neuer Prozess von der Funktion " [**forateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " erstellt wird, werden die Handles des neuen Prozesses und des zugehörigen primären Threads zurückgegeben. Diese Handles werden mit vollständigen Zugriffsrechten erstellt, und – unterliegt der Sicherheits Zugriffs Überprüfung – kann in allen Funktionen verwendet werden, die Thread-oder Prozess Handles akzeptieren. Diese Handles können von untergeordneten Prozessen geerbt werden, abhängig von dem Vererbungs Flag, das bei der Erstellung angegeben wird. Die Handles sind bis zum Schließen gültig, auch nachdem der Prozess oder Thread, den Sie darstellen, beendet wurde.

Die Funktion " [**deateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " gibt auch einen Bezeichner zurück, der den Prozess im gesamten System eindeutig identifiziert. Ein Prozess kann die [**GetCurrentProcessId-**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) Funktion verwenden, um eine eigene Prozess-ID (auch als Prozess-ID oder PID bezeichnet) zu erhalten. Der Bezeichner ist ab dem Zeitpunkt gültig, zu dem der Prozess erstellt wird, bis der Prozess beendet wurde. Ein Prozess kann die [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) -Funktion verwenden, um den Prozess Bezeichner des übergeordneten Prozesses abzurufen.

Wenn Sie einen Prozess Bezeichner haben, können Sie das Prozess handle abrufen, indem Sie die [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) -Funktion aufrufen. Mit **OpenProcess** können Sie die Zugriffsrechte des Handles angeben und angeben, ob es vererbt werden kann.

Ein Prozess kann die [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) -Funktion verwenden, um ein Pseudo Handle zum eigenen Prozess Objekt abzurufen. Dieses Pseudo Handle ist nur für den aufrufenden Prozess gültig. Sie kann nicht für die Verwendung durch andere Prozesse geerbt oder dupliziert werden. Um das eigentliche Handle für den Prozess zu erhalten, nennen Sie die [**duplialisierandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) -Funktion.

 

 
