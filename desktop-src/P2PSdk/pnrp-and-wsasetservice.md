---
description: PNRP verwendet die WSASetService-Funktion, um Peernamen zu registrieren oder zu entfernen.
ms.assetid: ea7941cd-2b3c-42d1-a291-759cbc32db0c
title: PNRP und WSASetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afbc11e65c9d583f91b5070e960435612ad05717b6ccfe087924da133c531b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518100"
---
# <a name="pnrp-and-wsasetservice"></a>PNRP und WSASetService

PNRP verwendet die [**WSASetService-Funktion,**](winsock-nsp-reference-links.md) um [Peernamen](peer-names.md)zu registrieren oder zu entfernen.

## <a name="registering-a-name"></a>Registrieren eines Namens

Die Registrierung umfasst einen Peernamen und eine Gruppe von Endpunkten, mit denen ein Dienst kontaktiert werden kann. Eine Registrierung ist spezifisch für eine PNRP-Cloud. Nach der Registrierung eines Peers kommt es zu einer Verzögerung zwischen der Registrierung und der Weitergabe der Registrierungsinformationen an andere Knoten. Während dieser Zeit können andere Knoten einen neu registrierten Peer möglicherweise nicht auflösen.

Die Dienstregistrierung ist nicht persistent.

-   Wenn ein Clientprozess, der einen Peernamen registriert, beendet wird oder [**WSACleanup**](winsock-nsp-reference-links.md)aufruft, wird die Registrierung des Peernamens aufgehoben.
-   Wenn ein angegebener Peername bereits durch den aktuellen Prozess in derselben Cloud registriert ist, wird er durch neue Registrierungswerte ersetzt.

Beim Registrieren eines Peernamens müssen die folgenden Parameterwerte angegeben werden:

-   Der *essOperation-Parameter* muss den Wert **RNRSERVICE \_ REGISTER aufweisen.**
-   Der *dwControlFlags-Parameter* muss 0 (null) sein.

Beim Registrieren eines Peernamens muss die [**LPWSAQUERYSET-Struktur,**](pnrp-and-wsaqueryset.md) auf die der *lpqsRegInfo-Parameter* verweist, die folgenden Werte enthalten:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe dieser Struktur an.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Gibt einen zu registrierenden Peernamen an. Wenn der [Peername](peer-names.md) nicht gesichert ist, ist die Identität optional. Wenn die Identität als **NULL** angegeben ist, verwendet PNRP standardmäßig die lokale Identität des Computers.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Muss SVCID \_ PNRPNAME sein.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Ignoriert. Legen Sie auf **NULL** fest.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Ignoriert. Die Zeichenfolge muss jedoch immer noch weniger als 40 Zeichen umfassen, einschließlich des **NULL-Abschlusszeichens.**

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Muss entweder **NS \_ PNRPNAME** oder **NS \_ ALL** sein.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Muss entweder **NS \_ PROVIDER \_ PNRPNAME** oder **NULL** sein.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Muss ein Cloudname, eine leere Zeichenfolge oder **NULL** sein. Wenn dieser Wert **NULL** oder eine leere Zeichenfolge ist, wird die Standardcloud "Global" verwendet. Andernfalls muss er auf einen gültigen Cloudnamen verweisen.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Ignoriert. Auf 0 (null) festgelegt.

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Ignoriert. Legen Sie auf **NULL** fest.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Gibt die Anzahl der von einem Dienst registrierten Adressen an. Die maximale Anzahl von Adressen, die für einen einzelnen Namen registriert werden können, beträgt 10.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Zeiger auf eine Liste der zu registrierende Adressen.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Ignoriert. Auf 0 (null) festgelegt.

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Zeiger auf eine [**BLOB-Struktur,**](winsock-nsp-reference-links.md) die auf eine [**PNRPINFO-Struktur**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) zeigt. Bestimmte Parameter in der **PNRPINFO-Struktur** müssen festgelegt werden. Weitere Informationen finden Sie im folgenden **Abschnitt PNRPINFO-Struktur.**

</dd> </dl>

## <a name="pnrpinfo-structure"></a>PNRPINFO-Struktur

Wenn der **lpBlob-Member** der [**LPWSAQUERYSET-Struktur**](pnrp-and-wsaqueryset.md) festgelegt ist, müssen die folgenden Member der [**PNRPINFO-Struktur**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) festgelegt werden:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe dieser Struktur an.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**
</dt> <dd>

