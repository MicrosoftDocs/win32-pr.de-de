---
description: Ein Experte ist eine Microsoft Win32-DLL (Dynamic-Link Library), die den Netzwerk Datenverkehr analysiert, der von einem Netzwerk Paketanbieter (NPP) erfasst und in einer Erfassungs Datei abgelegt wird.
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: Experte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf5fc0096b15d590bf70859443667f2d9969f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340154"
---
# <a name="expert"></a>Experte

Ein Experte ist eine Microsoft Win32-DLL (Dynamic-Link Library), die den Netzwerk Datenverkehr analysiert, der von einem [*Netzwerk Paketanbieter*](n.md) (NPP) erfasst und in einer Erfassungs Datei abgelegt wird. Nachdem die Daten aufgezeichnet und in einer Erfassungs Datei gespeichert wurden, arbeitet der Experte mit einem Parser, der auch als Protokoll Parser bezeichnet wird, um die Daten in der Datei zu analysieren. Beispielsweise können Sie die Frames der Erfassungs Datei überprüfen und einen [*Parser*](p.md) verwenden, um Protokolle wie SMB (Server Message Block) oder TCP/IP (Transmission Control Protocol/Internet Protocol) zu erkennen.

Sie können einen Experten so entwerfen, dass er mit allen Netzwerkmonitor Parser und sämtlichen Parser arbeitet, die Sie selbst erstellen.

Nachdem eine angeforderte Entsprechung von Protokollen einen bestimmten Frame identifiziert hat, extrahiert der Experte Daten aus dem Frame. Sie können den Experten programmieren, um Informationen in nutzbare Daten zu bearbeiten, die in der Netzwerkmonitor Ereignisanzeige angezeigt werden.

Sie können einen Experten zur Laufzeit konfigurieren und dann Netzwerkmonitor verwenden, um die Benutzer Konfigurationsdaten für die Wiederverwendung mit unterschiedlichen Erfassungs Dateien zu speichern. Sie können einen Experten verwenden, um Korrelations Daten und benutzerdefinierte Lösungen für Endbenutzer bereitzustellen. Weitere Informationen zur Erstellung von HTML-basierten Konfigurationsinformationen finden Sie auf der [Seite mit der Ereignis Referenz](event-reference-page.md).

Während der Netzwerkmonitor-Installation werden die folgenden Experten-DLLs im Unterverzeichnis für Experten installiert:

-   Coalesce.dll
-   Propdist.dll
-   Protdist.dll
-   Resptime.dll
-   Tcpipe.dll
-   Topuser.dll

Wenn Sie Netzwerkmonitor starten, erstellt die [**DllMain**](dllmain-expert.md) -Funktion alle Experten im Unterverzeichnis "Experten". Wenn der Benutzer **im Menü Extras der Netzwerkmonitor** -Benutzeroberfläche auf **Experten** klickt, lädt Netzwerkmonitor die Experten-DLLs. Der Experte wird über den Einstiegspunkt " [Register Expert](register-expert.md) " aufgerufen, um grundlegende Details zum Experten bereitzustellen.

![Dialogfeld "Experten für Netzwerküberwachung"](images/expick.png)

Netzwerkmonitor die folgenden Funktionen zum Verwalten des Experten aufruft:

-   [**DllMain**](dllmain-expert.md)
-   [**Experte registrieren**](register-expert.md)
-   [**Ausführen**](run.md)
-   [**Konfigurieren**](configure.md)

Der Experte muss jede der vorangehenden Funktionen implementieren.

 

 



