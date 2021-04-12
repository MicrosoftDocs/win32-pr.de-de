---
description: Das Windows-Verzeichnis ist das Verzeichnis, das Windows-basierte Anwendungen, Initialisierungsdateien und Hilfedateien enthält. Die GetWindowsDirectory-Funktion Ruft den Pfad zu diesem Verzeichnis ab.
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: Konfiguration des Betriebssystems
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38aa2c2b6b4f6b3ac5caac78a89ad980a9bd074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217146"
---
# <a name="operating-system-configuration"></a>Konfiguration des Betriebssystems

Das *Windows-Verzeichnis* ist das Verzeichnis, das Windows-basierte Anwendungen, Initialisierungsdateien und Hilfedateien enthält. Die [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) -Funktion Ruft den Pfad zu diesem Verzeichnis ab.

Das *System Verzeichnis* ist das Verzeichnis, das Dynamic Link Libraries, Treiber und Schriftart Dateien enthält. Die [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) -Funktion Ruft den Pfad zu diesem Verzeichnis ab.

Die [**GetUsername**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) -Funktion Ruft den Namen des Benutzers ab, der derzeit beim System angemeldet ist. Der Benutzername ist entweder der Anmelde Name oder der vollständige Name des Benutzers, sofern er in der Registrierung enthalten ist.

Eine *Umgebungsvariable* ist eine symbolische Variable, die ein Element des Systems darstellt, z. b. einen Pfad, einen Dateinamen oder andere Literaldaten. Der Umgebungsvariablen Pfad stellt z. b. die Verzeichnisse dar, in denen nach ausführbaren Dateien gesucht werden soll. Wenn sich ein Benutzer anmeldet, initialisiert das System Umgebungsvariablen basierend auf dem Umgebungs Abschnitt der Registrierung. Die [**expandenvironment Strings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) -Funktion Ruft die Werte der angegebenen Umgebungsvariablen ab.

Weitere Informationen werden von der [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) -Schnittstelle bereitgestellt.

 

 
