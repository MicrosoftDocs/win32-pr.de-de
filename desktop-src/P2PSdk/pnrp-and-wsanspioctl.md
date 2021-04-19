---
description: PNRP verwendet die wsanspioctl-Funktion, um Benachrichtigungen zu Änderungen an folgenden Informationen zu erhalten.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP und wsanspioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36dc53fb3d00eeaa2b74be643a7ea62af436e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349863"
---
# <a name="pnrp-and-wsanspioctl"></a>PNRP und wsanspioctl

PNRP verwendet die [**wsanspioctl**](winsock-nsp-reference-links.md) -Funktion, um Benachrichtigungen zu Änderungen an folgenden Informationen zu erhalten:

-   Eine netzwerkcloudliste
-   Verfügbarkeit der Ergebnisse einer namens Auflösungs Anforderung

Der erste [**wsalookupservicebegin**](winsock-nsp-reference-links.md) -Befehl definiert den Typ der Informationen, über die ein Client benachrichtigt wird. Ein Client kann mit einer Windows-Meldung, einer Abschluss Routine, einem Handle für ein wsaevent-Objekt oder einem Port benachrichtigt werden. Weitere Informationen zu Optionen und zum Festlegen des *lpcompletion* -Parameters finden Sie unter **wsanspioctl**.

Um nach einem [**WSALookupServiceNext**](winsock-nsp-reference-links.md)-Aufrufvorgang weiterhin Benachrichtigungen zu empfangen, muss eine Anwendung **wsanspioctl** erneut abrufen.

Die [**WSALookupServiceNext**](winsock-nsp-reference-links.md) -Funktion wird blockiert, auch wenn **wsanspioctl** aufgerufen wird. Vor dem Aufrufen von **WSALookupServiceNext** muss eine Anwendung warten, bis Sie eine Benachrichtigung erhält – Wenn die Blockierung ein Problem ist.

Wenn diese Funktion aufgerufen wird, müssen die Parameter die folgenden Werte aufweisen:

<dl> <dt>

<span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*HLOOKUP*
</dt> <dd>

Gibt das Handle an, das [**wsalookupservicebegin**](winsock-nsp-reference-links.md) zurückgibt.

</dd> <dt>

<span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwcontrolcode*
</dt> <dd>

Muss eine **\_ MSP- \_ Benachrichtigungs \_ Änderung** sein.

</dd> <dt>

<span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvinbuffer*
</dt> <dd>

Muss **null** sein.

</dd> <dt>

<span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbinbuffer*
</dt> <dd>

Muss NULL (0) sein.

</dd> <dt>

<span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvoutbuffer*
</dt> <dd>

Muss **null** sein.

</dd> <dt>

<span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cboutbuffer*
</dt> <dd>

Muss NULL (0) sein.

</dd> <dt>

<span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbbyteszurück gegeben*
</dt> <dd>

Muss **null** sein.

</dd> <dt>

<span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpcompletion*
</dt> <dd>

Gibt entweder **null** oder einen Zeiger auf eine [**wsacompletion**](winsock-nsp-reference-links.md) -Struktur an.

</dd> </dl>

Nachdem eine Benachrichtigung empfangen wurde, rufen Sie [**WSALookupServiceNext**](winsock-nsp-reference-links.md) einmal auf, um die Ergebnisse zu erhalten.

Um eine Suche zu beenden, nennen Sie [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).

## <a name="resolution-notifications"></a>Auflösungs Benachrichtigungen

Ein Client kann jederzeit benachrichtigt werden, wenn ein namens Auflösungs Eintrag hinzugefügt wird. Der Client ruft dann [**WSALookupServiceNext**](winsock-nsp-reference-links.md) auf, um die Auflösungs Daten zu erhalten.

Wenn der Client dieses Verfahren nicht verwendet, kann ein [**WSALookupServiceNext**](winsock-nsp-reference-links.md) -Aufrufe blockiert werden, bis das angegebene Timeout eintritt.

## <a name="cloud-list-notifications"></a>Benachrichtigungen in der cloudliste

Ein Client kann jederzeit benachrichtigt werden, wenn eine Gruppe von Clouds geändert wird.

Die [**WSALookupServiceNext**](winsock-nsp-reference-links.md) -Funktion gibt **WSA \_ E \_ nicht \_ mehr** als festgelegter Trennzeichen zurück. Die Client Anwendung muss vorhandene Clouds aufzählen, bis diese Nachricht zurückgegeben wird, und dann ein Benachrichtigungs Schema verwenden, um nachfolgende Änderungen abzurufen. Eine Client Anwendung kann auch **WSALookupServiceNext** anrufen, aber der-Befehl wird blockiert, bis eine Änderung auftritt.

Die [**WSALookupServiceNext**](winsock-nsp-reference-links.md) -Funktion gibt eine Cloud in einer **wsaqueryset** -Struktur zurück. Eines der folgenden Flags wird im **dwoutputflags** -Member zurückgegeben.



| Wert               | BESCHREIBUNG                                             |
|---------------------|---------------------------------------------------------|
| Ergebnis \_ wird \_ hinzugefügt   | Die zurückgegebene Cloud wird hinzugefügt.                    |
| Ergebnis \_ wurde \_ geändert | Die zurückgegebene Cloud wird geändert.                  |
| Das Ergebnis \_ ist \_ gelöscht. | Die zurückgegebene Cloud wird gelöscht und ist ungültig. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PNRP und wsalookupservicebegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[PNRP und WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP und wsaqueryset](pnrp-and-wsaqueryset.md)
</dt> <dt>

[PNRP-NSP-Fehler Codes](pnrp-nsp-error-codes.md)
</dt> <dt>

[**Wsanspioctl**](winsock-nsp-reference-links.md)
</dt> <dt>

**Wsalookupservicebegin**
</dt> <dt>

**WSALookupServiceEnd**
</dt> <dt>

**Wsaqueryset**
</dt> </dl>

 

 



