---
description: Die Reihenfolge, in der Transport Dienstanbieter anfänglich installiert werden, steuert die Reihenfolge, in der Sie über wscenumprotokolls und WSCEnumProtocols32 an der Dienstanbieter Schnittstelle oder über wsaenumprotokolls auf der Anwendungs Schnittstelle aufgelistet werden. Noch wichtiger ist, dass diese Reihenfolge auch die Reihenfolge bestimmt, in der Protokolle und Dienstanbieter berücksichtigt werden, wenn ein Client die Erstellung eines Sockets basierend auf der Adressfamilie, dem Typ und der Protokoll Kennung anfordert.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Dienstanbieter-Reihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c23d9357d30c94b084bf6288013c38a2d46a4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863811"
---
# <a name="service-provider-ordering"></a>Dienstanbieter-Reihenfolge

Die Reihenfolge, in der Transport Dienstanbieter anfänglich installiert werden, steuert die Reihenfolge, in der Sie über [**wscenumprotokolls**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) und [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) an der Dienstanbieter Schnittstelle oder über [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) auf der Anwendungs Schnittstelle aufgelistet werden. Noch wichtiger ist, dass diese Reihenfolge auch die Reihenfolge bestimmt, in der Protokolle und Dienstanbieter berücksichtigt werden, wenn ein Client die Erstellung eines Sockets basierend auf der Adressfamilie, dem Typ und der Protokoll Kennung anfordert.

Windows Sockets 2 enthält ein Applet namens Sporder.exe, mit dem der Katalog installierter Protokolle interaktiv neu angeordnet werden kann, nachdem Protokolle bereits installiert wurden. Winsock umfasst auch eine zusätzliche dll, Sporder.dll, die eine prozedurale Schnittstelle zum Neuanordnen von Protokollen exportiert. Diese prozedurale Schnittstelle besteht aus einer einzelnen Prozedur namens [**wscschreiteproviderorder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).

Die Schnittstellen Definition kann mithilfe der Includedatei sporder. h in ein C-oder C++-Programm importiert werden. Der Einstiegspunkt kann mithilfe der LIB-Datei sporder. lib verknüpft werden.

 

 



