---
title: Bluetooth und WSASetService
description: Bluetooth verwendet die WSASetService-Funktion, um eine Dienstinstanz innerhalb des Bluetooth-Namespace (NS BTH) in der \_ Registrierung zu registrieren oder zu entfernen.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- WSASetService-Bluetooth
- Bluetooth und WSASetService Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671e43636de67cee1e1c3c945a3647b5db59e7b0dd22b6eefd70b51f4977c31e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004170"
---
# <a name="bluetooth-and-wsasetservice"></a>Bluetooth und WSASetService

Bluetooth verwendet die [**WSASetService-Funktion,**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) um eine Dienstinstanz im Bluetooth-Namespace (NS BTH) in der \_ Registrierung zu registrieren oder zu entfernen. Das von diesem Vorgang zurückgegebene Handle kann nur zum Löschen des Diensts verwendet werden.

Bluetooth bietet zwei Möglichkeiten, Dienste mithilfe der [**WSASetService-Funktion zu**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) werben:

-   Für die Anwendung kann das System einen einfachen Bluetooth SDP-Dienstdatensatz ankregen, der aus Standardmitgliedern in der [**WSAQUERYSET-Struktur erstellt**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) wird.
-   Die Anwendung kann festlegen, dass das System seinen eigenen SDP Bluetooth datensatz anklädt, indem eine [**BTH \_ SET \_ SERVICE-Struktur**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) im **lpBlob-Member** der [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) übergeben wird. Dies ist ein komplexerer Ansatz.

> [!Note]  
> Von [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) angekündigte SDP-Datensätze werden nach dem Beenden des Prozesses, der sie veröffentlicht hat, nicht beibehalten.

 

Die Verwendung [**von WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) mit Bluetooth erfüllt die folgenden Anforderungen:

-   Der *lpqsRegInfo-Parameter* ist die Adresse der [**WSAQUERYSET-Struktur,**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) die registriert werden soll.
-   Der *essOperation-Parameter* ist eine Enumeration, die einen der in der folgenden Tabelle gezeigten Vorgänge enthält.



| Wert                  | Beschreibung                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| RNRSERVICE \_ REGISTER   | Startet die Ankundung des Diensts für Remote-Radios, die abfragen, Bluetooth SDP-Protokoll verwenden. |
| RNRSERVICE \_ DEREGISTER | Ungültig. Gibt einen Fehler zurück.                                                               |
| RNRSERVICE \_ DELETE     | Beendet die Werbung für den Dienst.                                                             |



 

> [!Note]  
> Diensthandles, die während eines [**WSALookupServiceBegin-**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) oder [**WSALookupServiceNext-Aufrufs**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) gefunden wurden, sind nicht mit dem RNRSERVICE \_ DELETE-Vorgang kompatibel.

 

-   Der *dwControlFlags-Parameter* ist reserviert und muss 0 (null) sein.

Weitere Informationen und eine Liste der Socketoptionen Bluetooth finden Sie unter Bluetooth [und Socketoptionen.](bluetooth-and-socket-options.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 