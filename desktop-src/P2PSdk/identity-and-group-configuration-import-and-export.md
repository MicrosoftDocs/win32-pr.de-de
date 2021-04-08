---
description: Peer-Identitäts-und Gruppen Konfigurationsdateien können mithilfe der Funktionen zum Importieren und Exportieren von Identitäten, die sich in den Identitäts-Manager-und Gruppierungs-APIs befinden, von einem Endpunkt zu einem anderen importiert und exportiert
ms.assetid: 876d9c57-15f6-4f5e-8035-792e15f8035e
title: Importieren und Exportieren von Identitäts-und Gruppen Konfigurationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a356f2747e3c8276446568b6f82bcbd773b14af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756601"
---
# <a name="identity-and-group-configuration-import-and-export"></a>Importieren und Exportieren von Identitäts-und Gruppen Konfigurationen

Peer-Identitäts-und Gruppen Konfigurationsdateien können mithilfe der Funktionen zum Importieren und Exportieren von Identitäten, die sich in den Identitäts-Manager-und Gruppierungs-APIs befinden, von einem Endpunkt zu einem anderen importiert und exportiert Diese Funktionen sind nützlich, da Sie Benutzern das schnelle und bequeme Exportieren von Identitäten und das Gruppieren von Konfigurationsinformationen von einem Computer auf einen anderen Computer ermöglichen.

## <a name="importing-and-exporting-peer-identity-data"></a>Importieren und Exportieren von Peer-Identitätsdaten

Die Identitätsdaten eines Peers werden exportiert, indem [**peeridentityexport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) mit dem zu exportierenden Identitäts Namen und ein Kennwort zum Verschlüsseln der zugehörigen Anmelde Informationen aufgerufen wird. Diese Funktion gibt eine XML-Zeichenfolge mit dem Identitäts Namen des Peers und den verschlüsselten Anmelde Informationen für die jeweilige Identität zurück, die dann mithilfe eines externen Übertragungsmechanismus, z. b. e-Mail, an einen anderen Computer übergeben werden kann. Das folgende Beispiel zeigt das Format der XML-Zeichenfolge:

``` syntax
<PEERIDENTITYEXPORT VERSION="1.0">
   <PEERNAME>
     <!-- UTF-8 encoded peer name of the identity -->
   </PEERNAME>
   <DATA xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
      <!-- base64 encoded / PFX encoded and encrypted IDC with the private key -->
   </DATA>
</PEERIDENTITYEXPORT>
```

Die exportierten Identitätsdaten können abgerufen werden, indem Sie " [**Peer Identity Import**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)" aufrufen und die XML-Zeichenfolge mit dem Kennwort übergeben, das im vorherigen Aufruf von " [**Peer Identity Export**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)" angegeben wurde. Diese Funktion gibt den Peernamen der importierten Identität zurück. Der importierte Identitäts Name und die Anmelde Informationen können genau wie ein Identitäts Name verwendet werden, der von " [**Peer-enumidentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) " oder " [**Peer**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)Identity" zurückgegeben wird.

> [!Note]  
> Wenn Sie " [**Peer**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)Identity" aufrufen, muss der Benutzer der Anwendung oder der API ein sicheres Kennwort mit ausreichender Länge angeben. Dies ist wichtig, da die importierten Identitätsdaten den privaten Schlüssel für die Identität enthalten.

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a>Importieren und Exportieren einer Gruppen Identitäts Konfiguration

Mithilfe der Peer Gruppierung kann ein Peer Gruppen Konfigurationsdaten von einem Endpunkt zu einem anderen exportieren, indem bestimmte Import-und Export-APIs verwendet werden. Zum Importieren von Konfigurationsdaten muss die Identität des Peers, der den Import durchführt (und der zuvor den Export durchgeführt hat), auf dem Computer vorhanden sein, auf dem die Konfigurationsdaten importiert werden sollen. Diese Identität kann durch Exportieren und importieren durch die Methoden abgerufen werden, die im vorherigen Abschnitt dieses Themas angegeben sind: [importieren und Exportieren von Peer Identitätsdaten](#importing-and-exporting-peer-identity-data).

Die Gruppen Konfigurationsdaten enthalten alle Informationen für eine Identität, um eine Gruppe von einem neuen Endpunkt zu verknüpfen. Die Konfigurationsdaten enthalten insbesondere die GMC-Kette, den gruppenpeernamen, den cloudnamen, den Bereich und einen Satz von PNRP-spezifischen Flags. Für eine Identität, die eine Gruppe besitzt, ist ein privater Schlüssel für die Gruppe in den Gruppen Konfigurationsinformationen enthalten.

> [!Note]  
> Beim Aufrufen von " [**Peer groupexportconfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)" muss ein Anwendungs-oder API-Benutzer ein sicheres Kennwort mit ausreichender Länge angeben. Dies ist wichtig, da die importierten Identitätsdaten den privaten Schlüssel für die Gruppe enthalten.

 

Rufen Sie zum Exportieren der aktuellen Peer Gruppenkonfiguration [**peergroupexportconfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)auf, und übergeben Sie dabei das Handle an die Gruppe (abgerufen durch einen vorherigen [**peergroupjoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)-, [**peergroupopen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)-oder [**peergroupcreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)-Befehl) und ein Kennwort, das zum Verschlüsseln und schützen der Konfigurationsdatei verwendet wird. Diese Funktion gibt eine XML-Zeichenfolge zurück, die die Konfiguration im folgenden Beispiel enthält, das dann in eine Datei geschrieben und mithilfe eines externen Übertragungsmechanismus (z. b. per e-Mail) an einen anderen Computer übergeben werden kann.

``` syntax
<PEERGROUPCONFIG VERSION="1.0">
  <IDENTITYPEERNAME>
    <!-- UTF-8 encoded peer name of the identity -->
  </IDENTITYPEERNAME>
  <GROUPPEERNAME>
    <!-- UTF-8 encoded peer name of the group -->
  </GROUPPEERNAME>
  <CLOUDNAME>
    <!-- UTF-8 encoded Unicode name of the cloud -->
  </CLOUDNAME>
  <SCOPE>
    <!-- UTF-8 encoded Unicode name of the scope: global, site-local, link-local -->
  </SCOPE>
  <CLOUDFLAGS>
    <!-- A DWORD that contains cloud-specific settings, represented as a string -->
  </CLOUDFLAGS>
  <GMC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
    <!-- base64/PKCS7 encoded GMC chain -->
  </GMC>
</PEERGROUPCONFIG>
```

Nachdem Sie die Gruppenkonfiguration als XML-Zeichenfolge erhalten haben, kann die Gruppe importiert werden, indem Sie " [**Peer groupimportconfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) " mit der XML-Konfigurations Zeichenfolge und dem für " [**Peer groupexportconfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)" angegebenen spezifischen Kennwort aufrufen. Diese Funktion gibt einen Identitäts Namen und einen gruppenpeernamen zurück, die dann für [**peergroupopen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) und eine Verbindung mit der eingerichteten Gruppe bereitgestellt werden können.

 

 



