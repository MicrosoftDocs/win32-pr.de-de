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
# <a name="identity-and-group-configuration-import-and-export"></a><span data-ttu-id="0aabe-103">Importieren und Exportieren von Identitäts-und Gruppen Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="0aabe-103">Identity and Group Configuration Import and Export</span></span>

<span data-ttu-id="0aabe-104">Peer-Identitäts-und Gruppen Konfigurationsdateien können mithilfe der Funktionen zum Importieren und Exportieren von Identitäten, die sich in den Identitäts-Manager-und Gruppierungs-APIs befinden, von einem Endpunkt zu einem anderen importiert und exportiert</span><span class="sxs-lookup"><span data-stu-id="0aabe-104">Peer identity and group configuration files can be imported and exported from one endpoint to another by using the identity import and export functions located in the Identity Manager and Grouping APIs.</span></span> <span data-ttu-id="0aabe-105">Diese Funktionen sind nützlich, da Sie Benutzern das schnelle und bequeme Exportieren von Identitäten und das Gruppieren von Konfigurationsinformationen von einem Computer auf einen anderen Computer ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0aabe-105">These functions are useful because they allow a user to quickly and conveniently export identities and group configuration information from one computer to another computer.</span></span>

## <a name="importing-and-exporting-peer-identity-data"></a><span data-ttu-id="0aabe-106">Importieren und Exportieren von Peer-Identitätsdaten</span><span class="sxs-lookup"><span data-stu-id="0aabe-106">Importing and Exporting Peer Identity Data</span></span>

<span data-ttu-id="0aabe-107">Die Identitätsdaten eines Peers werden exportiert, indem [**peeridentityexport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) mit dem zu exportierenden Identitäts Namen und ein Kennwort zum Verschlüsseln der zugehörigen Anmelde Informationen aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0aabe-107">The identity data of a peer is exported by calling [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport) with the identity name to export and a password used to encrypt the associated credentials.</span></span> <span data-ttu-id="0aabe-108">Diese Funktion gibt eine XML-Zeichenfolge mit dem Identitäts Namen des Peers und den verschlüsselten Anmelde Informationen für die jeweilige Identität zurück, die dann mithilfe eines externen Übertragungsmechanismus, z. b. e-Mail, an einen anderen Computer übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="0aabe-108">This function returns an XML string that contains the identity name of the peer and the encrypted credentials for that specific identity, which can then be passed to a different computer by using an external transfer mechanism, such as e-mail.</span></span> <span data-ttu-id="0aabe-109">Das folgende Beispiel zeigt das Format der XML-Zeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="0aabe-109">The following example shows you the format of the XML string:</span></span>

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

<span data-ttu-id="0aabe-110">Die exportierten Identitätsdaten können abgerufen werden, indem Sie " [**Peer Identity Import**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)" aufrufen und die XML-Zeichenfolge mit dem Kennwort übergeben, das im vorherigen Aufruf von " [**Peer Identity Export**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)" angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="0aabe-110">The exported identity data can be retrieved by calling [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport), and passing in the XML string with the password supplied in the previous call to [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport).</span></span> <span data-ttu-id="0aabe-111">Diese Funktion gibt den Peernamen der importierten Identität zurück.</span><span class="sxs-lookup"><span data-stu-id="0aabe-111">This function returns the peer name of the imported identity.</span></span> <span data-ttu-id="0aabe-112">Der importierte Identitäts Name und die Anmelde Informationen können genau wie ein Identitäts Name verwendet werden, der von " [**Peer-enumidentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) " oder " [**Peer**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)Identity" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0aabe-112">The imported identity name and credentials can be used just like an identity name returned by [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) or [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span></span>

> [!Note]  
> <span data-ttu-id="0aabe-113">Wenn Sie " [**Peer**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)Identity" aufrufen, muss der Benutzer der Anwendung oder der API ein sicheres Kennwort mit ausreichender Länge angeben.</span><span class="sxs-lookup"><span data-stu-id="0aabe-113">When calling [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport), the application or API user must provide a strong password of sufficient length.</span></span> <span data-ttu-id="0aabe-114">Dies ist wichtig, da die importierten Identitätsdaten den privaten Schlüssel für die Identität enthalten.</span><span class="sxs-lookup"><span data-stu-id="0aabe-114">This is important because the imported identity data contains the private key for the identity.</span></span>

 

## <a name="importing-and-exporting-a-group-identity-configuration"></a><span data-ttu-id="0aabe-115">Importieren und Exportieren einer Gruppen Identitäts Konfiguration</span><span class="sxs-lookup"><span data-stu-id="0aabe-115">Importing and Exporting a Group Identity Configuration</span></span>

