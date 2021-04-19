---
description: Windows Update-Agent (WUA) aktualisiert sich automatisch selbst, wenn er mit einem Windows Server Update Services (WSUS)-Server verbunden ist oder Windows Update.
ms.assetid: 829112ab-b240-4cc4-8053-18b484934886
title: Aktualisieren von Windows Update-Agent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00fe439b1bea377e2699f6fe5714b208ac5d951
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357361"
---
# <a name="updating-windows-update-agent"></a>Aktualisieren von Windows Update-Agent

Der Windows Update-Agent (WUA) wird auf verschiedene Weise aktualisiert, abhängig von der Windows-Version, die auf dem Gerät ausgeführt wird. Alte Versionen von WUA sind möglicherweise nicht in der Lage, eine Verbindung mit aktuellen Update Diensten herzustellen, sind möglicherweise nicht mit allen Updates kompatibel und unterstützen möglicherweise nicht alle dokumentierten APIs. Im folgenden wird erläutert, wie sichergestellt wird, dass WUA vollständig aktualisiert und kompatibel ist.

**Unter Windows-Versionen ab Windows 7 und Windows Server 2008 R2**

Die Updates von Windows Update-Agent (WUA) sind in regelmäßigen regelmäßigen Updates für Windows enthalten, die über Windows Update oder die Windows Server Update Services (WSUS) verteilt sind. Sie müssen keine besonderen Schritte ausführen, um WUA für diese Windows-Versionen zu aktualisieren.

**Unter Windows-Versionen vor Windows 7 und Windows Server 2008 R2**

WUA wird automatisch aktualisiert, wenn automatische Updates eine Verbindung mit Windows Update oder mit WSUS herstellt.

Wenn automatische Updates noch nicht erfolgreich ausgeführt wurde, ist es möglich, dass auf einem Gerät, auf dem diese Windows-Versionen ausgeführt werden, eine ältere Version von WUA ausgeführt wird, die nicht alle dokumentierten APIs unterstützt. Wenn Sie ein WU_E_SELFUPDATE_REQUIRED Ergebnis erhalten, wenn Sie die WUA-API zum Durchführen einer Überprüfung, eines Downloads oder einer Installation verwenden, wird mit diesem Fehler angezeigt, dass die installierte Version von WUA zu alt ist, um eine Verbindung mit aktuellen Windows Update Diensten herzustellen. Sie können die normalen WUA-APIs nicht zum Aktualisieren von WUA unter diesen Betriebssystemen verwenden. 

Ein Benutzer kann WUA manuell auf eine aktuelle Version aktualisieren, indem er die Windows Update Systemsteuerung öffnet, auf nach Updates suchen und dann das selbst Update annimmt, das angezeigt wird. Alternativ können Sie WUA Programm gesteuert aktualisieren.

**So aktualisieren Sie WUA auf Windows-Versionen vor Windows 7 und Windows Server 2008 R2 Programm gesteuert**

1.  Verwenden Sie die [WinHTTP](../winhttp/winhttp-start-page.md) -APIs, um [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab)herunterzuladen.
2.  Verwenden Sie die [Kryptografiefunktionen](../seccrypto/cryptography-functions.md) , um zu überprüfen, ob die heruntergeladene Kopie [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab) über eine digitale Signatur von Microsoft verfügt. Wenn die digitale Signatur nicht überprüft werden kann, können Sie den Vorgang abbrechen.
3.  Extrahieren Sie die XML-Datei mit den APIs für die [Datei Dekomprimierungs Schnittstelle](../devnotes/cabinet-api-functions.md) aus [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab).
4.  Verwenden Sie die Microsoft XML Core Services ([MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)))-APIs, um die XML-Datei zu laden und den Knoten wuredist/standaloneredist/Architecture für die Architektur des Computers zu suchen. Suchen Sie z. b. für x86 den Knoten wuredist/standaloneredist/Architecture mit dem **namens** Attribut x86.
5.  Aufrufen von [**iwindowsupdateagentinfo:: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) , um die aktuelle Version von WUA zu ermitteln. Wenn **iwindowsupdateagentinfo:: GetInfo** eine Versionsnummer zurückgibt, die mindestens so hoch ist wie das **Clientversion** -Attribut im Knoten "Architektur", den Sie gefunden haben, wird beendet.
6.  Verwenden Sie die [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) -APIs, um das **DownloadURL** -Attribut aus dem Knoten Architektur zu lesen, den Sie gefunden haben. **Download URL** gibt Ihnen die Download-URL für den entsprechenden WUA-Installer für die Architektur des Computers.
7.  Verwenden Sie die [WinHTTP](../winhttp/winhttp-start-page.md) -APIs, um den entsprechenden Installer herunterzuladen.
8.  Verwenden Sie die Funktion "up- [**Process**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " oder eine ähnliche API, um den heruntergeladenen Installer auszuführen.

 

 
