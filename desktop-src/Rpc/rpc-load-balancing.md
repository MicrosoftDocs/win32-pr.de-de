---
title: RPC-Lastenausgleich
description: RPC-Lastenausgleich
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4039742fcfcc67280c610270908bed51034f691a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036405"
---
# <a name="rpc-load-balancing"></a>RPC-Lastenausgleich

Der Microsoft RPC-Lastenausgleich soll eine skalierbare Lösung für Szenarien bereitstellen, die eine hohe Auslastung von [RPC-über-HTTP](remote-procedure-calls-using-rpc-over-http.md) -Datenverkehr erfordern. Der primäre Zweck des RPC-Load Balancer besteht darin sicherzustellen, dass der RPC-/HTTP-Datenverkehr von einer Serverfarm gewartet werden kann, um die Skalierbarkeit Um dies zu erreichen, muss RPC sicherstellen, dass alle Verbindungen von einem Client Prozess durch denselben Server Endpunkt in der Serverfarm gewartet werden. Der RPC-Load Balancer wird als Dienst implementiert, der in Verbindung mit dem RPC-über-HTTP-Proxy Dienst ausgeführt wird.

Um den Lastenausgleich zu ermöglichen, kommuniziert der RPC-Lasten Ausgleichs Dienst, der auf den einzelnen Servern ausgeführt wird, miteinander, um den bevorzugten Server für die anfängliche Client Verbindung zu ermitteln. Dieser Vorgang wird als "Schiedsgerichtsbarkeit" bezeichnet und erfolgt zum Zeitpunkt der anfänglichen Client Verbindung. Um den Server übergreifenden Datenverkehr zu reduzieren, wählt der RPC-Lasten Ausgleichs Dienst den lokalen Endpunkt aus, um die Verbindung zu bedienen, wenn der Client nicht bereits einem Server zugeordnet ist. Bei einer bestimmten Client Verbindung besteht das Ergebnis einer-Vermittlung aus zwei Möglichkeiten:

-   Wenn der Client bereits eine Verbindung hergestellt hat, verarbeitet der Server, auf dem die Verbindung zum ersten Mal empfangen wird, die nachfolgenden Verbindungen.
-   Wenn es sich um die erste Verbindung vom Client handelt, führt die-Vermittlung dazu, dass der lokale Server die Verbindung und somit alle Verbindungen vom Client verarbeitet. Diese Informationen werden nach der Festlegung an die anderen RPC-Load Balancer Dienste in der Serverfarm committet, sodass Sie von dem Server informiert werden, der alle Anforderungen des Clients verarbeitet.

Dieser Abschnitt bietet eine Übersicht über den RPC-Lastenausgleich in den folgenden Themen:

-   [Bereitstellen des Lasten Ausgleichs](deploying-load-balancing.md)
-   [Konfigurieren des Lasten Ausgleichs](configuring-load-balancing.md)
-   [Bewährte Methoden für den Lastenausgleich](load-balancing-best-practices.md)

## <a name="requirements"></a>Anforderungen

Der RPC-Lasten Ausgleichs Dienst wird auf Servern unterstützt, auf denen Windows Server 2008 R2 oder höher ausgeführt wird, sowie auf Clients, auf denen Windows 7 oder höher ausgeführt wird.

Der RPC-Proxy Dienst, der RPC-Lasten Ausgleichs Dienst und die Server Endpunkte müssen alle auf dem gleichen Computer ausgeführt werden. Außerdem müssen alle Server in der Serverfarm in der Lage sein, den angeforderten Endpunkt zu verarbeiten. Informationen zum Konfigurieren des RPC-Proxy diensdienstanbieter und des RPC-Lasten Ausgleichs Dienstanbieter finden Sie unter [Konfigurieren von Computern für RPC über HTTP](configuring-computers-for-rpc-over-http.md) und [Konfigurieren des Lasten Ausgleichs](configuring-load-balancing.md).

## <a name="limitations"></a>Einschränkungen

Zu diesem Zeitpunkt unterstützt der RPC-Lastenausgleich nur eine Serverfarm pro Ressource. Alle Server in allen Serverfarmen müssen auch in der Lage sein, alle Ressourcen zu verarbeiten.

 

 




