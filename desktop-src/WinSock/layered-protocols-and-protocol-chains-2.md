---
description: 'Windows Sockets 2 umfasst das Konzept eines mehrstufigen Protokolls: ein Protokoll, das nur Kommunikationsfunktionen auf höherer Ebene implementiert, während ein zugrunde liegender Transportstapel für den tatsächlichen Datenaustausch mit einem Remoteendpunkt verwendet wird.'
ms.assetid: 80e0b229-ebdc-4ac1-8e8e-9e5b7cfc3ab5
title: Mehrstufige Protokolle und Protokollketten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e60943bac5545fd7bb2bc87709d08c59d3addab205d14cab80687596721b973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858450"
---
# <a name="layered-protocols-and-protocol-chains"></a>Mehrstufige Protokolle und Protokollketten

Windows Sockets 2 umfasst das Konzept eines mehrstufigen Protokolls: ein Protokoll, das nur Kommunikationsfunktionen auf höherer Ebene implementiert, während ein zugrunde liegender Transportstapel für den tatsächlichen Datenaustausch mit einem Remoteendpunkt verwendet wird. Ein Beispiel für diese Art von mehrstufigem Protokoll ist eine Sicherheitsschicht, die dem Socketverbindungsprozess ein Protokoll hinzufügt, um eine Authentifizierung durchzuführen und ein Verschlüsselungsschema einzurichten. Ein solches Sicherheitsprotokoll erfordert im Allgemeinen die Dienste eines zugrunde liegenden und zuverlässigen Transportprotokolls wie TCP oder SPX.

Der Begriff *Basisprotokoll* bezieht sich auf ein Protokoll wie TCP oder SPX, das die Datenkommunikation mit einem Remoteendpunkt vollständig ausführen kann. Ein *mehrstufiges Protokoll* ist ein Protokoll, das nicht eigenständig sein kann, während es sich bei einer *Protokollkette* um ein oder mehrere mehrstufige Protokolle handelt, die durch ein Basisprotokoll zusammengeführt und verankert werden.

Sie können eine Protokollkette erstellen, wenn Sie die mehrstufigen Protokolle so entwerfen, dass sie die Windows Sockets 2 SPI am oberen und unteren Rand unterstützen. Eine spezielle [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) bezieht sich auf die Protokollkette als Ganzes und beschreibt die explizite Reihenfolge, in der die mehrstufigen Protokolle verknüpft werden. Dies wird in der folgenden Abbildung veranschaulicht. Da nur Basisprotokolle und Protokollketten direkt von Anwendungen verwendet werden können, sind sie die einzigen, die aufgeführt werden, wenn die installierten Protokolle mit der [**WSAEnumProtocols-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) aufgelistet werden.

![Mehrschichtige Protokollarchitektur](images/ovrvw2-3.png)

 

 
