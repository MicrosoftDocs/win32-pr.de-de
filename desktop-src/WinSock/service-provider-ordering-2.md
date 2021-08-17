---
description: Die Reihenfolge, in der Transportdienstanbieter anfänglich installiert werden, bestimmt die Reihenfolge, in der sie über WSCEnumProtocols und WSCEnumProtocols32 in der Dienstanbieterschnittstelle oder über WSAEnumProtocols an der Anwendungsschnittstelle aufgeführt werden. Noch wichtiger ist, dass diese Reihenfolge auch die Reihenfolge bestimmt, in der Protokolle und Dienstanbieter berücksichtigt werden, wenn ein Client die Erstellung eines Sockets basierend auf seiner Adressfamilie, dem Typ und dem Protokollbezeichner anfordert.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Dienstanbieterreihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 445fcc0cadafae8fd61ee2e34a872485b67466037c1dc71e34ab173156c8d9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740581"
---
# <a name="service-provider-ordering"></a>Dienstanbieterreihenfolge

Die Reihenfolge, in der Transportdienstanbieter anfänglich installiert werden, bestimmt die Reihenfolge, in der sie über [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) und [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) in der Dienstanbieterschnittstelle oder über [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) an der Anwendungsschnittstelle aufgeführt werden. Noch wichtiger ist, dass diese Reihenfolge auch die Reihenfolge bestimmt, in der Protokolle und Dienstanbieter berücksichtigt werden, wenn ein Client die Erstellung eines Sockets basierend auf seiner Adressfamilie, dem Typ und dem Protokollbezeichner anfordert.

Windows Sockets 2 enthält ein Applet namens Sporder.exe, mit dem der Katalog der installierten Protokolle interaktiv neu angeordnet werden kann, nachdem protokolle bereits installiert wurden. Winsock enthält auch eine zusätzliche DLL Sporder.dll, die eine prozedurale Schnittstelle zum Neuanordnen von Protokollen exportiert. Diese prozedurale Schnittstelle besteht aus einer einzelnen Prozedur namens [**WSCWriteProviderOrder.**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder)

Die Schnittstellendefinition kann mithilfe der Includedatei Sporder.h in ein C- oder C++-Programm importiert werden. Der Einstiegspunkt kann über die Lib-Datei Sporder.lib verknüpft werden.

 

 