<span data-ttu-id="0aabe-116">Mithilfe der Peer Gruppierung kann ein Peer Gruppen Konfigurationsdaten von einem Endpunkt zu einem anderen exportieren, indem bestimmte Import-und Export-APIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0aabe-116">Peer Grouping allows a peer to export group configuration data from one endpoint to another by using specific import and export APIs.</span></span> <span data-ttu-id="0aabe-117">Zum Importieren von Konfigurationsdaten muss die Identität des Peers, der den Import durchführt (und der zuvor den Export durchgeführt hat), auf dem Computer vorhanden sein, auf dem die Konfigurationsdaten importiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0aabe-117">To import configuration data, the identity of the peer performing the import (and who previously performed the export) must be present on the computer where the configuration data is to be imported.</span></span> <span data-ttu-id="0aabe-118">Diese Identität kann durch Exportieren und importieren durch die Methoden abgerufen werden, die im vorherigen Abschnitt dieses Themas angegeben sind: [importieren und Exportieren von Peer Identitätsdaten](#importing-and-exporting-peer-identity-data).</span><span class="sxs-lookup"><span data-stu-id="0aabe-118">This identity can be obtained by exporting and importing it by the methods specified in the previous section of this topic: [Importing and Exporting Peer Identity Data](#importing-and-exporting-peer-identity-data).</span></span>

<span data-ttu-id="0aabe-119">Die Gruppen Konfigurationsdaten enthalten alle Informationen für eine Identität, um eine Gruppe von einem neuen Endpunkt zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="0aabe-119">The group configuration data contains all of the information for an identity to join a group from a new endpoint.</span></span> <span data-ttu-id="0aabe-120">Die Konfigurationsdaten enthalten insbesondere die GMC-Kette, den gruppenpeernamen, den cloudnamen, den Bereich und einen Satz von PNRP-spezifischen Flags.</span><span class="sxs-lookup"><span data-stu-id="0aabe-120">Specifically, the configuration data contains the GMC chain, group peer name, cloud name, scope, and a set of PNRP specific flags.</span></span> <span data-ttu-id="0aabe-121">Für eine Identität, die eine Gruppe besitzt, ist ein privater Schlüssel für die Gruppe in den Gruppen Konfigurationsinformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0aabe-121">For an identity that owns a group, a private key for the group is included in the group configuration information.</span></span>

> [!Note]  
> <span data-ttu-id="0aabe-122">Beim Aufrufen von " [**Peer groupexportconfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)" muss ein Anwendungs-oder API-Benutzer ein sicheres Kennwort mit ausreichender Länge angeben.</span><span class="sxs-lookup"><span data-stu-id="0aabe-122">When calling [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), an application or API user must provide a strong password of sufficient length.</span></span> <span data-ttu-id="0aabe-123">Dies ist wichtig, da die importierten Identitätsdaten den privaten Schlüssel für die Gruppe enthalten.</span><span class="sxs-lookup"><span data-stu-id="0aabe-123">This is important because the imported identity data contains the private key for the group.</span></span>

 

<span data-ttu-id="0aabe-124">Rufen Sie zum Exportieren der aktuellen Peer Gruppenkonfiguration [**peergroupexportconfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)auf, und übergeben Sie dabei das Handle an die Gruppe (abgerufen durch einen vorherigen [**peergroupjoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)-, [**peergroupopen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)-oder [**peergroupcreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)-Befehl) und ein Kennwort, das zum Verschlüsseln und schützen der Konfigurationsdatei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0aabe-124">To export the current peer group configuration, call [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig), passing in the handle to the group (obtained by a previous call to [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen), or [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)), and a password used to encrypt and protect the configuration file.</span></span> <span data-ttu-id="0aabe-125">Diese Funktion gibt eine XML-Zeichenfolge zurück, die die Konfiguration im folgenden Beispiel enthält, das dann in eine Datei geschrieben und mithilfe eines externen Übertragungsmechanismus (z. b. per e-Mail) an einen anderen Computer übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="0aabe-125">This function returns an XML string that contains the configuration in the format of the following example, which can then be written to a file and passed to another computer by using an external transfer mechanism, such as email.</span></span>

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

<span data-ttu-id="0aabe-126">Nachdem Sie die Gruppenkonfiguration als XML-Zeichenfolge erhalten haben, kann die Gruppe importiert werden, indem Sie " [**Peer groupimportconfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) " mit der XML-Konfigurations Zeichenfolge und dem für " [**Peer groupexportconfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig)" angegebenen spezifischen Kennwort aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0aabe-126">After obtaining the group configuration as an XML string, the group can be imported by calling [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) with the configuration XML string and the specific password supplied to [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig).</span></span> <span data-ttu-id="0aabe-127">Diese Funktion gibt einen Identitäts Namen und einen gruppenpeernamen zurück, die dann für [**peergroupopen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) und eine Verbindung mit der eingerichteten Gruppe bereitgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="0aabe-127">This function returns an identity name and a group peer name, which can then be supplied to [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) and a connection to the group established.</span></span>

 

 



