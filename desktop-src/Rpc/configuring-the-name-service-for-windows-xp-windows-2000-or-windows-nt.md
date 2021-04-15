---
title: Konfigurieren des Namens Dienstanbieter
description: Ab Windows 2000 wählt das Setup Programm beim Installieren des Windows SDK automatisch Microsoft Locator als Name Service Provider aus. Sie können den Namen des Dienstanbieters über die Systemsteuerung ändern.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c1c895aecb3bdf74189461cd6aa9ee814b2d68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471229"
---
# <a name="configuring-the-name-service"></a>Konfigurieren des Namens Dienstanbieter

Ab Windows 2000 wählt das Setup Programm beim Installieren des Windows SDK automatisch Microsoft Locator als Name Service Provider aus. Sie können den Namen des Dienstanbieters über die Systemsteuerung ändern.

Der Host Computer, der die nsid ausführt, fungiert als Gateway für den DCE-Zell Verzeichnisdienst und übergibt NSI-Funktionsaufrufe zwischen Computern, auf denen Microsoft-Betriebssysteme und DCE-Computer ausgeführt werden. Eine Netzwerkadresse kann bis zu 80 Zeichen lang sein – z. b. 11.1.9.169 ist eine gültige Adresse.

> [!Note]  
> Sie müssen über das DCE CDs-Produkt der Digital Equipment Corporation verfügen, um die DCE-CDs als Name Service Provider zu konfigurieren. Weitere Informationen zu DCE CDs finden Sie in der Dokumentation der Digital Equipment Corporation.

 

**So konfigurieren Sie den Namen Dienstanbieter neu**

1.  Klicken Sie in der Systemsteuerung auf das Symbol " **Netzwerkverbindungen** ". Das Fenster **Netzwerkverbindungen** wird angezeigt.
2.  Wählen Sie die zu konfigurier Netzwerkverbindung aus, klicken Sie mit der rechten Maustaste, und wählen Sie im Kontextmenü **Eigenschaften** aus. Das Dialogfeld **Verbindungs Eigenschaften** wird angezeigt.
3.  Wählen Sie im Dialogfeld **Verbindungs Eigenschaften** die Option **Client für Microsoft-Netzwerke** , und klicken Sie auf die Schaltfläche **Eigenschaften** . Das Dialogfeld **Client für Microsoft-Netzwerk Eigenschaften** wird angezeigt.
4.  Öffnen Sie im Dialogfeld **Client für Microsoft-Netzwerk Eigenschaften** die Dropdown Liste **Name Service Provider** , und wählen Sie einen Namen Anbieter aus der Liste aus.
    1.  Wenn Sie Microsoft Locator auswählen, klicken Sie auf OK. Der Konfigurations Vorgang ist dann beendet.
    2.  Wenn Sie den DCE-Zell Verzeichnisdienst auswählen, geben Sie im Feld **Netzwerkadresse** den Namen des Host Computers ein, auf dem der NSI-Daemon (nsid) ausgeführt wird, und klicken Sie dann auf OK.

**So konfigurieren Sie den Namen Dienstanbieter für Windows 2000 neu**

1.  Klicken Sie in der Systemsteuerung auf das **Netzwerk** Symbol.

    Das Dialogfeld **Netzwerk** wird angezeigt.

2.  Klicken Sie im Dialogfeld **Netzwerk** auf **Konfigurieren**.
3.  Wählen Sie in der Liste **networksoftware** die Option **RPC-Konfiguration** aus.

    Das Dialogfeld **Konfiguration des RPC-namens Dienstanbieters** wird angezeigt.

4.  Wählen Sie im Dialogfeld **Konfiguration des RPC-namens Dienstanbieters** in der Liste einen Namen Dienstanbieter aus.
    1.  Wenn Sie Microsoft Locator auswählen, klicken Sie auf OK. Der Konfigurations Vorgang ist dann beendet.
    2.  Wenn Sie den DCE-Zell Verzeichnisdienst auswählen, geben Sie im Feld **Netzwerkadresse** den Namen des Host Computers ein, auf dem der NSI-Daemon (nsid) ausgeführt wird, und klicken Sie dann auf OK.

 

 




