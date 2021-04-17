---
description: Wenn eine neue Dienstklasse installiert wird, muss eine wsaserviceclassinfo-Struktur vorbereitet und bereitgestellt werden. Diese Struktur besteht auch aus Unterstrukturen, die eine Reihe von Parametern enthalten, die für bestimmte Namespaces gelten.
ms.assetid: fb225e0c-a0c7-44e1-80fb-7b924b371afa
title: Dienst Klassen-Datenstrukturen in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bf249c7437751e7c6d08b2fdf3830e92921ce7
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104566179"
---
# <a name="service-class-data-structures-in-the-spi"></a>Dienst Klassen-Datenstrukturen in der SPI

Wenn eine neue Dienstklasse installiert wird, muss eine [**wsaserviceclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) -Struktur vorbereitet und bereitgestellt werden. Diese Struktur besteht auch aus Unterstrukturen, die eine Reihe von Parametern enthalten, die für bestimmte Namespaces gelten.

![Das Diagramm zeigt die wsaserviceclassinfo-Struktur, die Unterstrukturen und die Parameter, die für bestimmte Namespaces gelten.](images/ovrvw3-3.png)

Für jede Dienstklasse gibt es eine einzelne [**wsaserviceclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) -Struktur. Innerhalb der **wsaserviceclassinfo** -Struktur ist der eindeutige Bezeichner der Dienstklasse in **lpserviceclassid** enthalten, und auf eine zugeordnete Anzeige Zeichenfolge wird von **lpserviceclassname** verwiesen.

Der **lpclassinfos** -Member in der [**wsaserviceclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) -Struktur verweist auf ein Array von [**wsansclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) -Strukturen, von denen jedes einen benannten und typisierten Parameter bereitstellt, der für einen angegebenen Namespace gilt. Beispiele für Werte für den Member **lpszname** : SAPID, TcpPort, UDPPort usw. Diese Zeichen folgen sind in der Regel spezifisch für den Namespace, der in **dwnamespace** identifiziert wird. Typische Werte für " **dwvaluetype** " sind "reg \_ DWORD", "reg \_ SZ" usw. Der **dwvaluesize** -Member gibt die Länge des Datenelements an, auf das von **lpValue** verwiesen wird.

Die gesamte Sammlung von Daten, die in einer [**wsaserviceclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) -Struktur dargestellt wird, wird für jeden Namespace Anbieter über [**nspinstallserviceclass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)bereitgestellt. Jeder einzelne Namespace Anbieter durchläuft dann die Liste der [**wsansclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) -Strukturen und behält die für ihn anwendbaren Informationen bei. Diese Architektur stellt auch das zukünftige vorhanden sein eines speziellen Namespace Anbieters vor, der alle Dienst Klassen Schema-Informationen für alle Namespaces beibehält. Der Ws2- \_32.dll würde diesen Anbieter Abfragen, um die **wsaserviceclassinfo** -Daten abzurufen, die für Namespace Anbieter bereitgestellt werden müssen, wenn [**nsplookupservicebegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) aufgerufen wird, um eine Abfrage zu initiieren, und wenn [**nspsetservice**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice) aufgerufen wird, um einen Dienst zu registrieren. Der Namespace Anbieter sollte sich nicht für die Zeit auf diese Funktion verlassen und sollte stattdessen über ein Anbieter spezifisches Mittel verfügen, um alle benötigten Dienst Klassen Schema-Informationen zu erhalten. Wenn kein Anbieter vorhanden ist, der alle Dienst Klassen Schemas für alle Namespaces speichert, verwendet der Ws2- \_32.dll [**nspgetserviceclassinfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) , um solche Informationen von den einzelnen Namespace Anbietern abzurufen.

 

 



