---
title: Verbindungspunkte
description: Ein Verbindungspunktobjekt enthält Daten zu einer oder mehreren Instanzen eines Diensts, die im Netzwerk verfügbar sind.
ms.assetid: eb810e6d-c220-4a24-ae12-b12ace237413
ms.tgt_platform: multiple
keywords:
- Verbindungspunkte AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a0b7a4c8ddbf592bba0ed39e2eb8f93faf863e6ebff7081865466b6522c98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022045"
---
# <a name="connection-points"></a>Verbindungspunkte

Ein Verbindungspunktobjekt enthält Daten zu einer oder mehreren Instanzen eines Diensts, die im Netzwerk verfügbar sind. Die [**connectionPoint-Objektklasse**](/windows/desktop/ADSchema/c-connectionpoint) ist die abstrakte Basisklasse, von der Objekte abgeleitet werden, die verbindende Ressourcen in Active Directory Domain Services darstellen. Die folgende Abbildung zeigt einige der Von der **connectionPoint-Objektklasse** abgeleiteten Objektklassen.

![Von der Verbindungspunktobjektklasse abgeleitete Objektklassen](images/connection-points.png)

In der folgenden Tabelle sind die unmittelbaren Unterklassen der [**connectionPoint-Klasse**](/windows/desktop/ADSchema/c-connectionpoint) aufgeführt.



| Objektklasse                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) | SCP-Objekte (Service Connection Point) zum Veröffentlichen von Daten, die Clientanwendungen zum Binden an einen Dienst verwenden. Weitere Informationen finden Sie unter [Veröffentlichen mit Dienstverbindungspunkten (SCPs).](publishing-with-service-connection-points.md)                                                                               |
| [**rpcEntry**](/windows/desktop/ADSchema/c-rpcentry)                             | Eine abstrakte Klasse, deren Unterklassen vom RPC-Namensdienst (RPC Name Service, Ns) verwendet werden, auf den über die **RpcNs-Funktionen \*** in der Win32-API zugegriffen wird. Weitere Informationen finden Sie unter [Veröffentlichen mit dem RPC-Namensdienst (RPCNs).](publishing-with-the-rpc-name-service-rpcns.md)                                                          |
| [**serviceInstance**](/windows/desktop/ADSchema/c-serviceinstance)               | Verbindungspunktobjekt, das vom Namensdienst Windows Sockets Registration and Resolution (RnR) verwendet wird, auf den über die **WSA-APIs \*** für Windows Sockets zugegriffen wird. Weitere Informationen finden Sie unter [Veröffentlichen mit Windows Sockets Registration and Resolution (RnR)](publishing-with-windows-sockets-registration-and-resolution.md). |
| [**Printqueue**](/windows/desktop/ADSchema/c-printqueue)                         | Verbindungspunktobjekt zum Veröffentlichen von Netzwerkdruckern. Weitere Informationen finden Sie unter [**IADsPrintQueue**](/windows/desktop/api/iads/nn-iads-iadsprintqueue).                                                                                                                                                                                           |
| [**Volumen**](/windows/desktop/ADSchema/c-volume)                                 | Verbindungspunktobjekt, das zum Veröffentlichen von Dateidiensten verwendet wird.                                                                                                                                                                                                                                                                   |



 

Beachten Sie, dass COM-basierte Dienste keine Verbindungspunktobjekte verwenden, um sich selbst anzukündigen. Diese Dienste werden im Klassenspeicher veröffentlicht. Der Windows 2000-Klassenspeicher ist ein verzeichnisbasiertes Repository für alle COM-basierten Anwendungen, Schnittstellen und APIs, die die Veröffentlichung und Zuweisung von Anwendungen ermöglichen. Weitere Informationen finden Sie unter [Veröffentlichen von COM+-Diensten.](publishing-com-services.md)

 

 