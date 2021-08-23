---
description: Die Multicast-COM-Schnittstellen ermöglichen den Zugriff auf die Netzwerkeinrichtung zum Zuordnen, Erneuern und Freigeben von Leases für Multicastadressen.
ms.assetid: d4da9616-bdb4-4919-96aa-9e45582b05dd
title: Multicast-COM-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c87c231f18904e3b0287095f511cf3c82bfd263e23a9e69dd50c02eb491616d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575540"
---
# <a name="multicast-com-interfaces"></a>Multicast-COM-Schnittstellen

\[Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die Multicast-COM-Schnittstellen ermöglichen den Zugriff auf die Einrichtung des Netzwerks zum Zuordnen, Erneuern und Freigeben von Leases für Multicastadressen. Sie kapseln eine Reihe von Funktions- und Datenstrukturdefinitionen. Die COM-Schnittstellen entlasten den Programmierer von der Last, diese Datenstrukturen zu verstehen und zu bearbeiten. Da TAPI 3 selbst COM-basiert ist, ermöglichen diese Schnittstellen den Zugriff auf die Multicastadressenzuordnung auf eine Weise, die mit den anderen von TAPI 3 bereitgestellten Einrichtungen konsistent ist. Anwendungen, die mit Visual Basic, Java oder Skriptsprachen geschrieben wurden und normalerweise nicht direkt auf die Windows-API zugreifen können, können diese Schnittstellen verwenden.

Die Multicastadressenzuordnung ist derzeit Thema einer IETF-Arbeitsgruppe. Um auf aktuelle Informationen zu zugreifen, fragen Sie mithilfe einer beliebigen Internetsuch-Engine nach "MDHCP" oder "MADCAP" und "Internetentwurf" ab. Zusätzlich zu MADCAP enthält die vorgeschlagene Architektur ein Protokoll für die Server-zu-Server-Koordination innerhalb einer Domäne oder AS sowie ein Protokoll für die Domänenkoordinierung. Während sich diese Architektur gerade weiterentwickelt, muss sich der Client nicht um die Details dieses Schemas sorgen.

Diese Komponente unterstützt derzeit nur IP-Adressen der Version 4.

> [!Note]  
> Das für diese Schnittstellen verwendete Protokoll heißt derzeit "MADCAP". In früheren Versionen wurde dies als MDHCP bezeichnet.

 

Das Multicastobjekt wird durch Aufrufen von **CoCreateInstance** auf der [**IMcastAddressAllocation-Schnittstelle**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation) erstellt. Die **IMcastAddressAllocation-Schnittstelle** macht die [**EnumerateScopes-Methode**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes) verfügbar, die es einer Anwendung ermöglicht, eine Liste aller verfügbaren Multicast-Bereiche zu erhalten.

Nachdem ein Arbeitsbereich erhalten wurde, wird die [**RequestAddress-Methode**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress) verwendet, um eine Multicastadresse vom Server an fordern. Wenn die Anforderung erfolgreich ist, wird ein [**IMcastLeaseInfo-Zeiger**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo) zurückgegeben. Die von dieser Schnittstelle verfügbar gemachte [**EnumerateAddresses-Methode**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses) kann dann verwendet werden, um die Adressen zu erhalten.

Jedes Medienobjekt, das der Konferenz zugeordnet ist, macht eine [**ITConnection-Schnittstelle**](itconnection.md) verfügbar. Die [**ITConnection::SetAddressInfo-Methode**](itconnection-setaddressinfo.md) ermöglicht die Zuweisung der Multicastadressen, die den Medien der Konferenz zugeordnet werden. Die Adresse muss für jede **ITConnection-Schnittstelle** jedes Media-Objekts festgelegt werden, das der Konferenz zugeordnet ist.

 

 



