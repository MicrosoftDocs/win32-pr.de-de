---
description: PNRP verwendet die WSALookupServiceBegin-Funktion, um den Prozess zu starten, der einer Anwendung folgende Aufgaben ermöglicht.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP und WSALookupServiceBegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a90bee9e2979f80464b05a3f2891cc7d3cc8e1fa10fe33faefb7319940e321f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553400"
---
# <a name="pnrp-and-wsalookupservicebegin"></a>PNRP und WSALookupServiceBegin

PNRP verwendet die [**WSALookupServiceBegin-Funktion,**](winsock-nsp-reference-links.md) um den Prozess zu starten, der einer Anwendung folgende Aufgaben ermöglicht:

-   [Auflösen eines Namens](#resolving-a-name)
-   [Aufzählen von Netzwerk clouds](#enumerating-network-clouds)

Clients, die versuchen, eine der Funktionen auszuführen, verwenden die [**Funktionen WSALookupServiceBegin,**](winsock-nsp-reference-links.md) **WSALookupServiceNext** und **WSALookupServiceEnd.**

Mit [**WSANSPIoctl kann**](winsock-nsp-reference-links.md)der Suchdienst asynchron verwendet werden. Informationen zur asynchronen Verwendung der Suchdienstfunktionen finden Sie unter [PNRP und WSANSPIoctl](pnrp-and-wsanspioctl.md).

Der Prozess für die Arbeit mit Peernamen ist anders als bei der Arbeit mit Clouds. Jeder Prozess wird in diesem Thema separat beschrieben.

## <a name="resolving-a-name"></a>Auflösen eines Namens

Eine Anwendung verwendet [**WSALookupServiceBegin,**](winsock-nsp-reference-links.md) um die IP-Adresse, den Port und das Protokoll für einen Peerdienst zu erhalten, der auf einem anderen Computer registriert ist. Mit **der WSALookupServiceBegin-Funktion** wird der Namensauflösungsprozess gestartet und die Parameter und Einschränkungen eingerichtet. Ein Handle wird zurückgegeben und muss beim Aufrufen von **WSALookupServiceNext** und **WSANSPIoctl verwendet werden.**

### <a name="lpqsrestrictions"></a>lpqsRestrictions

Beim Auflösen eines Peernamens muss die [**LPWSAQUERYSET-Struktur,**](pnrp-and-wsaqueryset.md) auf die *die lpqsRestrictions-Parameterverweise* verweisen, die folgenden Werte enthalten:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe dieser -Struktur an.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Gibt einen aufzulösenden Peernamen an.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Muss **SVCID \_ PNRPNAME sein.**

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Reserviert, muss NULL **sein.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Reserviert, muss NULL **sein.**

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Muss entweder **NS \_ PNRPNAME oder** **NS \_ ALL sein.**

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Muss entweder **NS \_ PROVIDER \_ PNRPNAME oder** NULL **sein.**

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Muss ein Cloudname, eine leere Zeichenfolge oder **NULL sein.** Wenn dieser Wert **NULL oder** eine leere Zeichenfolge ist, wird die Standardwolke "Global" \_ verwendet. Andernfalls muss sie auf einen gültigen Cloudnamen verweisen.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Reserviert, muss 0 (null) sein.

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Reserviert, muss NULL **sein.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Reserviert, muss 0 (null) sein.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Reserviert, muss NULL **sein.**

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Reserviert, muss 0 (null) sein.

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Muss entweder ein Zeiger auf eine [**BLOB-Struktur**](winsock-nsp-reference-links.md) oder **NULL sein.** Wenn es NULL **ist,** werden Standardwerte verwendet. Wenn sie festgelegt ist, **verweist lpBlob** auf eine [**PNRPINFO-Struktur,**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) und bestimmte Parameter in der **PNRPINFO-Struktur** müssen festgelegt werden. Weitere Informationen finden Sie in den folgenden Beschreibungen für die PNRPINFO-Struktur.

</dd> </dl>

PNRPINFO-Struktur

Wenn das **lpBlob-Element** der [**LPWSAQUERYSET-Struktur**](pnrp-and-wsaqueryset.md) festgelegt ist, müssen die folgenden Member der [**PNRPINFO-Struktur**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) festgelegt werden:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe dieser -Struktur an.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**
</dt> <dd>

Reserviert, muss NULL **sein.**

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**
</dt> <dd>

Gibt die angeforderte Anzahl von Auflösungen an.

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**
</dt> <dd>

Gibt den angeforderten Timeoutzeitraum an, um auf Antworten zu warten. Der Standardwert ist 30 Sekunden. Der Höchstwert beträgt 600 Sekunden (10 Minuten).

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**
</dt> <dd>

Reserviert, muss 0 (null) sein.

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**
</dt> <dd>

Muss einer der zulässigen Werte sein. Der Standardwert ist **PNRP \_ RESOLVE CRITERIA NON CURRENT PROCESS PEER \_ \_ \_ \_ \_ \_ NAME**. Gültige Werte werden von [**PNRP \_ RESOLVE CRITERIA \_ angegeben.**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria)

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**Dwflags**
</dt> <dd>

Muss entweder null (0) oder **PNRPINFO \_ HINT sein.** Der Standardwert ist null (0).

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**
</dt> <dd>

Gibt die IP-Adresse für den Hinweis an. Der Hinweis wird verwendet, wenn versucht wird, den nächsten Peernamen zu finden. Das Format des Hinweises ist eine IPv6-Adresse. Wenn **saHint beim** Suchen des nächsten Peernamens nicht angegeben wird, wird stattdessen eine IPv6-Adresse des lokalen Computers verwendet. Dieser Member wird ignoriert, wenn **dwFlags** nicht festgelegt ist.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**
</dt> <dd>

Reserviert, muss 0 (null) sein.

</dd> </dl>

### <a name="dwcontrolflags"></a>dwControlFlags

Die folgenden \_ LUP-RÜCKGABEflags \_ \* werden von PNRP unterstützt:



| Wert                | Beschreibung                                |
|----------------------|--------------------------------------------|
| \_LUP-RÜCKGABENAME \_    | Gibt einen Namen und Kontext zurück.                |
| \_ \_ LUP-RÜCKGABEKOMMENTAR | Gibt einen Kommentar zurück, der einem Namen zugeordnet ist.  |
| \_ \_ LUP-RÜCKGABE-ADDR    | Gibt eine Adresse zurück, die einem Namen zugeordnet ist. |



 

## <a name="enumerating-network-clouds"></a>Aufzählen von Netzwerk clouds

### <a name="lpqsrestrictions"></a>lpqsRestrictions

Beim Aufzählen von Clouds muss die [**LPWSAQUERYSET-Struktur,**](pnrp-and-wsaqueryset.md) auf die *der lpqsRestrictions-Parameter* verweist, die folgenden Werte enthalten:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe dieser -Struktur an.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Muss NULL **sein.**

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Muss **SVCID \_ PNRPCLOUD sein.**

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Reserviert, muss NULL **sein.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Reserviert, muss **NULL** sein.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Muss **NS \_ PNRPCLOUD** sein.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Muss entweder **NS \_ PROVIDER \_ PNRPCLOUD** oder **NULL** sein.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Reserviert, muss **NULL** sein.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Reserviert, muss null (0) sein.

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Reserviert, muss **NULL** sein.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Reserviert, muss null (0) sein.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Reserviert, muss **NULL** sein.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Reserviert, muss null (0) sein.

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Zeiger auf eine [**BLOB-Struktur,**](winsock-nsp-reference-links.md) die auf eine [**PNRPCLOUDINFO-Struktur**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) zeigt. Wenn **lpBlob** **NULL** ist, werden alle Clouds aufzählt.

</dd> </dl>

PNRPCLOUDINFO-Struktur

Beim Aufzählen von Clouds müssen die folgenden Member der [**PNRPCLOUDINFO-Struktur**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) festgelegt werden:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe dieser Struktur an.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**
</dt> <dd>

Zeigt auf eine -Struktur, die Kriterien angibt, die Sie zum Filtern von Suchergebnissen verwenden können. Das **Cloud.Scope-Element** kann **PNRP \_ SCOPE \_ ANY,** **PNRP GLOBAL \_ \_ SCOPE,** **PNRP SITE LOCAL \_ \_ \_ SCOPE** oder **PNRP LINK LOCAL SCOPE \_ \_ \_ sein.** Wenn **PNRP \_ SCOPE \_ ANY** angegeben ist, werden alle Clouds zurückgegeben. Andernfalls werden nur Clouds zurückgegeben, die mit **Cloud.Scope** übereinstimmen.

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**
</dt> <dd>

Reserviert, muss null (0) sein.

</dd> </dl>

### <a name="dwcontrolflags"></a>dwControlFlags

Die folgenden LUP \_ \_ \* RETURN-Flags werden von PNRP unterstützt:



| Wert             | Beschreibung                                                       |
|-------------------|-------------------------------------------------------------------|
| \_LUP-RÜCKGABENAME \_ | Gibt einen Namen und Kontext zurück.                                       |
| \_ \_ LUP-RÜCKGABEBLOB | Gibt das [BLOB zurück,](pnrp-and-blob.md) das dieser Cloud zugeordnet ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PNRP und BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP und WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP und WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
</dt> <dt>

[PNRP und WSANSPIoctl](pnrp-and-wsanspioctl.md)
</dt> <dt>

[PNRP und WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[PNRP-NSP-Fehlercodes](pnrp-nsp-error-codes.md)
</dt> </dl>

 

 



