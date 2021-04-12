---
description: Mit der Liste "die Liste der \_ \_ \_ verfügbaren ioctl-Adressen" können Anwendungsentwickler eine Liste von IPv6-und IPv4-Zieladressen sortieren, um die beste verfügbare Adresse für eine Verbindung zu ermitteln. Die Liste der in der Liste für die Liste der IP \_ \_ -Adressen \_ Sortierungen wird unter Windows XP und höher unterstützt
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: Verwenden von SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6452023b69ccf72c78b393c5059fee497997af51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217979"
---
# <a name="using-sio_address_list_sort"></a>Verwenden der "sio- \_ Adress \_ Liste" \_

Mit **der \_ \_ Liste \_** "die Liste der verfügbaren ioctl-Adressen" können Anwendungsentwickler eine Liste von IPv6-und IPv4-Zieladressen sortieren, um die beste verfügbare Adresse für eine Verbindung zu ermitteln. Die Liste der in der Liste für die Liste der IP- **\_ Adressen \_ \_ Sortierungen** wird unter Windows XP und höher unterstützt

Unter Windows Vista und höher übernimmt die Funktion "Funktion" von "| [**atesortedadresssspairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) " eine angegebene Liste potenzieller IP-Zieladressen, fasst die Zieladressen mit den lokalen IP-Adressen des Host Computers zusammen und sortiert die Paare entsprechend dem Adress Paar, das sich am besten für die Kommunikation zwischen den beiden Peers eignet. Die Funktion "| **atesortedadresssspairs** " sollte anstelle der " **SIO \_ Address \_ List \_** ioctl" unter Windows Vista und höher verwendet werden.

In den folgenden Abschnitten werden die Verwendungs Überlegungen für die Verwendung der Liste "die **\_ \_ Liste \_** der

## <a name="parameters"></a>Parameter

Der an die Größe der " **SIO \_ Address \_ List \_** "-Sortierung an [**\_ \_**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) Jede [**\_ Socketadresse**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) in der Liste muss das sockaddr \_ IN6-Format aufweisen.

In der Liste der "sio-Adressen" **\_ \_ \_ Sortieren** "ioctl" sortiert IPv6-und IPv4-Adressen unter Windows Vista und höher. Alle IPv4-Adressen in der Liste, die sortiert werden sollen, müssen im IPv4-zugeordneten IPv6-Adressformat vorliegen. Weitere Informationen zum IPv4-zugeordneten IPv6-Adressformat finden Sie unter [Dual Stack Sockets (Dual-Stack-Sockets](dual-stack-sockets.md)).

Unter Windows Server 2003 und Windows XP sortiert die **Liste der "sio- \_ Adress \_ Liste \_** " nur IPv6-Adressen. IPv4-Adressen im IPv4-zugeordneten IPv6-Adressformat werden nicht unterstützt.

Bei der Ausgabe kann der **iaddresscount** -Member [**der \_ socketadressauflistungs \_**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) -Struktur kleiner als bei der Eingabe sein, wenn der IOCTL-Code ermittelt, dass einige Zieladressen ungültig sind.

## <a name="sorting-determination"></a>Sortier Bestimmung

Die Sortierreihenfolge für IPv6-Adressen für die Liste der "sio- \_ Adresse" \_ sortiert " \_ ioctl" basiert auf der Präfix Richtlinien Tabelle. Die Präfix Richtlinien Tabelle wird mithilfe des Befehlszeilen-Hilfsprogramms *Netsh.exe* konfiguriert. Die folgenden Befehlszeilen Ausschnitte veranschaulichen grundlegende Konfigurations Befehle für *Netsh.exe* -Präfix der Richtlinien Tabelle:

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> Unter Windows Server 2003 und Windows XP lautete der erste oben aufgeführte Netsh-Befehl wie folgt. Alle anderen zugehörigen Befehle sind identisch.

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

Die Adress Reihenfolge wird auch durch einen Algorithmus bestimmt, der in RFC 3484 bei der *Standard Adressauswahl für IPv6 (Internet Protocol, Version 6)* , die vom IETF veröffentlicht wurde, beschrieben wird. Weitere Informationen finden Sie unter [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484). (Diese Ressource ist möglicherweise nur in englischer Sprache verfügbar.)

**In der \_ \_** Liste der "sio-Adressen" können Sie ioctl sortieren, um Adressen vom besten zum schlechtesten zu **\_ \_ \_ Sortieren** Bei Site-Local-Adressen wird \_ durch \_ \_ die Liste der in der Liste der Adresslisten Sortierungen entweder die Bereichs-ID ausgefüllt oder die Adresse entfernt.

In der Liste der für die zu **\_ \_ \_ Sortier** enden IP-Adressen wird die Quelladresse ignoriert, die an den Socket gebunden ist, und nur nach der als Parameter übergebenen Ziel Adressliste sortiert.

Die Funktion "| [**atesortedadresssspairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) " sollte anstelle der " **SIO \_ Address \_ List \_** ioctl" unter Windows Vista und höher verwendet werden. Die Funktion " **anatesortedadresssspairs** " gibt eine Liste von Adress Paaren zurück, die eine lokale Quelladresse und eine Zieladresse enthalten. Dadurch wird eine Anwendung zur richtigen Quelladresse für die einzelnen Zieladressen bereitstellt. Eine Anwendung kann die Ergebnisse auch filtern, indem Sie nach einer bestimmten Quelladresse sucht. in den Ergebnissen.

## <a name="requirements"></a>Anforderungen

Die Liste der in der Liste für die TLS- **\_ Adressen \_ \_ Sortierung** ist in der Header Datei " *Winsock2. h* " definiert. Auf dem Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Header Dateien geändert, und die Datei "IOCTL **\_ \_ \_ Sort** " in der " *Ws2def. h* "-Header Datei ist in der Header Datei " Beachten Sie, dass die Header Datei " *Ws2def. h* " automatisch in " *Winsock2. h*" enthalten ist und niemals direkt verwendet werden sollte.

Die Liste der in der Liste für die Liste der IP- **\_ Adressen \_ \_ Sortierungen** wird unter Windows XP und höher unterstützt

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**"Kreatesortedadresssspairs"**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
