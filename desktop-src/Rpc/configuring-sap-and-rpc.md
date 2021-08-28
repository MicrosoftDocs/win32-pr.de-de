---
title: Konfigurieren von SAP und RPC
description: Verbund-NetWare-Netzwerkserver verwenden das Service Advertising Protocol (SAP), um Informationen zu verfügbaren Diensten im Netzwerk an andere Netzwerkgeräte zu übertragen.
ms.assetid: 6d6ef481-fc09-4795-8954-33329912ff4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf75a9ab45e97a66f1fc8d796b1d288367bb1c8d0e04b2ace4a90de7e21cbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931683"
---
# <a name="configuring-sap-and-rpc"></a>Konfigurieren von SAP und RPC

Verbund-NetWare-Netzwerkserver verwenden das Service Advertising Protocol (SAP), um Informationen zu verfügbaren Diensten im Netzwerk an andere Netzwerkgeräte zu übertragen. Ein Server sendet möglicherweise alle 60 Sekunden eine SAP-Übertragung, um andere Netzwerkgeräte über die von ihm angebotenen Dienste zu informieren. Arbeitsstationen verwenden SAPs, um dienste zu finden, die sie im Netzwerk benötigen.

Windows umfasst einen SAP-Agent-Dienst, um Windows-basierten Servern die Interaktion mit NetWare-Servern zu ermöglichen. Der SAP-Agent-Dienst lauscht auf SAP-Anforderungen von Netzwerkclients für IPX-basierte Dienste, die auf dem Server installiert sind und ausgeführt werden.

Software, die als Dienst über das Netzwerk über eine SAP-Übertragung angekündigt werden soll, gibt die SAP-Ankündigungen alle 60 Sekunden aus, ohne dass der SAP-Agent installiert ist. Damit Netzwerkclients jedoch schnell einen IPX-Netzwerkdienst finden können, muss ein Server, der eine Dienstdatenbank verwaltet, im Netzwerk verfügbar sein, um auf die Dienststandortanforderung zu reagieren. Diese Dienstdatenbank wird in der Regel von einem Reiner NetWare-Server oder einem NetWare-kompatiblen Server verwaltet. Microsoft File and Print Services for NetWare verwaltet auch eine IPX-Netzwerkdienstdatenbank.

Wenn auf einem Computer, auf dem Windows Server ausgeführt wird, Gateway Services für NetWare (GSNW) installiert ist, wird ein SAP-Typ 640 alle 60 Sekunden vom RPC-Dienst (Remote Procedure Call) übertragen. Diese SAP-Übertragung wird auch dann fortgesetzt, wenn der Benutzer GSNW und den SAP-Agent-Dienst deaktiviert.

Der RPC-Dienst führt die SAP-Übertragung durch, wenn die Clientdienste für NetWare (CSNW) und der SAP-Agent-Dienst installiert sind. Diese SAP-Übertragung wird auch dann fortgesetzt, wenn der Benutzer den SAP-Agent deaktiviert.

Standardmäßig überprüft der RPC-Dienst, ob Gatewaydienste für NetWare und der SAP-Agent-Dienst auf dem Computer vorhanden sind, auf dem Windows Server ausgeführt wird. Beim Installieren von Datei- und Druckdiensten für NetWare wird ein SAP-Agent installiert.

Auf dem Computer, auf dem eine Clientversion von Windows mit CSNW ausgeführt wird, überprüft der RPC-Dienst den SAP-Agent-Dienst. Wenn die Dienste vorhanden sind, startet RPC einen eigenen Thread, der jede Minute den SAP-Broadcasttyp 640 übernimmt.

> [!NOTE]
> Wenn SAP-Broadcasts nicht alle 60 Sekunden im Netzwerk übertragen werden sollen, können Sie SAP-Broadcasts mithilfe des Registrierungs-Editors deaktivieren. Sie müssen gewarnt werden, dass die falsche Verwendung des Registrierungs-Editors schwerwiegende Probleme verursachen kann, die möglicherweise eine Neuinstallation des Betriebssystems erfordern. Microsoft übernimmt keinerlei Garantie dafür, dass Probleme aufgrund nicht ordnungsgemäßer Verwendung des Registrierungs-Editors behoben werden können. Sie verwenden den Registrierungs-Editor auf eigene Gefahr. Sie sollten die Registrierung sichern, bevor Sie sie bearbeiten.

 

**So konfigurieren Sie für SAP**

1.  Führen Sie den Registrierungs-Editor (Regedt32.exe) aus, und wechseln Sie in der Registrierung zum folgenden Schlüssel:

    **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ RPC**

2.  Klicken Sie im Menü **Bearbeiten** auf **Wert hinzufügen,** und verwenden Sie den folgenden Eintrag:
    1.  Wertname: AdvertiseRpcService
    2.  Datentyp: REG \_ SZ
    3.  Zeichenfolge: Nein
3.  Wenn Sie "Nein" für die Zeichenfolge verwenden, wird die RPC-SAP-Übertragung deaktiviert. Wenn Sie Ja für die Zeichenfolge verwenden, wird die RPC-SAP-Übertragung aktiviert.
4.  Starten Sie den Computer neu, damit die Registrierungsänderung wirksam wird.
    > [!NOTE]
    > Wenn die SAP-Broadcasts nach dem Ausführen dieser Schritte fortgesetzt werden, sollten Sie einen Problembehandlungsschritt ausprobieren. Löschen Sie den **Ncacn \_ spx-Zeichenfolgenwert** im folgenden Registrierungsschlüssel:
    >
    > **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Rpc \\ ServerProtocols\\**

     

> [!NOTE]  
> Dies sollte nur als Problembehandlungsschritt verwendet werden. Durch das Löschen dieses Zeichenfolgenwerts werden SAP-Broadcasts vollständig deaktiviert, die einige Programme möglicherweise benötigen, um ordnungsgemäß zu funktionieren.