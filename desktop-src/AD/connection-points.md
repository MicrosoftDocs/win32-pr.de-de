---
title: Verbindungspunkte
description: Ein Verbindungspunkt Objekt enthält Daten zu einer oder mehreren Instanzen eines Dienstanbieter, der im Netzwerk verfügbar ist.
ms.assetid: eb810e6d-c220-4a24-ae12-b12ace237413
ms.tgt_platform: multiple
keywords:
- Verbindungspunkte (AD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc61c4c5b7dd74626ab1f3884ad403cfa20b843
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038791"
---
# <a name="connection-points"></a>Verbindungspunkte

Ein Verbindungspunkt Objekt enthält Daten zu einer oder mehreren Instanzen eines Dienstanbieter, der im Netzwerk verfügbar ist. Die [**ConnectionPoint**](/windows/desktop/ADSchema/c-connectionpoint) -Objektklasse ist die abstrakte Basisklasse, von der Objekte abgeleitet werden, die Verbindungs fähige Ressourcen in Active Directory Domain Services darstellen. Die folgende Abbildung zeigt einige der Objektklassen, die von der **ConnectionPoint** -Objektklasse abgeleitet werden.

![Objektklassen, die von der ConnectionPoint-Objektklasse abgeleitet werden](images/connection-points.png)

In der folgenden Tabelle sind die unmittelbaren Unterklassen der [**ConnectionPoint**](/windows/desktop/ADSchema/c-connectionpoint) -Klasse aufgeführt.



| Objektklasse                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**serviceConnectionPoint**](/windows/desktop/ADSchema/c-serviceconnectionpoint) | Dienst Verbindungspunkt-Objekte (Service Connection Point, SCP) zum Veröffentlichen von Daten, die Client Anwendungen zum Binden an einen Dienst verwenden. Weitere Informationen finden Sie unter [Veröffentlichen mit Dienst Verbindungs Punkten (SCPs)](publishing-with-service-connection-points.md).                                                                               |
| [**rpcentry**](/windows/desktop/ADSchema/c-rpcentry)                             | Eine abstrakte Klasse, deren Unterklassen vom RPC-Namen Dienst (RPC Name Service, NS) verwendet werden, auf den die **RpcNs \*** -Funktionen in der Win32-API zugreifen. Weitere Informationen finden Sie unter [Veröffentlichen mit dem RPC-Namensdienst (RPC Name Service, RpcNs)](publishing-with-the-rpc-name-service-rpcns.md).                                                          |
| [**serviceInstance**](/windows/desktop/ADSchema/c-serviceinstance)               | Das Verbindungspunkt Objekt, das vom Windows Sockets Registration and Resolution (RNR)-Namensdienst verwendet wird und auf das über die **WSA \*** -APIs von Windows Sockets zugegriffen wird. Weitere Informationen finden Sie unter [Veröffentlichen mit Windows Sockets Registration and Resolution (RNR)](publishing-with-windows-sockets-registration-and-resolution.md). |
| [**Print Queue**](/windows/desktop/ADSchema/c-printqueue)                         | Zum Veröffentlichen von Netzwerkdruckern verwendetes Verbindungspunkt Objekt. Weitere Informationen finden Sie unter [**iadsprintqueue**](/windows/desktop/api/iads/nn-iads-iadsprintqueue).                                                                                                                                                                                           |
| [**Handels**](/windows/desktop/ADSchema/c-volume)                                 | Verbindungspunkt Objekt, das zum Veröffentlichen von Datei Diensten verwendet wird.                                                                                                                                                                                                                                                                   |



 

Beachten Sie, dass COM-basierte Dienste keine Verbindungspunkt Objekte verwenden, um sich selbst ankündigen zu können. Diese Dienste werden im-Klassen Speicher veröffentlicht. Der Windows 2000-Klassen Speicher ist ein Verzeichnis basiertes Repository für alle COM-basierten Anwendungen, Schnittstellen und APIs, die zum Veröffentlichen und Zuweisen von Anwendungen bereitstellen. Weitere Informationen finden Sie unter [Veröffentlichen von COM+-Diensten](publishing-com-services.md).

 

 