---
description: Namensauflösung und Registrierungs Modell für den Windows Sockets (Winsock) SPI.
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: Namens Auflösungs Modell für den SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e79593f56cd11671b3c16ef9098d455bf548505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129149"
---
# <a name="name-resolution-model-for-the-spi"></a>Namens Auflösungs Modell für den SPI

Beim Entwickeln einer Protokoll unabhängigen Client/Server-Anwendung gibt es zwei grundlegende Anforderungen in Bezug auf die Namensauflösung und Registrierung:

-   Die Möglichkeit der Server Hälfte der Anwendung (im folgenden als Dienst bezeichnet), das vorhanden sein in einem oder mehreren Namespaces zu registrieren (oder für Sie zugänglich).
-   Die Fähigkeit der Client Anwendung, den Dienst innerhalb eines Namespace zu finden und das erforderliche Transportprotokoll und die Adressierungs Informationen abzurufen.

Für diejenigen, die an die Entwicklung von TCP/IP-basierten Anwendungen gewöhnt sind, kann dies möglicherweise kaum mehr als die Suche nach einer Host Adresse und dann die Verwendung einer vereinbarten Portnummer bedeuten. Andere Netzwerk Schemas ermöglichen jedoch den Speicherort des Dienstanbieter, das Protokoll, das für den Dienst verwendet wird, und andere Attribute, die zur Laufzeit ermittelt werden. Um den Umfang der in vorhandenen namens Diensten gefundenen Funktionen zu unterstützen, übernimmt die Windows Sockets 2-Schnittstelle das unten beschriebene Modell.

Ein *Namespace* bezieht sich auf eine Funktion, mit der (minimal) das Protokoll und die Adressierungs Attribute eines Netzwerk Dienstanbieter mit einem oder mehreren benutzerfreundlichen Namen verknüpft werden können. Derzeit werden viele Namespaces verwendet, einschließlich der Domain Name System des Internets (DNS), NetWare-Verzeichnisdienste (NDS), X. 500 usw. Diese Namespaces unterscheiden sich stark von der Organisation und Implementierung. Einige der Eigenschaften sind besonders wichtig, um aus der Perspektive der Windows Sockets-Namensauflösung zu verstehen.

 

 



