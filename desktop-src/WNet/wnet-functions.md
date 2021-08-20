---
title: WNet-Funktionen
description: Windows Netzwerkfunktionen stellen Informationen und Hilfsprogramme für die Verwaltung von Netzwerkressourcen bereit.
ms.assetid: 8a83186f-a912-4c61-8137-1f6be1f3afd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771974bcc2967ddba32439bb655173f62b8478ad367e086e620ca02825a2567f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330785"
---
# <a name="wnet-functions"></a>WNet-Funktionen

Windows Netzwerkfunktionen stellen Informationen und Hilfsprogramme für die Verwaltung von Netzwerkressourcen bereit. Die Windows Netzwerkfunktionen können wie folgt gruppiert werden:

-   [Verbindungsfunktionen](#connection-functions)
-   [Enumerationsfunktionen](#enumeration-functions)
-   [Informationsfunktionen](#information-functions)
-   [Benutzerfunktionen](#user-functions)

## <a name="connection-functions"></a>Verbindungsfunktionen

Rufen Sie die folgenden WNET-Verbindungsfunktionen auf, um ein lokales Gerät mit einer Netzwerkressource zu verbinden und Netzwerkverbindungen abzubrechen.



| Funktion                                                                     | Beschreibung                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MultinetGetConnectionPerformance**](/windows/win32/api/winnetwk/nf-winnetwk-multinetgetconnectionperformancea) | Gibt Informationen zur erwarteten Leistung einer Verbindung mit einer Netzwerkressource zurück.                                                                                                                                      |
| [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)                               | Verbindet ein lokales Gerät mit einer Netzwerkressource. (Aus Gründen der Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt.)                                                                                                                   |
| [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a)                             | Verbindet ein lokales Gerät mit einer Netzwerkressource.                                                                                                                                                                                 |
| [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)                             | Verbindet ein lokales Gerät mit einer Netzwerkressource. Diese Funktion enthält einen Parameter mehr als die **WNetAddConnection2-Funktion,** ein Handle für ein Fenster, das der Netzwerkanbieter als Besitzerfenster für Dialogfelder verwenden kann. |
| [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)                         | Bricht eine Netzwerkverbindung ab. (Aus Gründen der Kompatibilität mit 16-Bit-Versionen von Windows bereitgestellt.)                                                                                                                                    |
| [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)                       | Bricht eine Netzwerkverbindung ab und bietet die Möglichkeit, das Benutzerprofil mit Informationen zu persistenten Verbindungen zu aktualisieren.                                                                                                  |
| [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog)                         | Startet ein allgemeines Dialogfeld zum Durchsuchen von Verbindungen mit Netzwerkressourcen.                                                                                                                                                      |
| [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a)                       | Startet ein allgemeines Dialogfeld zum Durchsuchen von Verbindungen mit Netzwerkressourcen mithilfe einer [**CONNECTDLGSTRUCT-Struktur.**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa)                                                                                  |
| [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog)                         | Startet ein allgemeines Dialogfeld zum Durchsuchen der Verbindung mit Netzwerkressourcen.                                                                                                                                                 |
| [**WNetDisconnectDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog1a)                       | Startet ein allgemeines Dialogfeld zum Durchsuchen der Verbindung mit Netzwerkressourcen unter Verwendung einer [**DISCDLGSTRUCT-Struktur.**](/windows/win32/api/winnetwk/ns-winnetwk-discdlgstructa)                                                                                   |
| [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona)                               | Ruft den Namen der Netzwerkressource ab, die einem lokalen Gerät zugeordnet ist.                                                                                                                                                     |
| [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea)                         | Wenn ein laufwerkbasierter Pfad für eine Netzwerkressource angegeben wird, gibt eine universellere Form des Namens zurück.                                                                                                                               |
| [**WNetRestoreConnectionW**](/windows/win32/api/winnetwk/nf-winnetwk-wnetrestoreconnectionw)                     | Stellt die Verbindung mit einer Netzwerkressource wieder her und fordert den Benutzer bei Bedarf zur Eingabe eines Namens und Kennworts auf.                                                                                                                      |
| [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona)                               | Verbindet ein lokales Gerät mit einer Netzwerkressource. wählt automatisch ein nicht verwendetes lokales Gerät aus, das zur Netzwerkressource umgeleitet werden soll.                                                                                               |



 

> [!Note]  
> Die Funktionen [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) und [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) werden aus Gründen der Kompatibilität mit Windows für Arbeitsgruppen unterstützt. Neue Anwendungen sollten jedoch [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) oder [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)und [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)verwenden.

 

## <a name="enumeration-functions"></a>Enumerationsfunktionen

Rufen Sie die folgenden WNet-Funktionen auf, um Netzwerkressourcen aufzuzählen.



| Funktion                                     | Beschreibung                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum)       | Beendet eine Netzwerkressourcenenumeration.                                                    |
| [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) | Setzt eine Enumeration von Netzwerkressourcen fort, die von der **WNetOpenEnum-Funktion** gestartet wurden. |
| [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)         | Startet eine Enumeration von Netzwerkressourcen.                                             |



 

## <a name="information-functions"></a>Informationsfunktionen

Rufen Sie die folgenden WNET-Informations- und Hilfsprogrammfunktionen auf, um Netzwerkanbieter und andere Informationen abzurufen.



| Funktion                                                         | Beschreibung                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora)                     | Gibt den letzten Fehlercode zurück, der von einer WNet-Funktion festgelegt wurde, der von einem Netzwerkanbieter gemeldet wurde.  |
| [**WNetGetNetworkInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetnetworkinformationa)   | Gibt erweiterte Informationen zu einem bestimmten Netzwerkanbieter zurück.                                     |
| [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)               | Gibt den Anbieternamen für einen bestimmten Netzwerktyp zurück.                                           |
| [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) | Gibt den Netzwerkanbieter zurück, der eine Ressource besitzt, und ruft Informationen zum Ressourcentyp ab. |
| [**WNetGetResourceParent**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceparenta)           | Gibt das übergeordnete Element einer Netzwerkressource zurück.                                                           |



 

## <a name="user-functions"></a>Benutzerfunktionen

Rufen Sie die folgende WNet-Funktion auf, um den Namen des Benutzers abzurufen, der einem lokalen Gerät zugeordnet ist.



| Funktion                           | Beschreibung                                                                              |
|------------------------------------|------------------------------------------------------------------------------------------|
| [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) | Gibt den aktuellen Standardbenutzernamen oder den Benutzernamen zurück, der die Verbindung hergestellt hat. |



 

Viele der WNET-Funktionen verwenden eine [**NETRESOURCE-Struktur,**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) um Informationen zu einer Netzwerkressource zu speichern.

 

 