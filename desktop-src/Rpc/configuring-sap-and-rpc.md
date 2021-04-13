---
title: Konfigurieren von SAP und RPC
description: Novell NetWare-Netzwerkserver verwenden das Service Advertising Protocol (SAP), um Informationen zu verfügbaren Diensten im Netzwerk an andere vernetzte Geräte zu übertragen.
ms.assetid: 6d6ef481-fc09-4795-8954-33329912ff4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385d60168a52cbe5d31368959ec4f21d52f9ad80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2019
ms.locfileid: "104388837"
---
# <a name="configuring-sap-and-rpc"></a>Konfigurieren von SAP und RPC

Novell NetWare-Netzwerkserver verwenden das Service Advertising Protocol (SAP), um Informationen zu verfügbaren Diensten im Netzwerk an andere vernetzte Geräte zu übertragen. Ein Server kann eine SAP-Übertragung alle 60 Sekunden senden, um andere Netzwerkgeräte über die angebotenen Dienste zu informieren. Arbeitsstationen verwenden SAPS, um die Dienste zu suchen, die Sie im Netzwerk benötigen.

Windows umfasst einen SAP-Agent-Dienst, mit dem Windows-basierte Server mit NetWare-Servern interagieren können. Der SAP-Agent-Dienst lauscht auf den SAP-Anforderungen der Netzwerk Clients auf IPX-basierte Dienste, die auf dem-Server installiert sind und ausgeführt werden.

Software, die mithilfe von SAP Broadcast als Dienst über das Netzwerk angekündigt werden soll, gibt die SAP-Ankündigungen alle 60 Sekunden aus, ohne dass der SAP-Agent installiert ist. Damit Netzwerk Clients jedoch schnell einen IPX-Netzwerkdienst finden können, muss ein Server, auf dem eine Dienst Datenbank verwaltet wird, im Netzwerk verfügbar sein, um auf die Dienst Identifizierung zu antworten. Diese Dienst Datenbank wird in der Regel von einer Novell NetWare oder von einem mit NetWare kompatiblen Server verwaltet. Die Microsoft-Datei-und-Druckdienste für NetWare verwalten außerdem eine Datenbank des IPX-Netzwerk Diensts.

Wenn Gatewaydienste für NetWare (GSNW) auf einem Computer unter Windows Server installiert sind, wird der SAP-Typ 640 alle 60 Sekunden durch den RPC-Dienst (Remote Procedure Callcenter) übertragen. Diese SAP-Übertragung wird auch dann fortgesetzt, wenn der Benutzer die GSNW-und den SAP-Agent-Dienst deaktiviert.

Der RPC-Dienst führt den SAP-Broadcast aus, wenn die Client Dienste für NetWare (CSNW) und der SAP-Agent-Dienst installiert sind. Diese SAP-Übertragung wird auch dann fortgesetzt, wenn der Benutzer den SAP-Agent deaktiviert.

Standardmäßig prüft der RPC-Dienst auf dem Computer, auf dem Windows Server ausgeführt wird, Gatewaydienste für NetWare und den SAP-Agent-Dienst. Beim Installieren von Datei-und Druckdiensten für NetWare wird ein SAP-Agent installiert.

Auf dem Computer, auf dem eine Client Version von Windows mit CSNW ausgeführt wird, überprüft der RPC-Dienst den SAP-Agent-Dienst. Wenn die Dienste vorhanden sind, startet RPC ihren eigenen Thread, der den SAP-Broadcast-Typ 640 pro Minute durchführt.

> [!NOTE]
> Wenn Sie SAP nicht alle 60 Sekunden im Netzwerk übertragen möchten, können Sie SAP-Sendungen mithilfe des Registrierungs-Editors deaktivieren. Beachten Sie, dass die Verwendung des Registrierungs-Editors zu schwerwiegenden Problemen führen kann, die möglicherweise eine Neuinstallation des Betriebssystems erforderlich machen. Microsoft übernimmt keinerlei Garantie dafür, dass Probleme aufgrund nicht ordnungsgemäßer Verwendung des Registrierungs-Editors behoben werden können. Sie verwenden den Registrierungs-Editor auf eigene Gefahr. Sie sollten die Registrierung sichern, bevor Sie Sie bearbeiten.

 

**So konfigurieren Sie für SAP**

1.  Führen Sie den Registrierungs-Editor (Regedt32.exe) aus, und wechseln Sie zum folgenden Schlüssel in der Registrierung:

    **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ RPC**

2.  Klicken Sie im Menü **Bearbeiten** auf **Wert hinzufügen**, und verwenden Sie den folgenden Eintrag:
    1.  Wertname: der Name des Dienstanbieter Dienstanbieter
    2.  Datentyp: reg \_ SZ
    3.  Zeichenfolge: Nein
3.  Die Verwendung von No für die Zeichenfolge schaltet RPC-SAP-Broadcast aus. Wenn Sie für die Zeichenfolge ja verwenden, wird RPC-SAP-Broadcast auf
4.  Starten Sie den Computer neu, damit die Registrierungs Änderung wirksam wird.
    > [!NOTE]
    > Wenn die SAP-Sendungen fortgesetzt werden, nachdem Sie diese Schritte ausgeführt haben, können Sie einen Problem Behandlungsschritt ausprobieren. Löschen Sie den **ncacn- \_ SPX** -Zeichen folgen Wert im folgenden Registrierungsschlüssel:
    >
    > **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ RPC \\ Server-Protokolle\\**

     

> [!NOTE]  
> Dies sollte nur als Problem Behandlungsschritt verwendet werden. Wenn Sie diesen Zeichen folgen Wert löschen, werden SAP-Sendungen, die möglicherweise von einigen Programmen benötigt werden, vollständig deaktiviert.