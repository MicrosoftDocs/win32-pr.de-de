---
description: Peeridentitäts- und Gruppenkonfigurationsdateien können mithilfe der Identitätsimport- und -exportfunktionen in den Identitäts-Manager- und Gruppierungs-APIs importiert und von einem Endpunkt in einen anderen exportiert werden.
ms.assetid: 876d9c57-15f6-4f5e-8035-792e15f8035e
title: Importieren und Exportieren der Identitäts- und Gruppenkonfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0102bda821b7157edc512aeea4a8e315c0dbfa1def85f9a61919ec0f2c86da39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519330"
---
# <a name="identity-and-group-configuration-import-and-export"></a>Importieren und Exportieren der Identitäts- und Gruppenkonfiguration

Peeridentitäts- und Gruppenkonfigurationsdateien können mithilfe der Identitätsimport- und -exportfunktionen in den Identitäts-Manager- und Gruppierungs-APIs importiert und von einem Endpunkt in einen anderen exportiert werden. Diese Funktionen sind nützlich, da sie es einem Benutzer ermöglichen, Identitäten und Konfigurationsinformationen schnell und bequem von einem Computer auf einen anderen zu exportieren.

## <a name="importing-and-exporting-peer-identity-data"></a>Importieren und Exportieren von Peeridentitätsdaten

Die Identitätsdaten eines Peers werden exportiert, indem [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) mit dem zu exportierenden Identitätsnamen und einem Kennwort zum Verschlüsseln der zugehörigen Anmeldeinformationen aufgerufen wird. Diese Funktion gibt eine XML-Zeichenfolge zurück, die den Identitätsnamen des Peers und die verschlüsselten Anmeldeinformationen für diese spezifische Identität enthält, die dann mithilfe eines externen Übertragungsmechanismus wie E-Mail an einen anderen Computer übergeben werden können. Das folgende Beispiel zeigt das Format der XML-Zeichenfolge:

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

Die exportierten Identitätsdaten können abgerufen werden, indem [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)aufgerufen und die XML-Zeichenfolge mit dem Kennwort übergeben wird, das im vorherigen Aufruf von [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)angegeben wurde. Diese Funktion gibt den Peernamen der importierten Identität zurück. Der importierte Identitätsname und die Anmeldeinformationen können genau wie ein Identitätsname verwendet werden, der von [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) oder [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)zurückgegeben wird.

> [!Note]  
> Beim Aufrufen von [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)muss der Anwendungs- oder API-Benutzer ein sicheres Kennwort mit ausreichender Länge angeben. Dies ist wichtig, da die importierten Identitätsdaten den privaten Schlüssel für die Identität enthalten.

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a>Importieren und Exportieren einer Gruppenidentitätskonfiguration

Peergruppierung ermöglicht einem Peer das Exportieren von Gruppenkonfigurationsdaten von einem Endpunkt zu einem anderen mithilfe bestimmter Import- und Export-APIs. Zum Importieren von Konfigurationsdaten muss die Identität des Peers, der den Import durchführte (und der zuvor den Export ausgeführt hat), auf dem Computer vorhanden sein, auf dem die Konfigurationsdaten importiert werden sollen. Diese Identität kann durch Exportieren und Importieren mithilfe der methoden abgerufen werden, die im vorherigen Abschnitt dieses Themas angegeben wurden: Importieren und Exportieren von [Peeridentitätsdaten.](#importing-and-exporting-peer-identity-data)

Die Gruppenkonfigurationsdaten enthalten alle Informationen für eine Identität, die einer Gruppe von einem neuen Endpunkt beitreten soll. Die Konfigurationsdaten enthalten insbesondere die GMC-Kette, den Gruppenspeernamen, den Cloudnamen, den Bereich und eine Reihe von PNRP-spezifischen Flags. Für eine Identität, die eine Gruppe besitzt, ist ein privater Schlüssel für die Gruppe in den Gruppenkonfigurationsinformationen enthalten.

> [!Note]  
> Beim Aufrufen von [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)muss ein Anwendungs- oder API-Benutzer ein sicheres Kennwort mit ausreichender Länge angeben. Dies ist wichtig, da die importierten Identitätsdaten den privaten Schlüssel für die Gruppe enthalten.

 

Um die aktuelle Peergruppenkonfiguration zu exportieren, rufen Sie [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)auf, und übergeben Sie das Handle an die Gruppe (abgerufen durch einen vorherigen Aufruf von [**PeerGroupJoin,**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)oder [**PeerGroupCreate)**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)und ein Kennwort, das zum Verschlüsseln und Schützen der Konfigurationsdatei verwendet wird. Diese Funktion gibt eine XML-Zeichenfolge zurück, die die Konfiguration im Format des folgenden Beispiels enthält, die dann in eine Datei geschrieben und mithilfe eines externen Übertragungsmechanismus, z. B. E-Mail, an einen anderen Computer übergeben werden kann.

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

Nachdem Sie die Gruppenkonfiguration als XML-Zeichenfolge erhalten haben, kann die Gruppe importiert werden, indem [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) mit der XML-Konfigurationszeichenfolge und dem für [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)angegebenen spezifischen Kennwort aufgerufen wird. Diese Funktion gibt einen Identitätsnamen und einen Gruppenspeernamen zurück, die dann an [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) und eine Verbindung mit der eingerichteten Gruppe bereitgestellt werden können.

 

 



