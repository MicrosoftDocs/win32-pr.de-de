---
description: Windows Der Update-Agent (WUA) aktualisiert sich automatisch selbst, wenn er mit einem WSUS-Server (Windows Server Update Services) oder mit Windows Update verbunden ist.
ms.assetid: 829112ab-b240-4cc4-8053-18b484934886
title: Aktualisieren Windows Update-Agents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388475aaf9fa83413a916520035eb9539187390bf5a3bd8f5c836cb1b176357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814651"
---
# <a name="updating-windows-update-agent"></a>Aktualisieren Windows Update-Agents

Windows Der Update-Agent (WUA) aktualisiert sich selbst auf verschiedene Weise, je nach Version von Windows, die auf dem Gerät ausgeführt wird. Alte WuA-Versionen können möglicherweise keine Verbindung mit aktuellen Updatediensten herstellen, sind möglicherweise nicht mit allen Updates kompatibel und unterstützen möglicherweise nicht alle dokumentierten APIs. So stellen Sie sicher, dass WUA vollständig aktualisiert und kompatibel ist.

**Bei Versionen von Windows ab Windows 7 und Windows Server 2008 R2**

Windows Updates des Update-Agents (WUA) sind in den regelmäßigen regelmäßigen Updates für Windows enthalten, die über Windows Update oder an Windows Server Update Services (WSUS) verteilt werden. Sie müssen keine besonderen Schritte ausführen, um WUA auf diesen Windows Versionen zu aktualisieren.

**Auf Versionen von Windows vor Windows 7 und Windows Server 2008 R2**

WUA aktualisiert sich automatisch selbst, wenn Automatische Updates eine Verbindung mit Windows Update oder WSUS herstellt.

Wenn Automatische Updates noch nicht erfolgreich ausgeführt wurde, ist es möglich, dass auf einem Gerät, auf dem diese Windows Versionen ausgeführt werden, eine ältere WuA-Version ausgeführt wird, die nicht alle dokumentierten APIs unterstützt. Wenn Sie ein WU_E_SELFUPDATE_REQUIRED Ergebnis erhalten, wenn Sie die WUA-API zum Durchführen einer Überprüfung, eines Downloads oder einer Installation verwenden, wird Ihnen dieser Fehler angezeigt, dass die installierte Version von WUA zu alt ist, um eine Verbindung mit aktuellen Windows Updatediensten herzustellen. Sie können die normalen WUA-APIs nicht verwenden, um WUA unter diesen Betriebssystemen zu aktualisieren. 

Ein Benutzer kann WUA manuell auf eine aktuelle Version aktualisieren, indem er die Windows Update-Systemsteuerung öffnet, Nach Updates suchen auswählt und dann das angezeigte Selbstupdate akzeptiert. Alternativ können Sie WUA programmgesteuert aktualisieren.

**So aktualisieren Sie WUA programmgesteuert auf Versionen von Windows vor Windows 7 und Windows Server 2008 R2**

1.  Verwenden Sie die [WinHTTP-APIs,](../winhttp/winhttp-start-page.md) um [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab)herunterzuladen.
2.  Überprüfen Sie mithilfe der [Kryptografiefunktionen,](../seccrypto/cryptography-functions.md) ob die heruntergeladene Kopie von [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab) über eine digitale Signatur von Microsoft verfügt. Wenn Sie die digitale Signatur nicht überprüfen können, beenden Sie .
3.  Verwenden Sie die APIs der [Dateidekomprimierungsschnittstelle,](../devnotes/cabinet-api-functions.md) um die XML-Datei aus [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab)zu extrahieren.
4.  Verwenden Sie die APIs Microsoft XML Core Services ([MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85))), um die XML-Datei zu laden und den Knoten WURedist/StandaloneRedist/architecture für die Architektur des Computers zu suchen. Suchen Sie beispielsweise für x86 den Knoten WURedist/StandaloneRedist/architecture mit dem **Name-Attribut** x86.
5.  Rufen Sie [**IWindowsUpdateAgentInfo::GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) auf, um die aktuelle Version von WUA zu bestimmen. Wenn **IWindowsUpdateAgentInfo::GetInfo** eine Versionsnummer zurückgibt, die mindestens so hoch ist wie das **clientVersion-Attribut** im Architekturknoten, den Sie gefunden haben, beenden Sie .
6.  Verwenden [](/previous-versions/windows/desktop/ms763742(v=vs.85)) Sie die MSXML-APIs, um das **downloadUrl-Attribut** aus dem von Ihnen gefundenen Architekturknoten zu lesen. **downloadUrl** enthält die Download-URL für das entsprechende WUA-Installationsprogramm für die Architektur des Computers.
7.  Verwenden [](../winhttp/winhttp-start-page.md) Sie die WinHTTP-APIs, um das entsprechende Installationsprogramm herunterzuladen.
8.  Verwenden Sie die [**CreateProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) oder eine ähnliche API, um das heruntergeladene Installationsprogramm auszuführen.

 

 
