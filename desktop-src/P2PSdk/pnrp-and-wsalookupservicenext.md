---
description: PNRP verwendet die WSALookupServiceNext-Funktion, um Abfragen abzugleichen, die in einem vorherigen wsalookupservicebegin-Befehl angegeben wurden.
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP und WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398beca2f16e4920ab7fbe43bb648cbc22d9f336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367944"
---
# <a name="pnrp-and-wsalookupservicenext"></a>PNRP und WSALookupServiceNext

PNRP verwendet die [**WSALookupServiceNext**](winsock-nsp-reference-links.md) -Funktion, um Abfragen abzugleichen, die in einem vorherigen **wsalookupservicebegin**-Befehl angegeben wurden. Die Ergebnisse der **WSALookupServiceNext** -Funktion werden durch Einstellungen in der **wsaqueryset** -Struktur festgelegt, die im anfänglichen **wsalookupservicebegin** -Funktions aufruft übergeben werden. Diese Funktion wird verwendet, um die folgenden zwei Funktionen auszuführen:

-   Auflösen eines Peer namens in eine Liste von Adressen
-   Auflisten von Netzwerk Clouds

Mithilfe von [**wsanspioctl**](winsock-nsp-reference-links.md)kann der Suchdienst asynchron verwendet werden. Weitere Informationen zur asynchronen Verwendung der Suche-Dienstfunktionen finden Sie unter [PNRP und wsanspioctl](pnrp-and-wsanspioctl.md).

Die [**WSALookupServiceNext**](winsock-nsp-reference-links.md) -Funktion wird blockiert, auch wenn **wsanspioctl** aufgerufen wird. Vor dem Aufrufen von **WSALookupServiceNext** muss eine Anwendung warten, bis Sie eine Benachrichtigung erhält – Wenn die Blockierung ein Problem ist.

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a>Auflösen eines Peer namens in eine Liste von Adressen

Beim Auflösen eines Peer namens in eine Liste von Adressen enthält die im *lpqsresults* -Parameter zurückgegebene [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur die folgenden Werte:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe der-Struktur zurück.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszserviceingestancename**
</dt> <dd>

Gibt einen Peernamen zurück – wenn ein **luprückgabetame \_ \_**, eine **Lup \_ Return \_ all** oder **null** angegeben ist.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpserviceclassid**
</dt> <dd>

Gibt **svcid \_ pnrpname** zurück.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpversion**
</dt> <dd>

Gibt **null** zurück.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszcomment**
</dt> <dd>

Gibt einen Kommentar zurück – wenn ein **luprückgabetcomment \_ \_**, eine **Lup \_ Return \_ all** oder **null** angegeben wird.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwnamespace**
</dt> <dd>

Gibt **NS \_ pnrpname** zurück.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpnsproviderid**
</dt> <dd>

Gibt den **NS- \_ Anbieter \_ pnrpname** zurück.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszcontext**
</dt> <dd>

Gibt den cloudnamen zurück, wenn der **\_ Rückgabe \_ Name** des PPS, die **Lup- \_ Rückgabe \_ all** oder **null** angegeben ist.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwnumofprotokolle**
</dt> <dd>

Gibt 0 (null) zurück.

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszquerystring**
</dt> <dd>

Gibt **null** zurück.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwnumofcsaddrs**
</dt> <dd>

Gibt die Anzahl der Einträge im csaddr- \_ Informations Array zurück, wenn " **Lup \_ Return \_ addr**", " **Lup \_ Return \_ all**" oder " **null** " angegeben wird. Dieser Wert und die Informationen in **lpcsabuffer** sind die Schlüssel Bits der Informationen, die in dieser Struktur zurückgegeben werden.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsabuffer**
</dt> <dd>

Gibt einen Zeiger auf ein Array von csaddr- \_ Informationsstrukturen zurück, wenn " **Lup \_ Return \_ addr**", " **Lup \_ Return \_ all**" oder " **null** " angegeben wird. Dieser Puffer und der Wert in **dwnumofcsaddrs** sind die wichtigsten Informations Bits, die in dieser Struktur zurückgegeben werden.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwoutputflags**
</dt> <dd>

Gibt 0 (null) zurück.

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpblob**
</dt> <dd>

Gibt **null** zurück.

</dd> </dl>

## <a name="enumerating-network-clouds"></a>Auflisten von Netzwerk Clouds

Beim Auflisten von Clouds enthält die im *lpqsresults* -Parameter zurückgegebene [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur die folgenden Werte:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe der-Struktur zurück.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszserviceingestancename**
</dt> <dd>

Gibt einen cloudnamen zurück – wenn der **\_ Rückgabe \_ Name** des PPS, die **Lup- \_ Rückgabe \_ all** oder **null** angegeben ist.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpserviceclassid**
</dt> <dd>

Gibt **svcid \_ pnrpcloud** zurück.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpversion**
</dt> <dd>

Gibt **null** zurück.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszcomment**
</dt> <dd>

Gibt **null** zurück.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwnamespace**
</dt> <dd>

Gibt **NS \_ pnrpcloud** zurück.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpnsproviderid**
</dt> <dd>

Gibt den **NS- \_ Anbieter \_ pnrpcloud** zurück.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszcontext**
</dt> <dd>

Gibt **null** zurück.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwnumofprotokolle**
</dt> <dd>

Gibt 0 (null) zurück.

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszquerystring**
</dt> <dd>

Gibt **null** zurück.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwnumofcsaddrs**
</dt> <dd>

Gibt 0 (null) zurück.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsabuffer**
</dt> <dd>

Gibt **null** zurück.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwoutputflags**
</dt> <dd>

Gibt 0 (null) zurück.

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpblob**
</dt> <dd>

Gibt einen Zeiger auf eine [**BLOB**](winsock-nsp-reference-links.md) -Struktur zurück, die auf eine [**pnrpcloudinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) -Struktur zeigt – Wenn ein **luprückgabeblob \_ \_**, eine **Lup \_ Return \_ all** oder **null** angegeben wird.

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a>Pnrpcloudinfo-Struktur

Beim Auflisten von cloudnamen werden die folgenden Werte in der [**pnrpcloudinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) -Struktur zurückgegeben:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Die Größe dieser Struktur.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**
</dt> <dd>

Der tatsächliche cloudwert.

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**umcloudstate**
</dt> <dd>

Der aktuelle Zustand einer Cloud. [**PNRP \_ Der \_ cloudstatus**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) gibt die gültigen Werte an.

</dd> <dt>

<span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**encloudflags**
</dt> <dd>

Gibt an, dass ein cloudName in einem Netzwerk oder nur auf einem aktuellen Computer gültig ist. [**PNRP \_ Cloud- \_ Flags**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) gibt die gültigen Werte an. Einige cloudnamen sind auf einem beliebigen Computer im selben Netzwerk gültig. Andere cloudnamen gelten nur auf einem aktuellen Computer und sind möglicherweise nur für einen bestimmten Zeitraum gültig.

-   Wenn " **encloudflags** " auf " **PNRP \_ Cloud \_ Name \_ local** " festgelegt ist, ist der Name nur lokal gültig.
-   Wenn **encloudflags** nicht festgelegt ist, kann der cloudName an andere Computer übertragen werden.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PNRP und BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP und WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP und wsanspioctl](pnrp-and-wsanspioctl.md)
</dt> <dt>

[PNRP und wsaqueryset](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**Pnrpcloudinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[**Pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[PNRP-NSP-Fehler Codes](pnrp-nsp-error-codes.md)
</dt> <dt>

[**Wsalookupservicebegin**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



