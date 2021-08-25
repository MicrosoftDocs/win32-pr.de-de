---
title: RAS-Verwaltungs-DLL
description: Die DLL exportiert Funktionen, die der RAS-Server aufruft, wenn ein Benutzer versucht, eine Verbindung herzustellen oder die Verbindung zu trennen.
ms.assetid: 014ab85d-8924-4c7a-89ed-f83e75318ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6be479d00175750fb4d6ffce73aab4439d2c7df9e6e07f97e9964f267ce82a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909920"
---
# <a name="ras-administration-dll"></a>RAS-Verwaltungs-DLL

Die DLL exportiert Funktionen, die der RAS-Server aufruft, wenn ein Benutzer versucht, eine Verbindung herzustellen oder die Verbindung zu trennen. Sie können die DLL verwenden, um die folgenden administrativen Funktionen auszuführen:

-   Entscheiden Sie, ob ein Benutzer eine Verbindung mit dem Server herstellen soll. Dadurch kann zusätzlich zur standardmäßigen RAS-Benutzerauthentifizierung eine Sicherheitsüberprüfung bereitgestellt werden.
-   Zeichnen Sie die Zeit auf, zu der jeder Benutzer eine Verbindung mit dem Server herstellt und ihn trennt. Dies kann für Abrechnungs- oder Überwachungszwecke nützlich sein.
-   Weisen Sie jedem Benutzer eine IP-Adresse zu. Dies kann zu Sicherheitszwecken nützlich sein, um die Verbindung eines Benutzers einem bestimmten Computer zu zuordnen.

Implementieren Sie die folgenden Funktionen, wenn Sie eine RAS-Serververwaltungs-DLL entwickeln.

-   [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
-   [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
-   [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)
-   [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md)

Eine RAS-Verwaltungs-DLL muss alle oben genannten Funktionen implementieren und exportieren. Wenn eine der Funktionen nicht implementiert ist, kann der Remotezugriffsdienst nicht gestartet werden.

Mit [**den Funktionen RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md) und [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) kann die DLL Benutzerverbindungen mit dem Server überwachen. Ein Windows NT/Windows 2000 RAS-Server ruft die **RasAdminAcceptNewConnection-Funktion** auf, wenn ein Benutzer versucht, eine Verbindung herzustellen. Die -Funktion kann verhindern, dass der Benutzer eine Verbindung herstellen kann. Sie können die Funktion auch verwenden, um einen Eintrag in einem Protokoll für die Abrechnung oder Überwachung zu generieren. Wenn der Benutzer die Verbindung trennt, ruft der RAS-Server die **RasAdminConnectionHangupNotification-Funktion** auf, die den Zeitpunkt protokollieren kann, zu dem der Benutzer die Verbindung getrennt hat.

Nachdem der RAS-Server einen Aufrufer authentifiziert hat, ruft er die [**RasAdminGetIpAddressForUser-Funktion**](rasadmingetipaddressforuser.md) auf, um eine IP-Adresse für den Remoteclient zu erhalten. Die DLL kann diese Funktion verwenden, um ein alternatives Schema zum Zuordnen einer IP-Adresse zu einem Einwählbenutzer zur Verfügung zu stellen. Wenn **RasAdminGetIpAddressForUser** nicht implementiert ist, verbindet ein RAS-Server einen Remotebenutzer mit einer IP-Adresse, die aus einem statischen Ip-Adresspool oder einer von einem DHCP-Server (Dynamic Host Configuration Protocol) ausgewählten IP-Adresse ausgewählt wurde. Mit **der RasAdminGetIpAddressForUser-Funktion** kann die DLL diese Standard-IP-Adresse überschreiben und für jeden Benutzer eine bestimmte IP-Adresse angeben. Die **RasAdminGetIpAddressForUser-Funktion** kann ein Flag festlegen, das dazu führt, dass RAS die [**RasAdminReleaseIpAddress-Funktion**](rasadminreleaseipaddress.md) aufruft, wenn der Benutzer die Verbindung trennt. Die DLL kann [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) verwenden, um die Zuordnung zwischen Benutzer und IP-Adresse zu aktualisieren.

RAS serialisiert Aufrufe in die Verwaltungs-DLL. Ein Aufruf einer der DLL-Funktionen für einen bestimmten RAS-Client wird nie durch einen Aufruf dieser Funktion für einen anderen RAS-Client vorverlegt. Der erste Aufruf ist garantiert abgeschlossen, bevor RAS die Funktion für den anderen Client aufruft. Darüber hinaus erstreckt sich die Serialisierung auf bestimmte Gruppen von Funktionen. Die IP-Adressfunktionen werden als Gruppe serialisiert. Ein Aufruf von [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) oder [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md) blockiert Aufrufe in beide, bis der erste Aufruf abgeschlossen ist. [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md) und [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) werden ebenfalls als Gruppe serialisiert.

RAS führt die Funktionen zum Zuweisen von IP-Adressen in einem Prozess aus und führt die Funktionen für Verbindungs- und Trennungsbenachrichtigungen in einem anderen Prozess aus. Daher sollte die DLL nicht von freigegebenen Daten zwischen den beiden Funktionssätzen abhängen.

Der RAS-Server protokolliert einen Fehler im Systemereignisprotokoll, wenn beim Versuch, eine RAS-Verwaltungs-DLL zu laden, oder beim Aufrufen einer der DLL-Funktionen ein Fehler auftritt. Dies kann beispielsweise der Fall sein, wenn die DLL den falschen Namen für eine exportierte Funktion angegeben hat oder wenn der Funktionsname nicht in der DEF-Datei enthalten war. Der Eintrag im Ereignisprotokoll gibt die Ursache für den Fehler an.

**Windows 2000 Server und höher:** RAS-Verwaltungs-DLLs, die diese Funktionsschnittstelle implementieren, funktionieren nicht mehr. Verwenden Sie stattdessen die MprAdmin-Funktionsschnittstelle, die mit den neueren Versionen von Windows. Weitere Informationen finden Sie in der [RAS-Verwaltungsreferenz](remote-access-service-administration-reference.md) in der Routing- und RAS-Dokumentation.

 

 




