---
description: Die Ressourcenvorbereitung für eine CSV-Anwendung unterstützt sowohl Win32 PE- als auch Nicht-Win32 PE-Modelle.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Vorbereiten von Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef40453ca6db40bed1c07bad80f7e21cb7adaa7ea48ae8ee5ce2a2a5c657ba2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040670"
---
# <a name="preparing-resources"></a>Vorbereiten von Ressourcen

Die Ressourcenvorbereitung für eine CSV-Anwendung unterstützt sowohl Win32 PE- als auch Nicht-Win32 PE-Modelle. Win32 PE-Ressourcen werden in PE-basierten Dateien wie .dll, .exe oder .sys dateien bereitgestellt. Nicht-Win32 PE-Ressourcen werden in einem benutzerdefinierten Modul Ihrer Wahl zusammengestellt.

> [!Note]  
> Es wird dringend empfohlen, Win32 PE-Ressourcen für Win32-WEBANWENDUNGen zu verwenden, da diese Ressourcen vollständig von der RESOURCES-Ressourcentechnologie unterstützt werden. Nicht-Win32 PE-Ressourcendateien können durch Aufrufen der [**GetFileMUIPath-Funktion**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) wie unter [Suchen von Nicht-Win32 PE-Ressourcen](locating-non-win32-pe-resources.md)beschrieben gefunden werden. Die Anwendung muss jedoch ihre eigene Funktionalität bereitstellen, um die erforderlichen Ressourcen zu suchen und zu laden.

 

Dieser Abschnitt enthält die folgenden Themen:

-   [Erstellen der Ressourcendatei der Basissprache](creating-the-base-language-resource-file.md)
-   [Verwenden der Umleitung von Registrierungszeichenfolgen](using-registry-string-redirection.md)
-   [Vorbereiten einer Ressourcenkonfigurationsdatei](preparing-a-resource-configuration-file.md)

 

 



