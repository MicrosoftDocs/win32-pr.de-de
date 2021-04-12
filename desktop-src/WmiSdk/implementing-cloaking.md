---
description: Das Cloaking ist eine Erweiterung des Identitäts Wechsels, die eine bessere Kontrolle über die Identität eines Clients über einen Proxy durch com ermöglicht. Wie viele Arten von WMI-Sicherheit legen Sie den Cloaking über die CoSetProxyBlanket-und die CoInitializeSecurity-Schnittstelle fest.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Implementieren von Cloaking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac73d7aacf32a2168dc3651b82ae1ce3a977cf5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217125"
---
# <a name="implementing-cloaking"></a>Implementieren von Cloaking

Das Cloaking ist eine Erweiterung des Identitäts Wechsels, die eine bessere Kontrolle über die Identität eines Clients über einen Proxy durch com ermöglicht. Wie viele Arten von WMI-Sicherheit legen Sie den Cloaking über die [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) -und die [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) -Schnittstelle fest.

COM bietet die folgenden Arten von Verstopfungen:

-   statischen

    COM legt die Tokenidentität durch den Thread oder das Prozess Token beim ersten Proxy des Proxys fest. Wenn Sie statisches Cloaking mit [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)verwenden, legen Sie die Identität des Proxys für die Lebensdauer des Proxys fest.

-   Dynamisch

    COM stellt die Tokenidentität aus dem Thread-oder Prozess Token bei jedem Proxy Vorgang wieder her. Da com die Identität bei jedem-Rückruf überprüft, ermöglicht dynamisches Cloaking eine präzisere Steuerung der Client Identität. Das dynamische Cloaking ist jedoch weniger effizient als das statische Cloaking.

Wenn Sie das Cloaking in Verbindung mit der Delegierungs Ebene des Identitäts Wechsels festgelegt haben, kann ein Server die Identität eines Clients über mehrere Server hinweg weitergeben, auch wenn es sich um Remote Server handelt. Wenn Sie das Cloaking nicht aktivieren, führt com einen beliebigen Rückruf von einem lokalen Server an einen Remote Server im Kontext des eigentlichen Server Prozesses aus.

Durch das Cloaking kann WMI die Identität eines Clients annehmen, um sowohl auf lokale als auch auf Remote Netzwerkressourcen über mehrere Computer Grenzen zuzugreifen. WMI kann die Identität des Clients an lokale Server und Remote Server übergeben, z. b. an andere Remote Instanzen von WMI. Diese Remote Server können dann Vorgänge im ursprünglichen Client Kontext ausführen.

Im folgenden Verfahren wird beschrieben, wie Sie die Verwendung von Cloaking und Delegierungen kombinieren.

**So verwenden Sie das Cloaking und die Delegierung**

1.  Legen Sie den Authentifizierungsdienst auf Kerberos fest.

    Kerberos ist der einzige Authentifizierungsdienst, der Remote Lecks und Delegierungen unterstützt. Dies bedeutet, dass die über-und Delegierung nur auf Remote Servern verwendet werden kann.

2.  Markieren Sie das Server Anmelde Konto in den Active Directory Services als "Trusted for Delegation".
3.  Markieren Sie das Client Anmelde Konto in Active Directory Services als "Konto ist vertraulich und kann nicht delegiert werden".

Beispielsweise kann ein Ansichts Anbieter, der Objekte aus mehreren WMI-Instanzen auf mehreren Computern zurückgeben kann, von Delegierung und Cloaking profitieren.

 

 
