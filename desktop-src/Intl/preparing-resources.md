---
description: Die Ressourcen Vorbereitung für eine MUI-Anwendung unterstützt sowohl Win32 PE-als auch nicht-Win32 PE-Modelle.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Vorbereiten von Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ca7655535318fa7a385993e6a55f9e7b6110ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352663"
---
# <a name="preparing-resources"></a>Vorbereiten von Ressourcen

Die Ressourcen Vorbereitung für eine MUI-Anwendung unterstützt sowohl Win32 PE-als auch nicht-Win32 PE-Modelle. Win32 PE-Ressourcen werden in PE-basierten Dateien, z. b. dll-, exe-oder sys-Dateien, bereitgestellt. Nicht-Win32 PE-Ressourcen werden in einem benutzerdefinierten Modul Ihrer Wahl bereitgestellt.

> [!Note]  
> Es wird dringend empfohlen, Win32 PE-Ressourcen für Win32-MUI-Anwendungen zu verwenden, da diese Ressourcen vollständig von der MUI-Ressourcen Technologie unterstützt werden. Nicht-Win32 PE-Ressourcen Dateien können durch Aufrufen der [**getfilemuipath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) -Funktion aufgerufen werden, wie in Suchen von [nicht-Win32 PE-Ressourcen](locating-non-win32-pe-resources.md)beschrieben, aber die Anwendung muss eigene Funktionen bereitstellen, um die erforderlichen Ressourcen zu finden und zu laden.

 

Dieser Abschnitt enthält die folgenden Themen:

-   [Erstellen der Ressourcen Datei für die Basis Sprache](creating-the-base-language-resource-file.md)
-   [Verwenden von Registrierungs Zeichenfolgen](using-registry-string-redirection.md)
-   [Vorbereiten einer Ressourcen Konfigurationsdatei](preparing-a-resource-configuration-file.md)

 

 



