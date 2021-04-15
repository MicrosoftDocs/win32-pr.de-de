---
title: Informationen zu RAS-Verwaltungs-DLLs
description: Die RAS-Verwaltungs-dll exportiert Funktionen, die der RAS-Server aufruft, wenn ein Benutzer versucht, eine Verbindung herzustellen oder diese zu trennen
ms.assetid: c15c6e2d-3bb6-4583-9ac3-19528feb863f
keywords:
- RAS-Administration-RRAS, RAS-Verwaltungs-dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb170e8cfa331ab9591aa509772c6f6a743fa49
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104516532"
---
# <a name="about-ras-administration-dlls"></a>Informationen zu RAS-Verwaltungs-DLLs

Die RAS-Verwaltungs-dll exportiert Funktionen, die der RAS-Server aufruft, wenn ein Benutzer versucht, eine Verbindung herzustellen oder diese zu trennen Im folgenden finden Sie einige der möglichen Verwendungsmöglichkeiten für eine RAS-Verwaltungs-dll:

-   Entscheiden Sie, ob ein Benutzer eine Verbindung mit dem Server herstellen darf. Die Verwaltungs-dll kann zusätzlich zur standardmäßigen RAS-Benutzerauthentifizierung eine Sicherheitsüberprüfung bereitstellen.
-   Notieren Sie sich die Zeit, mit der die einzelnen Benutzer eine Verbindung mit dem Server herstellen und die Verbindung trennen. Dies kann für Abrechnungs-oder Überwachungszwecke nützlich sein.
-   Weisen Sie jedem Benutzer eine IP-Adresse zu. Dies ist für die Sicherheit nützlich, da diese Funktion verwendet wird, um die Verbindung eines Benutzers zu einem bestimmten Computer zuzuordnen.

Der Speicherort der RAS-Verwaltungs-dll wird in der Registrierung angegeben. Weitere Informationen finden Sie unter [Registrierungs Einrichtung der RAS-Verwaltung](ras-administration-dll-registry-setup.md).

RAS unterstützt mehrere DLLs für die Verwaltung. Die Registrierung unterstützt mehrere dll-Speicherorte. RAS Ruft die Funktionen in den DLLs in der Reihenfolge auf, in der die DLLs in der Registrierung aufgeführt sind. Weitere Informationen finden Sie unter [Registrierungs Einrichtung der RAS-Verwaltung](ras-administration-dll-registry-setup.md).

**Windows 2000-Server:** RAS unterstützt nicht mehrere DLLs.

Eine RAS-Verwaltungs-dll muss alle folgenden Funktionen implementieren und exportieren:

[**Mpradminakzeptnewlink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[**Mpradmininitializedll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll)

[**Mpradminlinkhangupnotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[**Mpradminterminatedll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll)

Außerdem muss die RAS-Verwaltungs-dll entweder implementieren und exportieren.

[**Mpradminakzeptnewconnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) und

[**Mpradminconnectionhangupnotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification)

oder

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) und

[**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

Wenn alle erforderlichen Funktionen nicht implementiert sind, kann RAS nicht gestartet werden.

**Windows 2000-Server:** Eine Verwaltungs-dll muss die [**mpradmingetipaddressforuser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) -und [**mpradminreleaseipaddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) -Funktionen implementieren. Wenn die DLL eine dieser Funktionen implementiert, muss Sie auch die andere implementieren.

RAS Ruft die [**mpradmininitializedll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininitializedll) -Funktion auf, wenn der Routing-und RAS-Dienst zum ersten Mal gestartet wird. Die **mpradmininitializedll** -Funktion bietet die Möglichkeit, dass die Verwaltungs-dll jede erforderliche Initialisierung durchführen kann. Ebenso ruft RAS den [**mpradminterminatedll**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminterminatedll) -Dienst auf, wenn der Routing-und RAS-Dienst heruntergefahren wird. Mit dieser Funktion kann die Verwaltungs-dll alle notwendigen Bereinigungs Vorgänge ausführen, bevor Sie beendet wird.

Die Funktionen [**mpradminaccept tnewconnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) und [**mpradminconnectionhangupnotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) ermöglichen der dll, Benutzer Verbindungen mit dem Server zu überwachen. Ein RAS-Server Ruft die **mpradminakzeptnewconnection** -Funktion auf, wenn ein Benutzer versucht, eine Verbindung herzustellen. Mit dieser Funktion kann verhindert werden, dass der Benutzer eine Verbindung herstellt. Die **mpradminaccept tnewconnection** -Funktion kann auch Protokolleinträge für die Abrechnung oder Überwachung generieren. Wenn der Benutzer die Verbindung trennt, ruft der RAS-Server die **mpradminconnectionhangupnotification** -Funktion auf, die die Uhrzeit protokollieren kann, zu der der Benutzer die Verbindung getrennt hat.

Die [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) -Funktion und die [**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2) -Funktion ähneln **mpradminaccept tnewconnection** und [**mpradminconnectionhangupnotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification). Wenn jedoch die **MprAdminAcceptNewConnection2** -Funktion und die **MprAdminConnectionHangupNotification2** -Funktion von RAS aufgerufen wird, übergibt RAS einen zusätzlichen Parameter vom Typ [**RAS- \_ Verbindung \_ 2**](/windows/desktop/api/Mprapi/ns-mprapi-ras_connection_2).

RAS unterstützt mehrere DLLs für die Verwaltung. Der Remote Zugriffs Benutzer darf nur dann eine Verbindung herstellen, wenn die Implementierung der [**mpradminaccept tnewconnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) -Funktion oder der [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) -Funktion in jeder der DLLs die Verbindung akzeptiert. Anders ausgedrückt muss jede dll die Verbindung akzeptieren, damit der Benutzer eine Verbindung herstellen darf.

Es ist möglich, dass eine einzelne RAS-Verbindung beim Herstellen einer Verbindung mit einem RAS-Server mehrere Verknüpfungen verwendet. Die Funktionen [**mpradminaccept tnewlink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink) und [**mpradminlinkhangupnotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification) ermöglichen es der Verwaltungs-dll, einzelne Verknüpfungen in einer Verbindung zu verwalten. RAS ruft **mpradminakzeptnewlink** auf, wenn ein neuer Link für eine Verbindung eingerichtet wird. Da alle Verbindungen mindestens einen Link umfassen, ruft RAS immer sofort **mpradminakzeptnewlink** auf, sobald [**mpradminaccept tnewconnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) oder [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) zurückgegeben wurde, vorausgesetzt, dass [**mpradminakzeptnewconnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) oder [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) die Verbindung akzeptiert hat. RAS ruft **mpradminlinkhangupnotification** immer dann auf, wenn ein Link für eine Verbindung heruntergefahren wird.

Da RAS mehrere Verwaltungs-DLLs unterstützt, darf der Remote Zugriffs Benutzer nur dann eine Verbindung herstellen, wenn die Implementierung der [**mpradminaccept tnewlink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink) -Funktion in jeder der DLLs die Verbindung akzeptiert. Anders ausgedrückt, muss jede DLL den Link akzeptieren, damit der Link eingerichtet wird.

Nachdem der RAS-Server einen Benutzer authentifiziert hat, ruft er die [**mpradmingetipaddressforuser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) -Funktion auf, um eine IP-Adresse für den Remote Client zu erhalten. Diese Funktion bietet ein alternatives Schema für die Zuordnung einer IP-Adresse zu einem Einwählbenutzer. Wenn **mpradmingetipaddressforuser** nicht implementiert ist, ordnet ein RAS-Server den Remote Benutzer einer IP-Adresse zu, die aus einem statischen Pool von IP-Adressen ausgewählt wird, oder einen, der von einem DHCP-Server (Dynamic Host Configuration Protocol) ausgewählt wird. Die **mpradmingetipaddressforuser** -Funktion ermöglicht der dll, diese Standard-IP-Adresse zu überschreiben und eine bestimmte IP-Adresse für jeden Benutzer anzugeben. Die **mpradmingetipaddressforuser** -Funktion kann ein Flag festlegen, das bewirkt, dass RAS die [**mpradminreleaseipaddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) -Funktion aufruft, wenn der Benutzer die Verbindung trennt. Die dll kann dann **mpradminreleaseipaddress** verwenden, um die Zuordnung von Benutzer und IP-Adresse zu aktualisieren.

RAS unterstützt mehrere Verwaltungs-DLLs, ruft jedoch die Funktionen [**mpradmingetipaddressforuser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) und [**mpradminreleaseipaddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) nur in der ersten dll auf, die Sie implementiert und exportiert. RAS ignoriert Implementierungen dieser Funktionen in den anderen DLLs. RAS prüft die DLLs für diese Funktionen in der Reihenfolge, in der Sie in der [Registrierung](ras-administration-dll-registry-setup.md)aufgeführt sind.

RAS serialisiert Aufrufe in die Verwaltungs-dll. Ein Rückruf für eine der DLL-Funktionen für einen bestimmten RAS-Client führt nicht zu einem Aufrufe dieser Funktion für einen anderen RAS-Client. RAS Ruft die-Funktion für den anderen Client erst auf, wenn der erste-Vorgang beendet ist. Darüber hinaus erstreckt sich die Serialisierung auf bestimmte Gruppen von Funktionen. Die IP-Adress Funktionen werden als Gruppe serialisiert. ein Aufruf von [**mpradmingetipaddressforuser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser) oder [**mpradminreleaseipaddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress) blockiert Aufrufe beider Funktionen, bis der erste Aufruf zurückgegeben wurde. [**Mpradminaccept tnewconnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) und [**mpradminconnectionhangupnotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) werden ebenfalls als Gruppe serialisiert.

RAS führt die Funktionen aus, die IP-Adressen in einem Prozess zuweisen. die Funktionen für Verbindungs-und Verbindungs Benachrichtigungen werden in einem anderen Prozess ausgeführt. Folglich hängt die dll nicht von freigegebenen Daten zwischen diesen beiden Funktions Sätzen ab.

Rufen Sie keine der RAS- [Verwaltungsfunktionen](ras-administration-functions.md) oder [RAS-Benutzer Verwaltungsfunktionen](ras-user-administration-functions.md) innerhalb einer Legenden Funktion auf. Aufrufe dieser Funktionen werden nicht zurückgegeben, wenn Sie von innerhalb einer Legenden Funktion erstellt werden.

Der RAS-Server protokolliert einen Fehler im System Ereignisprotokoll, wenn beim Versuch, eine RAS-Verwaltungs-dll zu laden, oder beim Aufrufen einer der Funktionen der dll ein Fehler auftritt. Dies kann z. b. der Fall sein, wenn die dll den falschen Namen für eine exportierte Funktion angegeben hat, oder wenn der Funktionsname nicht in der DEF-Datei enthalten ist. Der Eintrag im Ereignisprotokoll gibt den Grund für den Fehler an.

**Windows 2000/NT:** Mehrere Administrations-DLLs werden nicht unterstützt.

 

 