Gibt die Identität des Peernamens an, der mit [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)erstellt wird. Wenn ein Peername nicht gesichert ist, ist die Identität optional. Wenn die Identität als **NULL** angegeben ist, verwendet PNRP standardmäßig die lokale Identität des Computers.

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**
</dt> <dd>

Ignoriert. Auf 0 (null) festgelegt.

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**
</dt> <dd>

Ignoriert. Auf 0 (null) festgelegt.

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**
</dt> <dd>

Gibt die Anzahl von Sekunden zwischen Aktualisierungsvorgängen an.

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**
</dt> <dd>

Ignoriert. Auf 0 (null) festgelegt.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**Dwflags**
</dt> <dd>

Muss entweder null (0) oder **PNRPINFO \_ HINT** sein. Der Standardwert ist null (0). Dies bedeutet, dass der Dienstidentifikationsteil der PNRP-ID mithilfe der IP-Adresse in **saHint** erstellt wird. Andernfalls wird der Dienstspeicherort mithilfe der ersten IP-Adresse im ersten IPv6-Eintrag des **lpcsaBuffer-Members** erstellt.

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**
</dt> <dd>

Gibt die IPv6-Adresse für den Hinweis an.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**
</dt> <dd>

Ignoriert. Auf 0 (null) festgelegt.

</dd> </dl>

## <a name="unregistering-a-peer-name"></a>Aufheben der Registrierung eines Peernamens

In der folgenden Liste sind die wichtigen Informationen zum Aufheben der Registrierung eines Peernamens aufgeführt.

-   Nur eine Anwendung, die einen Peernamen registriert, kann die Registrierung aufheben.
-   Die Registrierung eines Peernamens wird automatisch aufgehoben, wenn [**WSACleanup**](winsock-nsp-reference-links.md) aufgerufen wird.
-   PNRP entfernt immer die gesamte Dienstnamenregistrierung. Das Entfernen einzelner Adressen ist nicht zulässig.
-   Wenn Sie die Registrierung eines Namens aufheben, muss der *essOperation-Parameter* den Wert **RNRSERVICE \_ DELETE aufweisen.**
-   PNRP unterstützt den Wert **RNRSERVICE \_ DEREGISTER** nicht.
-   Der *dwControlFlags-Parameter* muss 0 (null) sein.

Beim Aufheben der Registrierung eines Namens muss die [**LPWSAQUERYSET-Struktur,**](pnrp-and-wsaqueryset.md) auf die der *lpqsRegInfo-Parameter* verweist, die folgenden Werte enthalten:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe dieser Struktur an.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Gibt einen Peernamen an, der die Registrierung aufheben soll.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Muss **SVCID \_ PNRPNAME** sein.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Ignoriert. Legen Sie auf **NULL** fest.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Ignoriert. Legen Sie auf **NULL** fest.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Muss entweder **NS \_ PNRPNAME** oder **NS \_ ALL** sein.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Muss entweder **NS \_ PROVIDER \_ PNRPNAME** oder **NULL** sein.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Muss ein Cloudname, eine leere Zeichenfolge oder **NULL** sein. Wenn dieser Wert **NULL** oder eine leere Zeichenfolge ist, wird die Standardcloud "Global" verwendet. Andernfalls muss er auf einen gültigen Cloudnamen verweisen.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Ignoriert. Auf 0 (null) festgelegt.

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Ignoriert. Legen Sie auf **NULL** fest.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Ignoriert. Legen Sie auf **NULL** fest.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Ignoriert. Legen Sie auf **NULL** fest.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Ignoriert. Auf 0 (null) festgelegt.

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Zeiger auf eine [**BLOB-Struktur,**](winsock-nsp-reference-links.md) die auf eine [**PNRPINFO-Struktur**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) zeigt. Der **lpszIdentity-Member** der **lpBlob-Struktur** identifiziert den Namen der Identität, die zum Registrieren eines Peernamens verwendet wird. Die verbleibenden Member müssen auf die gleichen Werte festgelegt werden, die beim Registrieren eines Namens verwendet werden.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PNRP und BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP und WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[PNRP-NSP-Fehlercodes](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSACleanup**](winsock-nsp-reference-links.md)
</dt> <dt>

**WSASetService**
</dt> </dl>

 

 



