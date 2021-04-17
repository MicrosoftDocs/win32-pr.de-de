---
title: Klassen und Server
description: Klassen und Server
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d319fd985b812692e6d0bfc421c4bb9da2a2605c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391067"
---
# <a name="classes-and-servers"></a>Klassen und Server

COM verwendet **HKEY \_ - \_ Klassen** für Computer weite Einstellungen, bietet aber auch eine benutzerspezifische Konfiguration von CLSIDs, um Sicherheit und Flexibilität zu erhöhen. COM prüft zuerst **HKEY- \_ \_ \\ Software \\ Klassen für aktuelle Benutzer** , bevor Sie unter **HKEY \_ Classes \_ root** suchen. COM behält Computer weite Informationen im Zusammenhang mit CLSIDs unter **HKEY \_ Classes \_ root \\ CLSID** bei und speichert benutzerspezifische Klassen Informationen unter **HKEY \_ Current \_ User \\ Software \\ Classes \\ CLSID**.

COM-Server unterstützen die Selbstregistrierung. Bei einem in-Process-Server bedeutet dies, dass die dll die folgenden Funktionen exportieren muss:

-   [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

Sie müssen diese Funktionen mithilfe einer Modul Definitionsdatei, Linker Switches oder Compilerdirektiven explizit exportieren. Der Klassen Speicher verwendet diese Funktionen, um die lokale Registrierung zu konfigurieren, nachdem die Datei auf den Client Computer heruntergeladen wurde. Zusätzlich zum Klassen Speicher werden diese Funktionen auch von anderen Umgebungen verwendet, um Server auf Host Computern zu installieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von com-Anwendungen](registering-com-applications.md)
</dt> </dl>

 

 