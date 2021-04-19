---
description: Die Hardware Konfigurationsfunktionen rufen Informationen wie Prozessor, Hardwareprofil und Tastatur Informationen ab.
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: Hardware Configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee4abe543f0603ab6cf80ef395fe56e4e3300c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350891"
---
# <a name="hardware-configuration"></a>Hardware Configuration

Die Hardware Konfigurationsfunktionen rufen Informationen wie Prozessor, Hardwareprofil und Tastatur Informationen ab.

Die Funktion " [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) " ruft Prozessor-und Arbeitsspeicher Informationen ab, wie z. b. die Seitengröße, den OEM-Bezeichner (Original Equipment Manufacturer), die Anzahl und den Typ der Prozessoren, den Adressbereich der Anwendung usw. Die [**isprocessorfeaturepräsentiert**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) -Funktion Ruft Informationen zu den Gleit Komma Vorgängen und Anweisungs Sätzen ab, die vom Prozessor unterstützt werden.

Die Funktion " [**gethappthwprofile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) " Ruft Informationen über das Hardwareprofil ab. Das Hardwareprofil enthält Informationen wie den Andock Zustand, Globally Unique Identifier (GUID) und den anzeigen Amen für das Profil. Die [**getkeyboardtype**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) -Funktion ruft solche Informationen als den Typ der Tastatur und die Anzahl der Funktionstasten auf der aktuellen Tastatur ab.

 

 
