---
title: Bluetooth und wsasetservice
description: Bluetooth verwendet die wsasetservice-Funktion, um eine Dienst Instanz im Bluetooth-Namespace (NS \_ BTH) aus der Registrierung zu registrieren oder zu entfernen.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- Wsasetservice Bluetooth
- Bluetooth und wsasetservice Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473245"
---
# <a name="bluetooth-and-wsasetservice"></a>Bluetooth und wsasetservice

Bluetooth verwendet die [**wsasetservice**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) -Funktion, um eine Dienst Instanz im Bluetooth-Namespace (NS \_ BTH) aus der Registrierung zu registrieren oder zu entfernen. Das Handle, das von diesem Vorgang zurückgegeben wird, kann nur verwendet werden, um den Dienst zu löschen.

Bluetooth bietet zwei Möglichkeiten, Dienste mithilfe der [**wsasetservice**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) -Funktion zu bewerben:

-   Die Anwendung kann das System einen einfachen Bluetooth-SDP-Dienst Eintrag ankündigen, der aus Standard Mitgliedern in der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur erstellt wird.
-   Die Anwendung kann das System einen eigenen Bluetooth-SDP-Datensatz ankündigen, indem er eine [**BTH- \_ Set- \_ Service**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) -Struktur im **lpblob** -Member der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur übergibt. Dies ist ein komplexerer Ansatz.

> [!Note]  
> SDP-Datensätze, die von [**wsasetservice**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) angekündigt werden, werden nicht beibehalten, nachdem der von Ihnen veröffentlichte Prozess beendet wurde.

 

Die Verwendung von [**wsasetservice**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) mit Bluetooth hat die folgenden Anforderungen:

-   Der *lpqsreginfo* -Parameter ist die Adresse der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur, die registriert werden soll.
-   Der *ESS Operation* -Parameter ist eine Enumeration, die einen der in der folgenden Tabelle gezeigten Vorgänge enthält.



| Wert                  | BESCHREIBUNG                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| rnrservice- \_ Registrierung   | Startet die Ankündigung des dienstanterdienstanbieter mit dem Bluetooth-SDP-Protokoll. |
| rnrservice \_ -Registrierung | Ungültig. Gibt einen Fehler zurück.                                                               |
| rnrservice \_ Löschen     | Beendet die Ankündigung des Dienstanbieter.                                                             |



 

> [!Note]  
> Dienst Handles, die während eines [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -oder [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Aufrufes erkannt werden, sind mit dem Löschvorgang rnrservice nicht kompatibel \_ .

 

-   Der *dwcontrolflags* -Parameter ist reserviert und muss NULL sein.

Weitere Informationen und eine Liste der Optionen für Bluetooth-Sockets finden Sie unter [Optionen für Bluetooth und Socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 