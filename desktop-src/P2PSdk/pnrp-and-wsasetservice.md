---
description: PNRP verwendet die wsasetservice-Funktion, um Peer Namen zu registrieren oder zu entfernen.
ms.assetid: ea7941cd-2b3c-42d1-a291-759cbc32db0c
title: PNRP und wsasetservice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a04251a8b038c5895ae5dfafd65be9263edfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349226"
---
# <a name="pnrp-and-wsasetservice"></a>PNRP und wsasetservice

PNRP verwendet die [**wsasetservice**](winsock-nsp-reference-links.md) -Funktion, um [Peer Namen](peer-names.md)zu registrieren oder zu entfernen.

## <a name="registering-a-name"></a>Registrieren eines Namens

Die Registrierung umfasst einen Peernamen und eine Gruppe von Endpunkten, an die ein Dienst kontaktiert werden kann. Eine Registrierung ist spezifisch für eine PNRP-Cloud. Nachdem ein Peer registriert wurde, gibt es eine Verzögerung zwischen der Registrierung und der Weitergabe der Registrierungsinformationen an andere Knoten. Während dieser Zeit sind andere Knoten möglicherweise nicht in der Lage, einen neu registrierten Peer aufzulösen.

Die Dienst Registrierung ist nicht persistent.

-   Wenn ein Client Prozess, der einen [**Peernamen registriert, das WSACleanup**](winsock-nsp-reference-links.md)-Ereignis beendet oder aufruft, wird die Registrierung des Peer namens aufgehoben.
-   Wenn ein angegebener PeerName bereits vom aktuellen Prozess in der gleichen Cloud registriert ist, wird er durch neue Registrierungs Werte ersetzt.

Beim Registrieren eines Peer namens müssen die folgenden Parameterwerte angegeben werden:

-   der *ESS Operation* -Parameter muss den Wert " **rnrservice \_ Register**" aufweisen.
-   der *dwcontrolflags* -Parameter muss NULL (0) sein.

