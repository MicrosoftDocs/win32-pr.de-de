---
description: PNRP verwendet die wsalookupservicebegin-Funktion, um den Prozess zu starten, mit dem eine Anwendung folgende Aktionen ausführen kann.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP und wsalookupservicebegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78efd0ee28284cb41866795aea8a2a8d5f17e871
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106354344"
---
# <a name="pnrp-and-wsalookupservicebegin"></a>PNRP und wsalookupservicebegin

PNRP verwendet die [**wsalookupservicebegin**](winsock-nsp-reference-links.md) -Funktion, um den Prozess zu starten, mit dem eine Anwendung folgende Aktionen ausführen kann:

-   [Auflösen eines Namens](#resolving-a-name)
-   [Auflisten von Netzwerk Clouds](#enumerating-network-clouds)

Clients, die versuchen, eine der Funktionen auszuführen, verwenden die Funktionen [**wsalookupservicebegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext** und **WSALookupServiceEnd** .

Mithilfe von [**wsanspioctl**](winsock-nsp-reference-links.md)kann der Suchdienst asynchron verwendet werden. Weitere Informationen zur asynchronen Verwendung der Suche-Dienstfunktionen finden Sie unter [PNRP und wsanspioctl](pnrp-and-wsanspioctl.md).

Der Prozess zum Arbeiten mit Peernamen unterscheidet sich von der Arbeit mit Clouds. Jeder Prozess wird in diesem Thema separat beschrieben.

## <a name="resolving-a-name"></a>Auflösen eines Namens

Die IP-Adresse, der Port und das Protokoll für einen Peer Dienst, der auf einem anderen Computer registriert ist, werden von einer Anwendung mithilfe von [**wsalookupservicebegin**](winsock-nsp-reference-links.md) abgerufen. Die **wsalookupservicebegin** -Funktion wird verwendet, um den namens Auflösungsprozess zu starten und die Parameter und Einschränkungen einzurichten. Ein Handle wird zurückgegeben und muss beim Aufrufen von **WSALookupServiceNext** und **wsanspioctl** verwendet werden.

### <a name="lpqsrestrictions"></a>lpqsrestrictions

Beim Auflösen eines Peer namens muss die [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur, auf die der *lpqsrestrictions* -Parameter verweist, die folgenden Werte enthalten:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe der-Struktur an.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszserviceingestancename**
</dt> <dd>

Gibt einen aufzulösenden Peernamen an.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpserviceclassid**
</dt> <dd>

Muss " **svcid \_ pnrpname**" lauten.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpversion**
</dt> <dd>

Reserviert, muss **null** sein.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszcomment**
</dt> <dd>

Reserviert, muss **null** sein.

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

Muss ein cloudName, eine leere Zeichenfolge oder **null** sein. Wenn dieser Wert **null** oder eine leere Zeichenfolge ist, wird die Standard-Cloud "Global \_ " verwendet. Andernfalls muss Sie auf einen gültigen cloudnamen verweisen.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwnumofprotokolle**
</dt> <dd>

Reserviert, muss NULL (0) sein.

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszquerystring**
</dt> <dd>

Reserviert, muss **null** sein.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwnumofcsaddrs**
</dt> <dd>

Reserviert, muss NULL (0) sein.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsabuffer**
</dt> <dd>

Reserviert, muss **null** sein.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwoutputflags**
</dt> <dd>

Reserviert, muss NULL (0) sein.

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpblob**
</dt> <dd>

Muss entweder ein Zeiger auf eine [**BLOB**](winsock-nsp-reference-links.md) -Struktur oder **null** sein. Wenn er **null** ist, werden Standardwerte verwendet. Wenn Sie festgelegt ist, verweist **lpblob** auf eine [**pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) -Struktur, und bestimmte Parameter in der **pnrpinfo** -Struktur müssen festgelegt werden. Weitere Informationen finden Sie in den folgenden Beschreibungen der pnrpinfo-Struktur.

</dd> </dl>

Pnrpinfo-Struktur

Wenn das **lpblob** -Element der [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur festgelegt ist, müssen die folgenden Member der [**pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) -Struktur festgelegt werden:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe der-Struktur an.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszidentity**
</dt> <dd>

Reserviert, muss **null** sein.

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nmaxresolve**
</dt> <dd>

Gibt die angeforderte Anzahl von Auflösungen an.

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwtimeout**
</dt> <dd>

Gibt den angeforderten Timeout Zeitraum an, der auf Antworten gewartet werden soll. Der Standardwert ist 30 Sekunden. Der Höchstwert beträgt 600 Sekunden (10 Minuten).

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwlifetime**
</dt> <dd>

Reserviert, muss NULL (0) sein.

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**einlösungs Vektor**
</dt> <dd>

Muss einer der zulässigen Werte sein. Der Standardwert ist **PNRP \_ Auflösungs \_ Kriterien \_ nicht \_ aktueller \_ Prozess \_ Peer \_ Name**. Gültige Werte werden von [**PNRP- \_ Auflösungs \_ Kriterien**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria)angegeben.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**
</dt> <dd>

Muss entweder NULL (0) oder **pnrpinfo- \_ Hinweis** sein. Der Standardwert ist null (0).

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**sahint**
</dt> <dd>

Gibt die IP-Adresse für den Hinweis an. Der Hinweis wird verwendet, wenn versucht wird, den nächsten Peernamen zu suchen. Das Format des Hinweises ist eine IPv6-Adresse. Wenn bei der Suche nach dem nächstgelegenen Peernamen **sahint** nicht angegeben wird, wird stattdessen eine IPv6-Adresse des lokalen Computers verwendet. Dieser Member wird ignoriert, wenn **dwFlags** nicht festgelegt ist.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**ennamestate**
</dt> <dd>

Reserviert, muss NULL (0) sein.

</dd> </dl>

### <a name="dwcontrolflags"></a>dwcontrolflags

Die folgenden Lup \_ - \_ \* rückgabeflags werden von PNRP unterstützt:



| Wert                | BESCHREIBUNG                                |
|----------------------|--------------------------------------------|
| Name der Lup- \_ Rückgabe \_    | Gibt einen Namen und einen Kontext zurück.                |
| Lup- \_ Rückgabe \_ Kommentar | Gibt einen Kommentar zurück, der einem Namen zugeordnet ist.  |
| Lup \_ Return \_ addr    | Gibt eine Adresse zurück, die einem Namen zugeordnet ist. |



 

## <a name="enumerating-network-clouds"></a>Auflisten von Netzwerk Clouds

### <a name="lpqsrestrictions"></a>lpqsrestrictions

Beim Auflisten von Clouds muss die [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur, auf die der *lpqsrestrictions* -Parameter verweist, die folgenden Werte enthalten:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe der-Struktur an.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszserviceingestancename**
</dt> <dd>

Muss **null** sein.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpserviceclassid**
</dt> <dd>

Muss **svcid \_ pnrpcloud** sein.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpversion**
</dt> <dd>

Reserviert, muss **null** sein.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszcomment**
</dt> <dd>

Reserviert, muss **null** sein.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwnamespace**
</dt> <dd>

Muss **NS \_ pnrpcloud** sein.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpnsproviderid**
</dt> <dd>

Muss entweder der **NS- \_ Anbieter \_ pnrpcloud** oder **null** sein.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszcontext**
</dt> <dd>

Reserviert, muss **null** sein.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwnumofprotokolle**
</dt> <dd>

Reserviert, muss NULL (0) sein.

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszquerystring**
</dt> <dd>

Reserviert, muss **null** sein.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwnumofcsaddrs**
</dt> <dd>

Reserviert, muss NULL (0) sein.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsabuffer**
</dt> <dd>

Reserviert, muss **null** sein.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwoutputflags**
</dt> <dd>

Reserviert, muss NULL (0) sein.

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpblob**
</dt> <dd>

Zeiger auf eine [**BLOB**](winsock-nsp-reference-links.md) -Struktur, die auf eine [**pnrpcloudinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) -Struktur zeigt. Wenn **lpblob** den Wert **null** hat, werden alle Clouds aufgelistet.

</dd> </dl>

Pnrpcloudinfo-Struktur

Beim Auflisten von Clouds müssen die folgenden Member der [**pnrpcloudinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) -Struktur festgelegt werden:

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

Gibt die Größe der-Struktur an.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**
</dt> <dd>

Verweist auf eine-Struktur, die Kriterien angibt, die Sie zum Filtern von Suchergebnissen verwenden können. Das Element **Cloud. Scope** kann den **PNRP \_ -Bereich \_ any**, den **globalen PNRP- \_ \_ Bereich**, den **lokalen PNRP- \_ Standort \_ \_ Bereich** oder den **lokalen PNRP- \_ Link \_ \_** aufweisen. Wenn **PNRP- \_ Bereich \_ any** angegeben ist, werden alle Clouds zurückgegeben. Andernfalls werden nur Clouds zurückgegeben, die dem **Cloud. Scope** entsprechen.

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**umcloudstate**
</dt> <dd>

Reserviert, muss NULL (0) sein.

</dd> </dl>

### <a name="dwcontrolflags"></a>dwcontrolflags

Die folgenden Lup \_ - \_ \* rückgabeflags werden von PNRP unterstützt:



| Wert             | BESCHREIBUNG                                                       |
|-------------------|-------------------------------------------------------------------|
| Name der Lup- \_ Rückgabe \_ | Gibt einen Namen und einen Kontext zurück.                                       |
| Lup- \_ Rückgabe- \_ BLOB | Gibt das [BLOB](pnrp-and-blob.md) zurück, das dieser Cloud zugeordnet ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PNRP und BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP und WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP und WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
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
</dt> </dl>

 

 



