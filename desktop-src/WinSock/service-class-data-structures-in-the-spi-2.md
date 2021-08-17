---
description: Wenn eine neue Dienstklasse installiert wird, muss eine WSASERVICECLASSINFO-Struktur vorbereitet und bereitgestellt werden. Diese Struktur besteht auch aus Unterstrukturen, die eine Reihe von Parametern enthalten, die für bestimmte Namespaces gelten.
ms.assetid: fb225e0c-a0c7-44e1-80fb-7b924b371afa
title: Datenstrukturen der Dienstklasse in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53eb2fd61c5ec6295b65128048bc9fe477ae63f78f89bfba4be73798002ead88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993565"
---
# <a name="service-class-data-structures-in-the-spi"></a>Datenstrukturen der Dienstklasse in der SPI

Wenn eine neue Dienstklasse installiert wird, muss eine [**WSASERVICECLASSINFO-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) vorbereitet und bereitgestellt werden. Diese Struktur besteht auch aus Unterstrukturen, die eine Reihe von Parametern enthalten, die für bestimmte Namespaces gelten.

![Diagramm: WSASERVICECLASSINFO-Struktur, Unterstrukturen und Parameter, die für bestimmte Namespaces gelten](images/ovrvw3-3.png)

Für jede Dienstklasse gibt es eine einzelne [**WSASERVICECLASSINFO-Struktur.**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) Innerhalb der **WSASERVICECLASSINFO-Struktur** ist der eindeutige Bezeichner der Dienstklasse in **lpServiceClassId** enthalten, und auf eine zugeordnete Anzeigezeichenfolge wird von **lpServiceClassName verwiesen.**

Der **lpClassInfos-Member** in der [**WSASERVICECLASSINFO-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) verweist auf ein Array von [**WSANSCLASSINFO-Strukturen,**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) von denen jedes einen benannten und typierten Parameter liefert, der für einen angegebenen Namespace gilt. Beispiele für Werte für das **lpszName-Member** sind: SAPID, TCPPORT, UDPPORT usw. Diese Zeichenfolgen sind im Allgemeinen spezifisch für den Namespace, der in **dwNameSpace identifiziert wird.** Typische Werte für **dwValueType** können REG \_ DWORD, REG \_ SZ usw. sein. Das **dwValueSize-Element** gibt die Länge des Datenelements an, auf das **lpValue zeigt.**

Die gesamte Auflistung von Daten, die in einer [**WSASERVICECLASSINFO-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) dargestellt werden, wird jedem Namespaceanbieter über [**NSPInstallServiceClass bereitgestellt.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) Jeder einzelne Namespaceanbieter durchsieft dann die Liste der [**WSANSCLASSINFO-Strukturen**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) und behält die entsprechenden Informationen bei. Diese Architektur sieht auch das zukünftige Vorhandensein eines speziellen Namespaceanbieters vor, der alle Schemainformationen der Dienstklasse für alle Namespaces beibehalten würde. Die Ws2-32.dll würde diesen Anbieter abfragen, um die WSASERVICECLASSINFO-Daten zu erhalten, die für namespace-Anbieter erforderlich sind, wenn \_ [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) aufgerufen wird, um eine Abfrage zu initiieren, und wenn [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice) aufgerufen wird, um einen Dienst zu registrieren.  Der Namespaceanbieter sollte sich vorerst nicht auf diese Funktion verlassen und stattdessen über eine anbieterspezifische Möglichkeit verfügen, alle erforderlichen Informationen zum Dienstklassenschema zu erhalten. Wenn kein Anbieter verfügbar ist, der alle Dienstklassenschemas für alle Namespaces speichert, verwendet die \_ Ws2-32.dll [**NSPGetServiceClassInfo,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) um solche Informationen von jedem einzelnen Namespaceanbieter zu erhalten.

 

 



