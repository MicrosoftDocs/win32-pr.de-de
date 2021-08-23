---
description: PNRP verwendet die WSANSPIoctl-Funktion, um Benachrichtigungen zu Folgendenänderungen zu erhalten.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP und WSANSPIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cc07415fb483e75af8d836274d45a2c53f205e3aae15f893f909d2363c0d15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553310"
---
# <a name="pnrp-and-wsanspioctl"></a>PNRP und WSANSPIoctl

PNRP verwendet die [**WSANSPIoctl-Funktion,**](winsock-nsp-reference-links.md) um Benachrichtigungen zu Änderungen an Folgenden zu erhalten:

-   Liste der Netzwerkclouds
-   Verfügbarkeit der Ergebnisse einer Namensauflösungsanforderung

Der erste Aufruf von [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) definiert den Informationstyp, über den ein Client benachrichtigt wird. Ein Client kann mit einer Windows Nachricht, einer Abschlussroutine, einem Handle für ein WSAEVENT-Objekt oder einem Port benachrichtigt werden. Weitere Informationen zu Optionen und zum Festlegen des *lpCompletion-Parameters* finden Sie unter **WSANSPIoctl.**

Um nach einem Aufruf von [**WSALookupServiceNext**](winsock-nsp-reference-links.md)weiterhin Benachrichtigungen zu erhalten, muss eine Anwendung **WSANSPIoctl** erneut aufrufen.

Die [**WSALookupServiceNext-Funktion**](winsock-nsp-reference-links.md) blockiert auch dann, wenn **WSANSPIoctl** aufgerufen wird. Vor dem Aufrufen von **WSALookupServiceNext** muss eine Anwendung warten, bis sie eine Benachrichtigung empfängt– wenn die Blockierung ein Problem ist.

Beim Aufrufen dieser Funktion müssen die Parameter die folgenden Werte aufweisen:

<dl> <dt>

<span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*Wverweis*
</dt> <dd>

Gibt das Handle an, das [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) zurückgibt.

</dd> <dt>

<span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*
</dt> <dd>

Muss **SIO \_ NSP \_ NOTIFY \_ CHANGE** sein.

</dd> <dt>

<span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*
</dt> <dd>

Muss **NULL** sein.

</dd> <dt>

<span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*
</dt> <dd>

Muss 0 (null) sein.

</dd> <dt>

<span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*
</dt> <dd>

Muss **NULL** sein.

</dd> <dt>

<span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*
</dt> <dd>

Muss 0 (null) sein.

</dd> <dt>

<span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*
</dt> <dd>

Muss **NULL** sein.

</dd> <dt>

<span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*
</dt> <dd>

Gibt entweder **NULL** oder einen Zeiger auf eine [**WSACOMPLETION-Struktur**](winsock-nsp-reference-links.md) an.

</dd> </dl>

Nachdem eine Benachrichtigung empfangen wurde, rufen Sie [**WSALookupServiceNext**](winsock-nsp-reference-links.md) einmal auf, um die Ergebnisse abzurufen.

Um eine Suche zu beenden, rufen Sie [**WSALookupServiceEnd auf.**](winsock-nsp-reference-links.md)

## <a name="resolution-notifications"></a>Auflösungsbenachrichtigungen

Ein Client kann jederzeit benachrichtigt werden, wenn ein Namensauflösungseintrag hinzugefügt wird. Der Client ruft dann [**WSALookupServiceNext**](winsock-nsp-reference-links.md) auf, um die Auflösungsdaten abzurufen.

Wenn der Client diese Technik nicht verwendet, kann ein Aufruf von [**WSALookupServiceNext**](winsock-nsp-reference-links.md) blockiert werden, bis das angegebene Timeout auftritt.

## <a name="cloud-list-notifications"></a>Cloudlistenbenachrichtigungen

Ein Client kann bei jeder Änderung an einer Gruppe von Clouds benachrichtigt werden.

Die [**WSALookupServiceNext-Funktion**](winsock-nsp-reference-links.md) gibt **WSA \_ E NO \_ \_ MORE** als Set-Trennzeichen zurück. Die Clientanwendung muss vorhandene Clouds aufzählen, bis diese Nachricht zurückgegeben wird, und dann ein Benachrichtigungsschema verwenden, um nachfolgende Änderungen abzurufen, sobald sie auftreten. Eine Clientanwendung kann auch **WSALookupServiceNext** aufrufen, aber der Aufruf wird blockiert, bis eine Änderung erfolgt.

Die [**WSALookupServiceNext-Funktion**](winsock-nsp-reference-links.md) gibt eine Cloud in einer **WSAQUERYSET-Struktur** zurück. Eines der folgenden Flags wird im **dwOutputFlags-Member** zurückgegeben.



| Wert               | Beschreibung                                             |
|---------------------|---------------------------------------------------------|
| ERGEBNIS \_ \_ HINZUGEFÜGT   | Die zurückgegebene Cloud wird hinzugefügt.                    |
| ERGEBNIS \_ \_ GEÄNDERT | Die zurückgegebene Cloud wird geändert.                  |
| ERGEBNIS \_ WIRD \_ GELÖSCHT | Die zurückgegebene Cloud wird gelöscht und ist ungültig. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PNRP und WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[PNRP und WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP und WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[PNRP-NSP-Fehlercodes](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSANSPIoctl**](winsock-nsp-reference-links.md)
</dt> <dt>

**WSALookupServiceBegin**
</dt> <dt>

**WSALookupServiceEnd**
</dt> <dt>

**WSAQUERYSET**
</dt> </dl>

 

 



