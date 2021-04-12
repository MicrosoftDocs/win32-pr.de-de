---
title: WNET-Funktionen
description: Windows-Netzwerkfunktionen stellen Informationen und Dienstprogramme für die Verwaltung von Netzwerkressourcen bereit.
ms.assetid: 8a83186f-a912-4c61-8137-1f6be1f3afd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623de7adfdb57e21f01bff8b9647d6d2d175bd63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209320"
---
# <a name="wnet-functions"></a>WNET-Funktionen

Windows-Netzwerkfunktionen stellen Informationen und Dienstprogramme für die Verwaltung von Netzwerkressourcen bereit. Die Windows-Netzwerkfunktionen können wie folgt gruppiert werden:

-   [Verbindungsfunktionen](#connection-functions)
-   [Enumerationsfunktionen](#enumeration-functions)
-   [Informationsfunktionen](#information-functions)
-   [Benutzer Funktionen](#user-functions)

## <a name="connection-functions"></a>Verbindungsfunktionen

Rufen Sie die folgenden WNET-Verbindungsfunktionen auf, um ein lokales Gerät mit einer Netzwerkressource zu verbinden und Netzwerkverbindungen abzubrechen.



| Funktion                                                                     | BESCHREIBUNG                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Getetgetconnectionperformance"**](/windows/win32/api/winnetwk/nf-winnetwk-multinetgetconnectionperformancea) | Gibt Informationen zur erwarteten Leistung einer Verbindung mit einer Netzwerkressource zurück.                                                                                                                                      |
| [**Wnetaddconnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)                               | Stellt eine Verbindung zwischen einem lokalen Gerät und einer Netzwerkressource her. (Aus Kompatibilitätsgründen mit 16-Bit-Versionen von Windows bereitgestellt.)                                                                                                                   |
| [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a)                             | Stellt eine Verbindung zwischen einem lokalen Gerät und einer Netzwerkressource her.                                                                                                                                                                                 |
| [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)                             | Stellt eine Verbindung zwischen einem lokalen Gerät und einer Netzwerkressource her. Diese Funktion enthält einen weiteren Parameter als die **WNetAddConnection2** -Funktion, ein Handle für ein Fenster, das vom Netzwerkanbieter als Besitzer Fenster für Dialogfelder verwendet werden kann. |
| [**Wnetcancelconnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)                         | Bricht eine Netzwerkverbindung ab. (Aus Kompatibilitätsgründen mit 16-Bit-Versionen von Windows bereitgestellt.)                                                                                                                                    |
| [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)                       | Bricht eine Netzwerkverbindung ab und bietet die Möglichkeit, das Benutzerprofil mit Informationen zu permanenten Verbindungen zu aktualisieren.                                                                                                  |
| [**Wnetconnectiondialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog)                         | Startet ein allgemeines Dialogfeld zum Durchsuchen, um eine Verbindung mit Netzwerkressourcen herzustellen.                                                                                                                                                      |
| [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a)                       | Startet ein allgemeines Dialogfeld zum Durchsuchen, um mithilfe einer [**connectdlgstruct**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) -Struktur eine Verbindung mit Netzwerkressourcen herzustellen.                                                                                  |
| [**Wnetdisconnectdialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog)                         | Startet das Dialogfeld "Allgemeines Durchsuchen" zum Trennen der Verbindung mit Netzwerkressourcen.                                                                                                                                                 |
| [**WNetDisconnectDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog1a)                       | Startet das Dialogfeld "Allgemeines Durchsuchen" zum Trennen der Verbindung mit Netzwerkressourcen mithilfe einer [**discdlgstruct**](/windows/win32/api/winnetwk/ns-winnetwk-discdlgstructa) -Struktur.                                                                                   |
| [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona)                               | Ruft den Namen der Netzwerkressource ab, die einem lokalen Gerät zugeordnet ist.                                                                                                                                                     |
| [**Wnetgetuniversalname**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea)                         | Wenn ein Laufwerks basierter Pfad für eine Netzwerkressource angegeben ist, gibt eine allgemeinere Form des Namens zurück.                                                                                                                               |
| [**Wnetrestoreconnectionw**](/windows/win32/api/winnetwk/nf-winnetwk-wnetrestoreconnectionw)                     | Stellt die Verbindung mit einer Netzwerkressource wieder her und fordert ggf. den Benutzer zur Eingabe eines Namens und Kennworts auf.                                                                                                                      |
| [**Wnettuseconnction**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona)                               | Verbindet ein lokales Gerät mit einer Netzwerkressource. wählt automatisch ein nicht verwendetes lokales Gerät für die Umleitung zur Netzwerkressource aus.                                                                                               |



 

> [!Note]  
> Die Funktionen [**wnetaddconnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) und [**wnetcancelconnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) werden für die Kompatibilität mit Windows für Arbeitsgruppen unterstützt. Neue Anwendungen sollten jedoch [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) , [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)und [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)verwenden.

 

## <a name="enumeration-functions"></a>Enumerationsfunktionen

Nennen Sie die folgenden WNET-Funktionen, um Netzwerkressourcen aufzulisten.



| Funktion                                     | BESCHREIBUNG                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Wnetcloseerum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum)       | Beendet eine netzwerkressourcenenumeration.                                                    |
| [**Wnettenumschlag-Ressource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) | Setzt eine Enumeration von Netzwerkressourcen fort, die von der **WNetOpenEnum** -Funktion gestartet wurden. |
| [**Wnetopenaufumum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)         | Startet eine Enumeration von Netzwerkressourcen.                                             |



 

## <a name="information-functions"></a>Informationsfunktionen

Rufen Sie die folgenden WNET-Informations-und Hilfsfunktionen auf, um den Netzwerkanbieter und weitere Informationen abzurufen.



| Funktion                                                         | BESCHREIBUNG                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Wnetgetlasterror**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora)                     | Gibt den letzten von einem Netzwerkanbieter gemeldeten Fehlercode zurück, der von einer WNET-Funktion festgelegt wurde.  |
| [**Wnetgetnetworkinformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetnetworkinformationa)   | Gibt erweiterte Informationen zu einem bestimmten Netzwerkanbieter zurück.                                     |
| [**Wnetgetprovidername**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)               | Gibt den Anbieter Namen für einen bestimmten Netzwerktyp zurück.                                           |
| [**Wnetgetresourceinformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) | Gibt den Netzwerkanbieter zurück, der eine Ressource besitzt, und ruft Informationen über den Ressourcentyp ab. |
| [**Wnetgetresourceparent**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceparenta)           | Gibt das übergeordnete Element einer Netzwerkressource zurück.                                                           |



 

## <a name="user-functions"></a>Benutzer Funktionen

Rufen Sie die folgende WNET-Funktion auf, um den Namen des Benutzers abzurufen, der einem lokalen Gerät zugeordnet ist.



| Funktion                           | BESCHREIBUNG                                                                              |
|------------------------------------|------------------------------------------------------------------------------------------|
| [**Wnetgetuser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) | Gibt den aktuellen Standardbenutzer Namen oder den Benutzernamen zurück, der die Verbindung hergestellt hat. |



 

Viele der WNET-Funktionen verwenden eine [**nettresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) -Struktur zum Speichern von Informationen zu einer Netzwerkressource.

 

 