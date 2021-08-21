---
description: PNRP verwendet die WSALookupServiceNext-Funktion, um Abfragen zu erfüllen, die in einem vorherigen Aufruf von WSALookupServiceBegin angegeben wurden.
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP und WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ec10c8021a2f13be1a1ffe228ca73a07c8af10dfc8714bef14f0bddeb0952aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553320"
---
# <a name="pnrp-and-wsalookupservicenext"></a>PNRP und WSALookupServiceNext

PNRP verwendet die [**WSALookupServiceNext-Funktion,**](winsock-nsp-reference-links.md) um Abfragen zu erfüllen, die in einem vorherigen Aufruf von **WSALookupServiceBegin angegeben wurden.** Die Ergebnisse der **WSALookupServiceNext-Funktion** werden durch Einstellungen in der **WSAQUERYSET-Struktur** bestimmt, die im ersten **WSALookupServiceBegin-Funktionsaufruf** übergeben werden. Diese Funktion wird verwendet, um die folgenden beiden Funktionen auszuführen:

-   Auflösen eines Peernamens in eine Liste von Adressen
-   Aufzählen von Netzwerk clouds

Mit [**WSANSPIoctl kann**](winsock-nsp-reference-links.md)der Suchdienst asynchron verwendet werden. Informationen zur asynchronen Verwendung der Suchdienstfunktionen finden Sie unter [PNRP und WSANSPIoctl](pnrp-and-wsanspioctl.md).

Die [**WSALookupServiceNext-Funktion**](winsock-nsp-reference-links.md) blockiert auch dann, wenn **WSANSPIoctl** aufgerufen wird. Vor dem **Aufruf von WSALookupServiceNext** muss eine Anwendung warten, bis sie eine Benachrichtigung empfängt– wenn die Blockierung ein Problem ist.

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a>Auflösen eines Peernamens in eine Liste von Adressen

Beim Auflösen eines Peernamens in eine Liste von Adressen enthält die im *lpqsResults-Parameter* zurückgegebene [**LPWSAQUERYSET-Struktur**](pnrp-and-wsaqueryset.md) die folgenden Werte:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe der -Struktur zurück.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Gibt einen Peernamen zurück, wenn **LUP \_ RETURN \_ NAME,** **LUP \_ RETURN \_ ALL** oder **NULL** angegeben sind.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Gibt **SVCID \_ PNRPNAME zurück.**

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Gibt **NULL zurück.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Gibt einen Kommentar zurück– wenn **LUP \_ RETURN \_ COMMENT,** **LUP \_ RETURN \_ ALL** oder **NULL** angegeben sind.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Gibt **NS \_ PNRPNAME zurück.**

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Gibt **NS \_ PROVIDER \_ PNRPNAME zurück.**

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Gibt den Cloudnamen zurück, **wenn LUP \_ RETURN \_ NAME,** **LUP RETURN \_ \_ ALL** oder **NULL** angegeben sind.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Gibt null (0) zurück.

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Gibt **NULL zurück.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Gibt die Anzahl der Einträge im ARRAY CSADDR INFO zurück, wenn \_ **LUP \_ RETURN \_ ADDR,** **LUP \_ RETURN \_ ALL** oder **NULL** angegeben sind. Dieser Wert und die Informationen in **lpcsaBuffer** sind die wichtigsten Informationen, die in dieser Struktur zurückgegeben werden.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Gibt einen Zeiger auf ein Array von CSADDR INFO-Strukturen zurück, wenn \_ **LUP \_ RETURN \_ ADDR,** **LUP RETURN \_ \_ ALL** oder **NULL** angegeben sind. Dieser Puffer und der Wert in **dwNumberOfCsAddrs** sind die Schlüsselinformationsbits, die in dieser Struktur zurückgegeben werden.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Gibt null (0) zurück.

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Gibt **NULL zurück.**

</dd> </dl>

## <a name="enumerating-network-clouds"></a>Aufzählen von Netzwerk clouds

Beim Aufzählen von Clouds enthält die im *lpqsResults-Parameter* zurückgegebene [**LPWSAQUERYSET-Struktur**](pnrp-and-wsaqueryset.md) die folgenden Werte:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe der -Struktur zurück.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Gibt einen Cloudnamen zurück– wenn **LUP \_ RETURN \_ NAME,** **LUP \_ RETURN \_ ALL** oder **NULL** angegeben sind.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Gibt **SVCID \_ PNRPCLOUD zurück.**

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Gibt **NULL zurück.**

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Gibt **NULL zurück.**

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Gibt **NS \_ PNRPCLOUD zurück.**

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Gibt **NS \_ PROVIDER \_ PNRPCLOUD zurück.**

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Gibt **NULL zurück.**

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Gibt null (0) zurück.

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Gibt **NULL zurück.**

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Gibt null (0) zurück.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Gibt **NULL zurück.**

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Gibt null (0) zurück.

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Gibt einen Zeiger auf eine [**BLOB-Struktur**](winsock-nsp-reference-links.md) zurück, die auf eine [**PNRPCLOUDINFO-Struktur**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) verweist– wenn **LUP \_ RETURN \_ BLOB,** **LUP \_ RETURN \_ ALL** oder **NULL** angegeben sind.

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a>PNRPCLOUDINFO-Struktur

Beim Aufzählen von Cloudnamen werden die folgenden Werte in der [**PNRPCLOUDINFO-Struktur**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) zurückgegeben:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Die Größe dieser Struktur.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**
</dt> <dd>

Der tatsächliche Cloudwert.

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**
</dt> <dd>

Der aktuelle Zustand einer Cloud. [**PNRP \_ CLOUD \_ STATE**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) gibt die gültigen Werte an.

</dd> <dt>

<span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**
</dt> <dd>

Gibt an, dass ein Cloudname in einem Netzwerk oder nur auf einem aktuellen Computer gültig ist. [**PNRP \_ CLOUD \_ FLAGS**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) gibt die gültigen Werte an. Einige Cloudnamen sind auf jedem Computer im gleichen Netzwerk gültig. Andere Cloudnamen sind nur auf einem aktuellen Computer gültig und können nur für einen bestimmten Zeitraum gültig sein.

-   Wenn **enCloudFlags** auf PNRP CLOUD NAME LOCAL festgelegt **\_ \_ \_ ist,** ist der Name nur lokal gültig.
-   Wenn **enCloudFlags** nicht festgelegt ist, kann der Cloudname auf andere Computer übertragen werden.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PNRP und BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP und WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
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
</dt> <dt>

[**WSALookupServiceBegin**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



