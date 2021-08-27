---
description: Mit der \_ Sortier-IOCTL für SIO ADDRESS LIST können \_ \_ Anwendungsentwickler eine Liste von IPv6- und IPv4-Zieladressen sortieren, um die beste verfügbare Adresse für die Verbindungsherstellung zu ermitteln. SIO \_ ADDRESS \_ LIST SORT \_ IOCTL wird unter Windows XP und höher unterstützt.
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: Verwenden von SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0bce27088052bfc029047d5f498ad90962567b50015a5331b26016e455d770
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121144"
---
# <a name="using-sio_address_list_sort"></a>Verwenden von SIO \_ ADDRESS \_ LIST \_ SORT

Mit der **\_ \_ \_ Sortier-IOCTL** für SIO ADDRESS LIST können Anwendungsentwickler eine Liste von IPv6- und IPv4-Zieladressen sortieren, um die beste verfügbare Adresse für die Verbindungsherstellung zu ermitteln. **SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL wird auf Windows XP und höher unterstützt.

Auf Windows Vista und höher nimmt die [**CreateSortedAddressPairs-Funktion**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) eine bereitgestellte Liste potenzieller IP-Zieladressen an, paart die Zieladressen mit den lokalen IP-Adressen des Hostcomputers und sortiert die Paare nach dem Adresspaar, das am besten für die Kommunikation zwischen den beiden Peers geeignet ist. Die **CreateSortedAddressPairs-Funktion** sollte anstelle von **SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL auf Windows Vista und höher verwendet werden.

In den folgenden Abschnitten werden Überlegungen zur Verwendung von **SIO \_ ADDRESS LIST \_ SORT \_ beschrieben.**

## <a name="parameters"></a>Parameter

Der an **SIO \_ ADDRESS \_ LIST \_ SORT** übergebene Puffer ist eine [**SOCKET ADDRESS \_ \_ LIST-Struktur.**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) Jede [**\_ SOCKETADRESSE**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) in der Liste muss im SOCKADDR \_ IM6-Format vorliegen.

Die **SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL sortiert sowohl IPv6- als auch IPv4-Adressen nach Windows Vista und höher. Alle IPv4-Adressen in der Liste, die sortiert werden sollen, müssen im IPv4-zugeordneten IPv6-Adressformat vorliegen. Weitere Informationen zum IPv4-zugeordneten IPv6-Adressformat finden Sie unter [Dual-Stack-Sockets.](dual-stack-sockets.md)

Auf Windows Server 2003 und Windows XP sortiert **SIO \_ ADDRESS LIST \_ \_ SORT** nur IPv6-Adressen. IPv4-Adressen im IPv4-zugeordneten IPv6-Adressformat werden nicht unterstützt.

Bei der Ausgabe ist der **iAddressCount-Member** der [**SOCKET ADDRESS \_ \_ LIST-Struktur**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) möglicherweise kleiner als bei der Eingabe, wenn der IOCTL-Code feststellt, dass einige Zieladressen ungültig sind.

## <a name="sorting-determination"></a>Sortierungsermittlung

Die Sortierreihenfolge für IPv6-Adressen für die \_ \_ SORT-IOCTL der SIO-ADRESSLISTE \_ basiert auf der Präfixrichtlinientabelle. Die Präfixrichtlinientabelle wird mit dem *BefehlszeilenprogrammNetsh.exe* konfiguriert. Die folgenden Befehlszeilenausschnitte veranschaulichen grundlegendeNetsh.exeKonfigurationsbefehle *für* Präfixrichtlinientabellen:

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> Auf Windows Server 2003 und Windows XP lautete der erste oben aufgeführte netsh-Befehl wie folgt. Alle anderen zugehörigen Befehle sind identisch.

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

Die Adressreihenfolge wird auch durch einen Algorithmus bestimmt, der in RFC 3484 unter *Standardadressauswahl für Internetprotokoll Version 6 (IPv6)* beschrieben ist, die von der IETF veröffentlicht wird. Weitere Informationen finden Sie unter [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484). (Diese Ressource ist möglicherweise nur auf Englisch verfügbar.)

Die **SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL sortiert Adressen vom besten zum schlechtesten und füllt bei Bedarf **\_ sin6-Bereichs-ID-Member \_** aus. Bei standortlokalen Adressen füllt SIO \_ ADDRESS LIST SORT entweder die \_ \_ Bereichs-ID aus oder entfernt die Adresse.

**SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL ignoriert die Quelladresse, die an den Socket gebunden ist, und sortiert nur nach der Zieladressliste, die als Parameter übergeben wird.

Die [**CreateSortedAddressPairs-Funktion**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) sollte anstelle von **SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL auf Windows Vista und höher verwendet werden. Die **CreateSortedAddressPairs-Funktion** gibt eine Liste von Adresspaaren zurück, die eine lokale Quelladresse und eine Zieladresse enthält. Dadurch wird einer Anwendung die richtige Quelladresse für jede Zieladresse zur Verfügung stehen. Eine Anwendung kann die Ergebnisse auch filtern, indem sie nach einer bestimmten Quelladresse sucht. in den Ergebnissen.

## <a name="requirements"></a>Anforderungen

Die **SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL wird in der *Headerdatei Winsock2.h* definiert. Im Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Headerdateien geändert, und **SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL wird in der *Headerdatei Ws2def.h* definiert. Beachten Sie, dass die *Headerdatei Ws2def.h* automatisch in *Winsock2.h* enthalten ist und niemals direkt verwendet werden sollte.

**SIO \_ ADDRESS LIST \_ \_ SORT** IOCTL wird auf Windows XP und höher unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
