---
description: Es gibt viele Möglichkeiten, die Verteilung empfangener SOAP-Nachrichten an den entsprechenden Dienst zu verarbeiten. Die beiden einfachsten Mechanismen sind Dispatch auf Transport Ebene und Adress-und Aktions Verteilung.
ms.assetid: 988dc505-5d1f-46df-9340-107483bb9581
title: Verteilen von SOAP-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a60e896557a64b840ec890ddc5c5d2e2cf8295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529381"
---
# <a name="dispatching-soap-messages"></a>Verteilen von SOAP-Nachrichten

Es gibt viele Möglichkeiten, die Verteilung empfangener SOAP-Nachrichten an den entsprechenden Dienst zu verarbeiten. Die beiden einfachsten Mechanismen sind Dispatch auf Transport Ebene und Adress-und Aktions Verteilung.

## <a name="transport-level-dispatch"></a>Dispatch auf Transport Ebene

Bei Transport Level Dispatch wird der zugrunde liegende http-Server (z. b. die [http-API](/windows/desktop/Http/http-api-start-page)) zum Verwalten des Routings von Anforderungen an das Gerät und seine Dienste verwendet. Der Server stellt eine andere URL für jeden Dienst und für das Gerät bereit, und für jede URL werden unterschiedliche senken registriert. Dadurch kann Code so entworfen werden, dass jeder Dienst vom anderen isoliert ist, entweder als separate Komponenten innerhalb desselben Prozesses ausgeführt oder als separate Prozesse ausgeführt werden.

Das Verteilen von Transport Ebenen hat einige Vorteile. Nachrichten können an die entsprechende Komponente gesendet werden, ohne zuerst den SOAP-Umschlag oder den Nachrichtentext zu übernehmen. Außerdem kann der vorhandene Mechanismus zum Weiterleiten von Nachrichten, die von den meisten HTTP-Server Implementierungen bereitgestellt werden, wieder verwendet werden Außerdem wird der SOAP-Verarbeitungs Code zwischen Diensten isoliert, was ein Maß an Sicherheit bietet, da sichere Dienste vermeiden, dass Nachrichten durchgängigen Code übertragen werden.

## <a name="address-and-action-dispatch"></a>Adressierung von Adressen und Aktionen

Address und Action Dispatch sind abhängig von den SOAP-Headern, um den entsprechenden Dienst zu ermitteln, an den die Nachricht gesendet wird. Dieses Modell kann auch zusätzliche Informationen, wie z. b. Verweis Parameter, verwenden, um die Weiterleitung zu unterstützen.

Dieses Modell fördert die Wiederverwendung von Code in einem geschichteten Messaging Stapel, da der gesamte Code bis zum SOAP-Prozessor von allen Diensten gemeinsam genutzt wird. Außerdem sind keine unterschiedlichen Transport Adressen für Dienste erforderlich. Dies bedeutet, dass uuid-Adressen für Dienst Endpunkte verwendet werden können. Die Adress-und Aktions Verteilung wird auch direkt in ein Programmiermodell übersetzt. Entwickler können Dienste und Geräte in eine einzelne Komponente einbinden, die das Routing verwaltet, anstatt eine Verknüpfung mit einer HTTP-Schicht herzustellen oder separate Komponenten für jeden Dienst zu erstellen.

 

 
