---
description: Die Multicast-com-Schnittstellen ermöglichen den Zugriff auf die Netzwerke, um Leases für Multicast Adressen zuzuordnen, zu erneuern und freizugeben.
ms.assetid: d4da9616-bdb4-4919-96aa-9e45582b05dd
title: Multicast-com-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01370372e3ea05b27dc789f90918b148075c28f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749529"
---
# <a name="multicast-com-interfaces"></a>Multicast-com-Schnittstellen

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die Multicast-com-Schnittstellen ermöglichen den Zugriff auf die Funktion des Netzwerks zum zuordnen, erneuern und Freigeben von Leases für Multicast Adressen. Sie Kapseln eine Reihe von Funktions-und Datenstruktur Definitionen. Die COM-Schnittstellen machen dem Programmierer den Aufwand, diese Datenstrukturen zu verstehen und zu bearbeiten. Da TAPI 3 selbst com-basiert ist, ist die Zuordnung von Multicast Adressen auf eine Weise möglich, die mit den anderen von TAPI 3 bereitgestellten Funktionen konsistent ist. Anwendungen, die mit Visual Basic-, Java-oder Skriptsprachen geschrieben wurden, die normalerweise nicht direkt auf die Windows-API zugreifen können, können diese Schnittstellen verwenden.

Die Zuordnung von Multicast Adressen ist zurzeit der Betreff einer IETF-Arbeitsgruppe. Wenn Sie auf aktuelle Informationen zugreifen möchten, Fragen Sie "MDHCP" oder "MADCAP" und "Internet Draft" mithilfe eines beliebigen Internet Suchmoduls ab. Zusätzlich zu MADCAP umfasst die vorgeschlagene Architektur ein Protokoll für die Server-zu-Server-Koordination innerhalb einer Domäne oder als sowie ein Protokoll für die Interoperabilität zwischen den Domänen. Obwohl sich diese Architektur gerade weiterentwickelt, muss sich der Client nicht mit den Details dieses Schemas befassen.

Diese Komponente unterstützt zurzeit nur IP-Adressen der Version 4.

> [!Note]  
> Das für diese Schnittstellen verwendete Protokoll wird derzeit als MADCAP bezeichnet. In früheren Versionen wurde sie als MDHCP bezeichnet.

 

Das Multicast Objekt wird durch Aufrufen von **CoCreateInstance** in der [**imcastaddressallocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation) -Schnittstelle erstellt. Die **imcastaddressallocation** -Schnittstelle macht die [**enumeratescopes**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes) -Methode verfügbar, die es einer Anwendung ermöglicht, eine Liste aller verfügbaren Multicast Bereiche zu erhalten.

Nachdem ein Arbeitsbereich abgerufen wurde, wird die [**requestaddress**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress) -Methode verwendet, um eine Multicast Adresse vom Server anzufordern. Wenn die Anforderung erfolgreich ist, wird ein [**imcastleaseinfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo) -Zeiger zurückgegeben. Die [**enumerateadressen**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses) -Methode, die von dieser Schnittstelle verfügbar gemacht wird, kann dann zum Abrufen der Adressen verwendet werden.

Jedes Medienobjekt, das der Konferenz zugeordnet ist, macht eine [**itconnection**](itconnection.md) -Schnittstelle verfügbar. Die [**itconnection:: setaddressinfo**](itconnection-setaddressinfo.md) -Methode ermöglicht die Zuweisung der Multicast Adressen, die an die Medien der Konferenz bezogen werden. Die Adresse muss für jede **itconnection** -Schnittstelle jedes Medien Objekts festgelegt werden, das der Konferenz zugeordnet ist.

 

 



