---
description: Die Befehle, die Sie in Windows Vista und höher verwenden können, um Proxy- und Ablaufverfolgungseinstellungen für Windows HTTP zu konfigurieren, finden Sie unter Netsh-Befehle für Windows Hypertext Transfer Protocol (WINHTTP).
ms.assetid: 81f6b25e-ea14-4dbd-a715-926db7cf90e7
title: Verwenden von WinHTTP-Tools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813b71ab56ef9b6705d7ead31412e32339495cb400ad87bd22060cb3f94c3b6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413170"
---
# <a name="using-winhttp-tools"></a>Verwenden von WinHTTP-Tools

Die Befehle, die Sie in Windows Vista und höher verwenden können, um Proxy- und Ablaufverfolgungseinstellungen für Windows HTTP zu konfigurieren, finden Sie unter [Netsh-Befehle für Windows Hypertext Transfer Protocol (WINHTTP).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10))

**Windows Server 2003 und früher:** Es stehen mehrere Tools zur Verfügung, mit denen Sie Ihre Anwendungen schreiben und debuggen können. Sie werden in den folgenden Themen erläutert:

-   WinHttpCfg.exe können Administratoren mithilfe eines Zertifikatkonfigurationstools Clientzertifikate [](glossary.md) in jedem Zertifikatspeicher installieren und [konfigurieren,](winhttpcertcfg-exe--a-certificate-configuration-tool.md) auf den das Internet Server Web Application Manager-Konto (IWAM) zugreifen kann. Das Tool entfällt auch die Notwendigkeit, besondere Maßnahmen für Konten wie das IWAM-Konto zu unternehmen, um zugriff auf Zertifikate zu erhalten, wenn sie Active Server Pages (ASP) verwenden.
-   [Netsh.exe proxy ProxyCfg.exe proxy Konfigurationstools](proxycfg-exe--a-proxy-configuration-tool.md) kann verwendet werden, um Proxyserver mit Microsoft Windows HTTP Services (WinHTTP) zu konfigurieren.
-   [WinHttpTraceCfg, ein Ablaufverfolgungskonfigurationstool,](winhttptracecfg-exe--a-trace-configuration-tool.md) bietet die Möglichkeit, WinHTTP-Funktionen und den entsprechenden Netzwerkdatenverkehr zu überwachen. Das Debuggen von Anwendungen, die verschlüsselte Wire Protocols wie Secure Sockets Layer (SSL) verwenden, schließt das Ausspähen von Paketen auf der Netzwerktransportschicht aus und erfordert die Möglichkeit, Datenverkehr zwischen Client und Server abzufangen, nachdem er entschlüsselt wurde. Die WinHTTP-Ablaufverfolgungseinrichtung verfügt über eine Reihe von Funktionen zum Abfangen des Datenverkehrsstreams zwischen Client und Server.

 

 
