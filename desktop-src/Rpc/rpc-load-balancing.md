---
title: RPC-Lastenausgleich
description: RPC-Lastenausgleich
ms.assetid: c646f748-d5f2-422d-8305-1f86c0dc61b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7fbace237f6d86ebadf3fadc5f3b376d94799b137153b114bc07fead3d64b09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101650"
---
# <a name="rpc-load-balancing"></a>RPC-Lastenausgleich

Der Microsoft RPC-Lastenausgleich soll eine skalierbare Lösung für Szenarien bereitstellen, die eine hohe Last von RPC über [HTTP-Datenverkehr](remote-procedure-calls-using-rpc-over-http.md) erfordern. Der Hauptzweck Load Balancer RPC-Diensts besteht in der Sicherstellung, dass RPC/HTTP-Datenverkehr von einer Serverfarm zur Verbesserung der Skalierbarkeit genutzt werden kann. Um dies zu erreichen, muss RPC sicherstellen, dass alle Verbindungen von einem Clientprozess vom gleichen Serverendpunkt in der Serverfarm hergestellt werden. Die RPC Load Balancer wird als Dienst implementiert, der in Verbindung mit dem RPC-über-HTTP-Proxydienst ausgeführt wird.

Um den Lastenausgleich zu aktivieren, kommuniziert der RPC-Lastenausgleichsdienst, der auf jedem der Server ausgeführt wird, miteinander, um den bevorzugten Server für die anfängliche Clientverbindung zu bestimmen. Dieser Prozess wird als Vermittlung bezeichnet und erfolgt zum Zeitpunkt der ersten Clientverbindung. Um den serverübergreifenden Datenverkehr zu reduzieren, wählt der RPC-Lastenausgleichsdienst den lokalen Endpunkt für die Verbindung aus, wenn der Client noch nicht einem Server zugeordnet ist. Für eine bestimmte Clientverbindung ist das Ergebnis der Vermittlung eine von zwei Möglichkeiten:

-   Wenn der Client bereits eine Verbindung hergestellt hat, verarbeitet der Server, der zuerst die Verbindung empfangen soll, die nachfolgenden Verbindungen.
-   Wenn dies die erste Verbindung vom Client ist, führt die Vermittlung dazu, dass der lokale Server die Verbindung und somit alle Verbindungen vom Client abfing. Diese Informationen werden, sobald sie bestimmt wurden, an die anderen RPC Load Balancer-Dienste in der Serverfarm übertragen, wodurch sie über den Server informiert werden, der alle Anforderungen des Clients abspricht.

Dieser Abschnitt enthält eine Übersicht über den RPC-Lastenausgleich in den folgenden Themen:

-   [Bereitstellen des Lastenausgleichs](deploying-load-balancing.md)
-   [Konfigurieren des Lastenausgleichs](configuring-load-balancing.md)
-   [Bewährte Methoden für den Lastenausgleich](load-balancing-best-practices.md)

## <a name="requirements"></a>Anforderungen

Der RPC-Lastenausgleichsdienst wird auf Servern unterstützt, auf denen Windows Server 2008 R2 oder höher ausgeführt wird, sowie auf Clients, die Windows 7 oder höher von Windows.

Der RPC-Proxydienst, der RPC-Lastenausgleichsdienst und die Serverendpunkte müssen alle auf demselben Computer ausgeführt werden. Darüber hinaus müssen alle Server in der Serverfarm in der Lage sein, den angeforderten Endpunkt zu bedienen. Informationen zum Konfigurieren des RPC-Proxydiensts und des RPC-Lastenausgleichsdiensts finden Sie unter Konfigurieren von Computern für [RPC über HTTP](configuring-computers-for-rpc-over-http.md) bzw. Konfigurieren des [Lastenausgleichs.](configuring-load-balancing.md)

## <a name="limitations"></a>Einschränkungen

Derzeit unterstützt der RPC-Lastenausgleich nur eine Serverfarm pro Ressource. Alle Server in allen Serverfarmen müssen auch in der Lage sein, alle Ressourcen zu bedienen.

 

 




