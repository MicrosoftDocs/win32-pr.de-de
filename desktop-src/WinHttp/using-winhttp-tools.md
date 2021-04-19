---
description: Die Befehle, die Sie in Windows Vista und höher zum Konfigurieren von Proxy-und Ablauf Verfolgungs Einstellungen für Windows HTTP verwenden können, finden Sie unter Netsh Commands for Windows Hypertext Transfer Protocol (WinHTTP).
ms.assetid: 81f6b25e-ea14-4dbd-a715-926db7cf90e7
title: Verwenden von WinHTTP-Tools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e402962dc34cbf654fa8db49f96b86e7406a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348782"
---
# <a name="using-winhttp-tools"></a>Verwenden von WinHTTP-Tools

Die Befehle, die Sie in Windows Vista und höher zum Konfigurieren von Proxy-und Ablauf Verfolgungs Einstellungen für Windows HTTP verwenden können, finden Sie unter [Netsh Commands for Windows Hypertext Transfer Protocol (WinHTTP)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)).

**Windows Server 2003 und früher:** Es stehen verschiedene Tools zur Verfügung, die Sie beim Schreiben und Debuggen Ihrer Anwendungen unterstützen. Diese werden in den folgenden Themen erläutert:

-   [WinHttpCfg.exe](winhttpcertcfg-exe--a-certificate-configuration-tool.md) ermöglicht es Administratoren, Client Zertifikate in einem beliebigen [*Zertifikat Speicher*](glossary.md) zu installieren und zu konfigurieren, auf den das Internet Server Web Application Manager-Konto (IWAM) zugreifen kann. Außerdem entfällt das Tool darauf, dass Sie spezielle Konten, wie z. b. das IWAM-Konto, benötigen, um bei Verwendung von Active Server Pages (ASP) Zugriff auf Zertifikate zu erhalten.
-   [Netsh.exe-oder ProxyCfg.exe Proxy Konfigurationstools](proxycfg-exe--a-proxy-configuration-tool.md) kann verwendet werden, um Proxy Server mit Microsoft Windows HTTP-Diensten (WinHTTP) zu konfigurieren.
-   [Winhttptracecfg, ein Konfigurations Tool](winhttptracecfg-exe--a-trace-configuration-tool.md) für die Ablauf Verfolgung, bietet die Möglichkeit, WinHTTP-Funktionen und den entsprechenden Netzwerk Datenverkehr zu überwachen. Das Debuggen von Anwendungen, bei denen verschlüsselte Übertragungsprotokolle verwendet werden, wie z. b. Secure Sockets Layer (SSL), schließt das Auslagern von Paketen auf der Netzwerk Transport Ebene aus und erfordert die Möglichkeit, den Datenverkehr zwischen Client und Server abzufangen, nachdem er entschlüsselt wurde Die WinHTTP-Ablauf Verfolgungs Funktion verfügt über eine Reihe von Funktionen, mit denen der datenverkehrstream zwischen Client und Server abgefangen werden konnte.

 

 
