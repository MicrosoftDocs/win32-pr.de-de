---
description: Die Hardwarekonfigurationsfunktionen rufen Informationen wie Prozessor, Hardwareprofil und Tastaturinformationen ab.
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: Hardware Configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e396b2d08b489e92c7a407ca892250135fdd3d174d16de50d0c2d75428a88dce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764418"
---
# <a name="hardware-configuration"></a>Hardware Configuration

Die Hardwarekonfigurationsfunktionen rufen Informationen wie Prozessor, Hardwareprofil und Tastaturinformationen ab.

Die [**GetSystemInfo-Funktion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) ruft Prozessor- und Arbeitsspeicherinformationen ab, z. B. Seitengröße, OEM-Bezeichner (Original Equipment Manufacturer), Anzahl und Typ der Prozessoren, Anwendungsadressenbereich und so weiter. Die [**IsProcessorFeaturePresent-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) ruft Informationen zu den gleitkommabasierten Vorgängen und Anweisungssätzen ab, die vom Prozessor unterstützt werden.

Die [**GetCurrentHwProfile-Funktion**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) ruft Informationen zum Hardwareprofil ab. Das Hardwareprofil enthält Informationen wie z. B. den Andockstatus, den global eindeutigen Bezeichner (Globally Unique Identifier, GUID) und den Anzeigenamen für das Profil. Die [**GetKeyboardType-Funktion**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) ruft Informationen wie den Tastaturtyp und die Anzahl der Funktionstasten auf der aktuellen Tastatur ab.

 

 
