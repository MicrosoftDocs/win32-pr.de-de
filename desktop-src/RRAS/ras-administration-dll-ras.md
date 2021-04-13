---
title: RAS-Verwaltungs-dll
description: Die dll exportiert Funktionen, die der RAS-Server aufruft, wenn ein Benutzer versucht, eine Verbindung herzustellen oder die Verbindung herzustellen.
ms.assetid: 014ab85d-8924-4c7a-89ed-f83e75318ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0908032e0916f0937e964408b1551d3f1515dea
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313781"
---
# <a name="ras-administration-dll"></a>RAS-Verwaltungs-dll

Die dll exportiert Funktionen, die der RAS-Server aufruft, wenn ein Benutzer versucht, eine Verbindung herzustellen oder die Verbindung herzustellen. Mit der dll können Sie die folgenden administrativen Funktionen ausführen:

-   Entscheiden Sie, ob ein Benutzer eine Verbindung mit dem Server herstellen darf. Dies kann zusätzlich zur standardmäßigen RAS-Benutzerauthentifizierung eine Sicherheitsüberprüfung bereitstellen.
-   Notieren Sie sich die Zeit, mit der die einzelnen Benutzer eine Verbindung mit dem Server herstellen und die Verbindung trennen. Dies kann für Abrechnungs-oder Überwachungszwecke nützlich sein.
-   Weisen Sie jedem Benutzer eine IP-Adresse zu. Dies kann aus Sicherheitsgründen nützlich sein, um die Verbindung eines Benutzers zu einem bestimmten Computer zuzuordnen.

Implementieren Sie die folgenden Funktionen, wenn Sie eine RAS-Server-Verwaltungs-dll entwickeln.

-   [**Rasadminakzeptnewconnection**](rasadminacceptnewconnection.md)
-   [**Rasadminconnectionhangupnotification**](rasadminconnectionhangupnotification.md)
-   [**Rasadmingetipaddressforuser**](rasadmingetipaddressforuser.md)
-   [**Rasadminreleaseipaddress**](rasadminreleaseipaddress.md)

Eine RAS-Verwaltungs-dll muss alle oben genannten Funktionen implementieren und exportieren. Wenn eine der Funktionen nicht implementiert ist, kann der Remote Zugriffs Dienst nicht gestartet werden.

Die Funktionen [**rasadminaccept tnewconnection**](rasadminacceptnewconnection.md) und [**rasadminconnectionhangupnotification**](rasadminconnectionhangupnotification.md) ermöglichen der dll, Benutzer Verbindungen mit dem Server zu überwachen. Ein Windows NT/Windows 2000-RAS-Server Ruft die **rasadminakzeptnewconnection** -Funktion auf, wenn ein Benutzer versucht, eine Verbindung herzustellen. Die Funktion kann verhindern, dass der Benutzer eine Verbindung herstellt. Sie können auch die-Funktion verwenden, um einen Eintrag in einem Protokoll zur Abrechnung oder Überwachung zu generieren. Wenn der Benutzer die Verbindung trennt, ruft der RAS-Server die **rasadminconnectionhangupnotification** -Funktion auf, die die Uhrzeit protokollieren kann, zu der der Benutzer die Verbindung getrennt hat.

Nachdem der RAS-Server einen Aufrufer authentifiziert hat, ruft er die [**rasadmingetipaddressforuser**](rasadmingetipaddressforuser.md) -Funktion auf, um eine IP-Adresse für den Remote Client abzurufen. Die dll kann diese Funktion verwenden, um ein alternatives Schema für die Zuordnung einer IP-Adresse zu einem Einwählbenutzer bereitzustellen. Wenn **rasadmingetipaddressforuser** nicht implementiert ist, verbindet ein RAS-Server einen Remote Benutzer mit einer IP-Adresse, die aus einem statischen Pool von IP-Adressen ausgewählt wurde, oder einer, der von einem DHCP-Server (Dynamic Host Configuration Protocol) ausgewählt wird. Die **rasadmingetipaddressforuser** -Funktion ermöglicht der dll, diese Standard-IP-Adresse zu überschreiben und eine bestimmte IP-Adresse für jeden Benutzer anzugeben. Die **rasadmingetipaddressforuser** -Funktion kann ein Flag festlegen, das bewirkt, dass RAS die [**rasadminreleaseipaddress**](rasadminreleaseipaddress.md) -Funktion aufruft, wenn der Benutzer die Verbindung trennt. Die dll kann [**rasadminreleaseipaddress**](rasadminreleaseipaddress.md) verwenden, um die Zuordnung von Benutzer und IP-Adresse zu aktualisieren.

RAS serialisiert Aufrufe in die Verwaltungs-dll. Ein Rückruf für eine der DLL-Funktionen für einen bestimmten RAS-Client wird nicht durch einen Rückruf dieser Funktion für einen anderen RAS-Client vorzeitig entfernt. der erste Aufruf ist garantiert, bevor RAS die-Funktion für den anderen Client aufruft. Darüber hinaus erstreckt sich die Serialisierung auf bestimmte Gruppen von Funktionen. Die IP-Adress Funktionen werden als Gruppe serialisiert. ein Aufruf von [**rasadmingetipaddressforuser**](rasadmingetipaddressforuser.md) oder [**rasadminreleaseipaddress**](rasadminreleaseipaddress.md) blockiert Aufrufe bis zum Abschluss des ersten Aufrufs. [**Rasadminaccept tnewconnection**](rasadminacceptnewconnection.md) und [**rasadminconnectionhangupnotification**](rasadminconnectionhangupnotification.md) werden ebenfalls als Gruppe serialisiert.

RAS führt die Funktionen zum Zuweisen von IP-Adressen in einem Prozess aus und führt die Funktionen für Verbindungs-und Verbindungs Benachrichtigungen in einem anderen Prozess aus. Folglich sollte die dll nicht von freigegebenen Daten zwischen den beiden Funktions Sätzen abhängen.

Der RAS-Server protokolliert einen Fehler im System Ereignisprotokoll, wenn beim Versuch, eine RAS-Verwaltungs-dll zu laden, oder beim Aufrufen einer der Funktionen der dll ein Fehler auftritt. Dies kann z. b. der Fall sein, wenn die dll den falschen Namen für eine exportierte Funktion angegeben hat, oder wenn der Funktionsname nicht in der DEF-Datei enthalten ist. Der Eintrag im Ereignisprotokoll gibt den Grund für den Fehler an.

**Windows 2000 Server und höher:** RAS-Verwaltungs-DLLs, die diese Funktions Schnittstelle implementieren, funktionieren nicht mehr. Verwenden Sie stattdessen die mpradmin-Funktions Schnittstelle, die mit den neueren Versionen von Windows bereitgestellt wird. Weitere Informationen finden Sie in der [Referenz zur RAS-Administration](remote-access-service-administration-reference.md) in der Dokumentation zu Routing und RAS.

 

 