Beim Registrieren eines Peer namens muss die [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur, auf die durch den *lpqsreginfo* -Parameter verwiesen wird, die folgenden Werte enthalten:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe der-Struktur an.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszserviceingestancename**
</dt> <dd>

Gibt einen zu Registrier ingpeer Namen an. Wenn der [PeerName](peer-names.md) nicht gesichert ist, ist die Identität optional. Wenn die Identität als **null** angegeben ist, verwendet PNRP die lokale Identität des Computers – standardmäßig.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpserviceclassid**
</dt> <dd>

Muss "svcid \_ pnrpname" lauten.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpversion**
</dt> <dd>

Ignoriert. Auf **null** festgelegt.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszcomment**
</dt> <dd>

Ignoriert. Allerdings muss die Zeichenfolge weiterhin weniger als 40 Zeichen enthalten, einschließlich des **null** -Terminator.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwnamespace**
</dt> <dd>

Muss entweder ' **NS \_ ' pnrpname** ' oder ' **NS \_ all**' sein.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpnsproviderid**
</dt> <dd>

Muss entweder der **NS- \_ Anbieter \_ pnrpname** oder **null** sein.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszcontext**
</dt> <dd>

Muss ein cloudName, eine leere Zeichenfolge oder **null** sein. Wenn dieser Wert **null** oder eine leere Zeichenfolge ist, wird die Standard-Cloud "Global" verwendet. Andernfalls muss Sie auf einen gültigen cloudnamen verweisen.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwnumofprotokolle**
</dt> <dd>

Ignoriert. Auf NULL (0) festgelegt.

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszquerystring**
</dt> <dd>

Ignoriert. Auf **null** festgelegt.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwnumofcsaddrs**
</dt> <dd>

Gibt die Anzahl der Adressen an, die von einem Dienst registriert wurden. Die maximale Anzahl von Adressen, die für einen einzelnen Namen registriert werden kann, ist 10.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsabuffer**
</dt> <dd>

Zeiger auf eine Liste von Adressen, die registriert werden sollen.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwoutputflags**
</dt> <dd>

Ignoriert. Auf NULL (0) festgelegt.

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpblob**
</dt> <dd>

Ein Zeiger auf eine [**BLOB**](winsock-nsp-reference-links.md) -Struktur, die auf eine [**pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) -Struktur zeigt. Bestimmte Parameter in der **pnrpinfo** -Struktur müssen festgelegt werden. Weitere Informationen finden Sie im folgenden Abschnitt der **pnrpinfo** -Struktur.

</dd> </dl>

## <a name="pnrpinfo-structure"></a>Pnrpinfo-Struktur

Wenn das **lpblob** -Element der [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur festgelegt ist, müssen die folgenden Member der [**pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) -Struktur festgelegt werden:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe der-Struktur an.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszidentity**
</dt> <dd>

Gibt die Identität des Peer namens an, der mit [**peeridentitycreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)erstellt wird. Wenn ein PeerName nicht gesichert ist, ist die Identität optional. Wenn die Identität als **null** angegeben ist, verwendet PNRP die lokale Identität des Computers – standardmäßig.

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nmaxresolve**
</dt> <dd>

Ignoriert. Auf NULL (0) festgelegt.

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwtimeout**
</dt> <dd>

Ignoriert. Auf NULL (0) festgelegt.

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwlifetime**
</dt> <dd>

Gibt die Anzahl der Sekunden zwischen Aktualisierungs Vorgängen an.

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**einlösungs Vektor**
</dt> <dd>

Ignoriert. Auf NULL (0) festgelegt.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**
</dt> <dd>

Muss entweder NULL (0) oder **pnrpinfo- \_ Hinweis** sein. Der Standardwert ist null (0). Dies bedeutet, dass der Dienst identifizierungsort der PNRP-ID mit der IP-Adresse in **sahint** erstellt wird. Andernfalls wird der Dienst Speicherort erstellt, indem die erste IP-Adresse im ersten IPv6-Eintrag des **lpcsabuffer** -Members verwendet wird.

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**sahint**
</dt> <dd>

Gibt die IPv6-Adresse für den Hinweis an.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**ennamestate**
</dt> <dd>

Ignoriert. Auf NULL (0) festgelegt.

</dd> </dl>

## <a name="unregistering-a-peer-name"></a>Aufheben der Registrierung eines Peer namens

In der folgenden Liste sind wichtige Informationen zum Aufheben der Registrierung eines Peer namens aufgeführt.

-   Nur eine Anwendung, die einen Peernamen registriert, kann die Registrierung aufheben.
-   Die Registrierung eines Peer namens wird automatisch aufgeh [**oben, wenn WSACleanup**](winsock-nsp-reference-links.md) aufgerufen wird.
-   PNRP entfernt immer die gesamte Dienstnamen Registrierung. Das Entfernen einzelner Adressen ist nicht zulässig.
-   Beim Aufheben der Registrierung eines Namens muss der Wert des Parameters " *ESS Operation* " den Wert " **rnrservice \_ Delete**" aufweisen.
-   PNRP unterstützt den **rnrservice \_**-Registrierungs Wert nicht.
-   Der *dwcontrolflags* -Parameter muss NULL (0) sein.

Beim Aufheben der Registrierung eines Namens muss die [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur, auf die der *lpqsreginfo* -Parameter verweist, die folgenden Werte enthalten:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe der-Struktur an.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszserviceingestancename**
</dt> <dd>

Gibt einen Peer Namen für die Aufhebung der Registrierung an.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpserviceclassid**
</dt> <dd>

Muss " **svcid \_ pnrpname**" lauten.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpversion**
</dt> <dd>

Ignoriert. Auf **null** festgelegt.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszcomment**
</dt> <dd>

Ignoriert. Auf **null** festgelegt.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwnamespace**
</dt> <dd>

Muss entweder ' **NS \_ ' pnrpname** ' oder ' **NS \_ all**' sein.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpnsproviderid**
</dt> <dd>

Muss entweder der **NS- \_ Anbieter \_ pnrpname** oder **null** sein.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszcontext**
</dt> <dd>

Muss ein cloudName, eine leere Zeichenfolge oder **null** sein. Wenn dieser Wert **null** oder eine leere Zeichenfolge ist, wird die Standard-Cloud "Global" verwendet. Andernfalls muss Sie auf einen gültigen cloudnamen verweisen.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwnumofprotokolle**
</dt> <dd>

Ignoriert. Auf NULL (0) festgelegt.

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszquerystring**
</dt> <dd>

Ignoriert. Auf **null** festgelegt.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwnumofcsaddrs**
</dt> <dd>

Ignoriert. Auf **null** festgelegt.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsabuffer**
</dt> <dd>

Ignoriert. Auf **null** festgelegt.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwoutputflags**
</dt> <dd>

Ignoriert. Auf NULL (0) festgelegt.

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpblob**
</dt> <dd>

Ein Zeiger auf eine [**BLOB**](winsock-nsp-reference-links.md) -Struktur, die auf eine [**pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) -Struktur zeigt. Der **lpszidentity** -Member der **lpblob** -Struktur identifiziert den Namen der Identität, die zum Registrieren eines Peer namens verwendet wird. Die übrigen Elemente müssen auf dieselben Werte festgelegt werden, die beim Registrieren eines Namens verwendet werden.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PNRP und BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP und wsaqueryset](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**Pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[PNRP-NSP-Fehler Codes](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSACleanup**](winsock-nsp-reference-links.md)
</dt> <dt>

**Wsasetservice**
</dt> </dl>

 

 



