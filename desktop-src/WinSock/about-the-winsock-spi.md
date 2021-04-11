---
description: Winsock stellt eine Dienstanbieter Schnittstelle zum Erstellen von Winsock-Diensten bereit, die häufig als Winsock SPI bezeichnet werden.
ms.assetid: e3d21dd8-2b58-4108-857d-a075b8be68b0
title: Informationen über die Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe70d5d381505085e2794a57a1183e8bec505917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129232"
---
# <a name="about-the-winsock-spi"></a>Informationen über die Winsock SPI

Winsock stellt eine Dienstanbieter Schnittstelle zum Erstellen von Winsock-Diensten bereit, die häufig als Winsock SPI bezeichnet werden. Es gibt zwei Typen von Dienstanbietern: Transportanbieter und Namespace Anbieter. Beispiele für Transportanbieter sind Protokollstapel wie z. b. TCP/IP oder IPX/SPX. ein Beispiel für einen Namespace Anbieter wäre eine Schnittstelle zum DNS (Domain Naming System) des Internets. Separate Abschnitte der Dienstanbieter Schnittstellen Spezifikation gelten für jeden Dienst Anbietertyp.

[Transport](transport-service-providers-2.md) -und [Namespace](name-space-service-providers-2.md) -Dienstanbieter müssen bei der Ws2- \_32.dll zum Zeitpunkt der Installation registriert werden. Diese Registrierung muss nur einmal für jeden Anbieter durchgeführt werden, da die erforderlichen Informationen im persistenten Speicher aufbewahrt werden.

 

 



