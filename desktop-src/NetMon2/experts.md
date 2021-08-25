---
description: Ein Experte ist eine Microsoft Win32-DLL (Dynamic Link Library), die netzwerkbasierten Datenverkehr analysiert, der von einem Netzwerkpaketanbieter (Network Packet Provider, NPP) erfasst und in einer Erfassungsdatei platziert wird.
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: Experte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2f4c3e34a9f6b8b36fdc6aa4793acfa5b652b9fa2c2117afc62943c0947af6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890915"
---
# <a name="expert"></a>Experte

Ein Experte ist eine Microsoft Win32-DLL (Dynamic Link Library), die netzwerkbasierten Datenverkehr analysiert, der von einem Netzwerkpaketanbieter (Network [*Packet Provider,*](n.md) NPP) erfasst und in einer Erfassungsdatei platziert wird. Nachdem die Daten erfasst und in einer Erfassungsdatei gespeichert wurden, arbeitet der Experte mit einem Parser zusammen, der auch als Protokollparser bezeichnet wird, um die Daten in der Datei zu analysieren. Beispielsweise können Sie die Frames der Erfassungsdatei untersuchen und einen [*Parser*](p.md) verwenden, um Protokolle wie Server Message Block (SMB) oder Transmission Control Protocol/Internet Protocol (TCP/IP) zu erkennen.

Sie können einen Experten so entwerfen, dass er mit allen Netzwerkmonitor Parsern und allen Parsern arbeitet, die Sie selbst erstellen.

Nachdem eine angeforderte Übereinstimmung von Protokollen einen bestimmten Frame identifiziert hat, extrahiert der Experte Daten aus dem Frame. Sie können den Experten programmieren, um Informationen in nutzbare Daten zu ändern, die Netzwerkmonitor Ereignisanzeige werden.

Sie können einen Experten zur Laufzeit konfigurieren und dann Netzwerkmonitor, um Benutzerkonfigurationsdaten für die Wiederverwendung mit verschiedenen Erfassungsdateien zu speichern. Sie können einen Experten verwenden, um Korrelationsdaten und benutzerdefinierte Lösungen für Endbenutzer zur Verfügung zu stellen. Weitere Informationen zum Erstellen von HTML-basierten Konfigurationsinformationen finden Sie auf der [Ereignisreferenzseite.](event-reference-page.md)

Während Netzwerkmonitor setup werden die folgenden Experten-DLLs im Unterverzeichnis Experts installiert:

-   Coalesce.dll
-   Propdist.dll
-   Protdist.dll
-   Resptime.dll
-   Tcpipe.dll
-   Topuser.dll

Wenn Sie mit Netzwerkmonitor, erstellt die [**DllMain-Funktion**](dllmain-expert.md) alle Experten im Unterverzeichnis experts. Wenn der Benutzer experten im **Menü** **Extras** der benutzeroberfläche Netzwerkmonitor auswählt, Netzwerkmonitor die Experten-DLLs. Der Experte wird über den Einstiegspunkt ["Experten](register-expert.md) registrieren" aufgerufen, um grundlegende Informationen zum Experten zu erhalten.

![Netzwerkmonitor-Experten (Dialogfeld)](images/expick.png)

Netzwerkmonitor ruft die folgenden Funktionen auf, um den Experten zu verwalten:

-   [**DllMain**](dllmain-expert.md)
-   [**Registrieren eines Experten**](register-expert.md)
-   [**Ausführung**](run.md)
-   [**Konfigurieren**](configure.md)

Der Experte muss jede der oben genannten Funktionen implementieren.

 

 



