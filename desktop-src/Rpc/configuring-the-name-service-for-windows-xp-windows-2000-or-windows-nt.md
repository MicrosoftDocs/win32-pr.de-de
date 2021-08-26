---
title: Konfigurieren des Namensdiensts
description: Ab Windows 2000 wählt das Setupprogramm bei der Installation des Windows SDK automatisch Microsoft Locator als Namendienstanbieter aus. Sie können den Namensdienstanbieter über Systemsteuerung ändern.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84450f4408ac0e90be04cfff7d1cbc92890cde4434969431a986e9cda378ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022440"
---
# <a name="configuring-the-name-service"></a>Konfigurieren des Namensdiensts

Ab Windows 2000 wählt das Setupprogramm bei der Installation des Windows SDK automatisch Microsoft Locator als Namendienstanbieter aus. Sie können den Namensdienstanbieter über Systemsteuerung ändern.

Der Hostcomputer, auf dem die nsid ausgeführt wird, fungiert als Gateway zum DCE Cell Directory Service und übergibt NSI-Funktionsaufrufe zwischen Computern, auf denen Microsoft-Betriebssysteme und DCE-Computer ausgeführt werden. Eine Netzwerkadresse kann bis zu 80 Zeichen lang sein, z.B. ist 11.1.9.169 eine gültige Adresse.

> [!Note]  
> Sie benötigen das DCE CDS-Produkt der Digital Equipment Corporation, um DCE CDS als Name-Dienstanbieter zu konfigurieren. Informationen zu DCE CDS finden Sie in der Dokumentation der Digital Equipment Corporation.

 

**So konfigurieren Sie den Namensdienstanbieter neu**

1.  Klicken Sie in Systemsteuerung auf das Symbol **Netzwerkverbindungen.** Das Fenster **Netzwerkverbindungen** wird angezeigt.
2.  Wählen Sie die zu konfigurierende Netzwerkverbindung aus, klicken Sie mit der rechten Maustaste darauf, und wählen Sie im Kontextmenü **Eigenschaften** aus. Das Dialogfeld **Verbindungseigenschaften** wird angezeigt.
3.  Wählen Sie im Dialogfeld **Verbindungseigenschaften** die Option **Client für Microsoft-Netzwerke** aus, und klicken Sie auf die Schaltfläche **Eigenschaften.** Das Dialogfeld **Client für Microsoft-Netzwerkeigenschaften** wird angezeigt.
4.  Öffnen Sie im Dialogfeld **Client für Microsoft-Netzwerkeigenschaften** die Dropdownliste **Name-Dienstanbieter,** und wählen Sie einen Namenanbieter aus der Liste aus.
    1.  Wenn Sie Microsoft Locator auswählen, klicken Sie auf OK. Der Konfigurationsprozess ist dann abgeschlossen.
    2.  Wenn Sie den DCE-Zellenverzeichnisdienst auswählen, geben Sie im Feld **Netzwerkadresse** den Namen des Hostcomputers ein, auf dem der NSI-Daemon (nsid) ausgeführt wird, und klicken Sie dann auf OK.

**So konfigurieren Sie den Namensdienstanbieter für Windows 2000 neu**

1.  Klicken Sie in Systemsteuerung auf das **Netzwerksymbol.**

    Das Dialogfeld **Netzwerk** wird angezeigt.

2.  Klicken Sie im Dialogfeld **Netzwerk** auf **Konfigurieren.**
3.  Wählen Sie in der Liste **NetworkSoftware** die Option **RPC-Konfiguration aus.**

    Das Dialogfeld KONFIGURATION DES **RPC-Namensdienstanbieters** wird angezeigt.

4.  Wählen Sie im Dialogfeld KONFIGURATION des **RPC-Namensdienstanbieters** in der Liste einen Namendienstanbieter aus.
    1.  Wenn Sie Microsoft Locator auswählen, klicken Sie auf OK. Der Konfigurationsprozess ist dann abgeschlossen.
    2.  Wenn Sie den DCE-Zellenverzeichnisdienst auswählen, geben Sie im Feld **Netzwerkadresse** den Namen des Hostcomputers ein, auf dem der NSI-Daemon (nsid) ausgeführt wird, und klicken Sie dann auf OK.

 

 




