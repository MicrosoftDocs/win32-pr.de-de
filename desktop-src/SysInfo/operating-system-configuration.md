---
description: Das Windows verzeichnis ist das Verzeichnis, das Windows-basierten Anwendungen, Initialisierungsdateien und Hilfedateien enthält. Die GetWindowsDirectory-Funktion ruft den Pfad zu diesem Verzeichnis ab.
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: Konfiguration des Betriebssystems
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 747a881568f9814152a230880d38891590d33ffc67cfa5e8178adfa66c1a01fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885287"
---
# <a name="operating-system-configuration"></a>Konfiguration des Betriebssystems

Das *Windows verzeichnis* ist das Verzeichnis, das Windows-basierten Anwendungen, Initialisierungsdateien und Hilfedateien enthält. Die [**GetWindowsDirectory-Funktion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) ruft den Pfad zu diesem Verzeichnis ab.

Das *Systemverzeichnis* ist das Verzeichnis, das Dynamic Link-Bibliotheken, Treiber und Schriftartdateien enthält. Die [**GetSystemDirectory-Funktion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) ruft den Pfad zu diesem Verzeichnis ab.

Die [**GetUserName-Funktion**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) ruft den Namen des Benutzers ab, der derzeit am System angemeldet ist. Der Benutzername ist entweder der Anmeldename oder der vollständige Name des Benutzers, wenn letzterer in der Registrierung enthalten ist.

Eine *Umgebungsvariable* ist eine symbolische Variable, die ein Element des Systems darstellt, z. B. einen Pfad, einen Dateinamen oder andere Literaldaten. Die Umgebungsvariable PATH stellt beispielsweise die Verzeichnisse dar, in denen nach ausführbaren Dateien gesucht werden soll. Wenn sich ein Benutzer anmeldet, initialisiert das System Umgebungsvariablen basierend auf dem Umgebungsabschnitt der Registrierung. Die [**Funktion ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) ruft die Werte der angegebenen Umgebungsvariablen ab.

Zusätzliche Informationen werden von der [**IADsADSystemInfo-Schnittstelle**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) bereitgestellt.

 

 
