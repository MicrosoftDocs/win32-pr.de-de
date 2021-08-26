---
description: Wenn ein neuer Prozess von der CreateProcess-Funktion erstellt wird, werden Handles des neuen Prozesses und seines primären Threads zurückgegeben.
ms.assetid: cf6b80de-de02-4222-a414-e940ffaed8fe
title: Verarbeiten von Handles und Bezeichnern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4603b3d217db0870aeb890b05c7a416f46f2309ea9a0230b33d150387ebc5173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031770"
---
# <a name="process-handles-and-identifiers"></a>Verarbeiten von Handles und Bezeichnern

Wenn ein neuer Prozess von der [**CreateProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) erstellt wird, werden Handles des neuen Prozesses und seines primären Threads zurückgegeben. Diese Handles werden mit Vollzugriffsrechten erstellt und können – je nach Überprüfung des Sicherheitszugriffs – in jeder der Funktionen verwendet werden, die Thread- oder Prozesshandles akzeptieren. Diese Handles können von untergeordneten Prozessen geerbt werden, abhängig vom Vererbungsflag, das beim Erstellen angegeben wird. Die Handles sind bis zum Schließen gültig, auch nachdem der Prozess oder Thread, den sie darstellen, beendet wurde.

Die [**CreateProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) gibt auch einen Bezeichner zurück, der den Prozess im gesamten System eindeutig identifiziert. Ein Prozess kann die [**GetCurrentProcessId-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) verwenden, um einen eigenen Prozessbezeichner (auch als Prozess-ID oder PID bezeichnet) abzurufen. Der Bezeichner ist gültig ab dem Zeitpunkt, zu dem der Prozess erstellt wird, bis der Prozess beendet wurde. Ein Prozess kann die [**Process32First-Funktion**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) verwenden, um den Prozessbezeichner des übergeordneten Prozesses abzurufen.

Wenn Sie über einen Prozessbezeichner verfügen, können Sie das Prozesshandle abrufen, indem Sie die [**OpenProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) aufrufen. **Mit OpenProcess** können Sie die Zugriffsrechte des Handles angeben und angeben, ob es geerbt werden kann.

Ein Prozess kann die [**GetCurrentProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) verwenden, um ein Pseudohandle für sein eigenes Prozessobjekt abzurufen. Dieses Pseudohandle ist nur für den aufrufenden Prozess gültig. sie kann nicht geerbt oder für die Verwendung durch andere Prozesse dupliziert werden. Rufen Sie die [**DuplicateHandle-Funktion**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) auf, um das echte Handle für den Prozess abzurufen.

 

 
