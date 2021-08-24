---
title: Bluetooth Funktionen
description: Die Funktionen in diesem Abschnitt werden zum Verwalten von Bluetooth und Diensten verwendet.
ms.assetid: 5cd4a050-51f3-40f4-b434-be639e109f0f
keywords:
- Bluetooth, Referenz, Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e8d945355b0bc25df4d91a96c30a4d20491eb3b0e86c3542e30c0f2b470833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701410"
---
# <a name="bluetooth-functions"></a>Bluetooth Funktionen

Die Funktionen in diesem Abschnitt werden zum Verwalten von Bluetooth und Diensten verwendet.

Bluetooth wird auch mithilfe der Windows Sockets-Programmierschnittstelle unterstützt. Weitere Informationen zum Programmieren von Bluetooth mithilfe der Windows Sockets-Schnittstelle finden Sie unter Windows [Sockets-Unterstützung für Bluetooth](windows-sockets-support-for-bluetooth.md).



| `Section`                                                                                | Inhalt                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)                     | Sendet eine Authentifizierungsanforderung an ein remote Bluetooth Gerät.                                                                                                                                 |
| [**BluetoothAuthenticateDeviceEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedeviceex)                 | Sendet eine Authentifizierungsanforderung an ein remote Bluetooth Gerät. Darüber hinaus ermöglicht diese Funktion die Übergeben von Out-of-Band-Daten an den Funktionsaufruf für das authentifizierte Gerät. |
| [**BluetoothAuthenticateMultipleDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatemultipledevices)   | Ermöglicht dem Aufrufer die Eingabeaufforderung, dass mehrere Geräte während einer einzelnen Instanz des Verbindungs-Assistenten Bluetooth werden sollen.                                                            |
| [**BluetoothDisplayDeviceProperties**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothdisplaydeviceproperties)           | Ruft das Systemsteuerung-Eigenschaftenblatt für Geräteinformationen auf.                                                                                                                                  |
| [**BluetoothEnableDiscovery**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenablediscovery)                           | Ändert den Ermittlungsstatus eines lokalen Bluetooth oder Radios.                                                                                                                             |
| [**BluetoothEnableIncomingConnections**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenableincomingconnections)       | Ändert, ob ein lokales Bluetooth eingehende Verbindungen akzeptiert.                                                                                                                        |
| [**BluetoothEnumerateInstalledServices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenumerateinstalledservices)     | Enumeriert die GUIDs (global eindeutige Bezeichner) der Dienste, die auf einem Bluetooth sind.                                                                                    |
| [**BluetoothFindDeviceClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfinddeviceclose)                           | Schließt ein Enumerationshand handle, das einer Geräteabfrage zugeordnet ist.                                                                                                                          |
| [**BluetoothFindFirstDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstdevice)                           | Beginnt die Enumeration von lokalen Bluetooth Geräten.                                                                                                                                            |
| [**BluetoothFindFirst Audio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)                             | Beginnt die Enumeration von lokalen Bluetooth Radios.                                                                                                                                             |
| [**BluetoothFindNextDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextdevice)                             | Sucht das nächste Bluetooth Gerät.                                                                                                                                                              |
| [**BluetoothFindNext Audio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)                               | Sucht das nächste Bluetooth Options options.                                                                                                                                                               |
| [**BluetoothFind LowClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)                             | Schließt das Enumerationshand handle, das dem Suchen von Bluetooth zugeordnet ist.                                                                                                               |
| [**BluetoothGetDeviceInfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetdeviceinfo)                               | Ruft Informationen zu einem Remotegerät Bluetooth ab. Das Bluetooth muss zuvor durch einen erfolgreichen Funktionsaufruf der Geräteanfrage identifiziert worden sein.                           |
| [**BluetoothGetInfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetradioinfo)                                 | Abrufen von Informationen zu einem Bluetooth Funkgerät.                                                                                                                                                  |
| [**BluetoothIsConnectable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisconnectable)                               | Bestimmt, ob ein Bluetooth oder Radios verbinden kann.                                                                                                                                |
| [**BluetoothIsDecoverable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisdiscoverable)                             | Bestimmt, ob ein Bluetooth radio oder radios erkennbar ist.                                                                                                                               |
| [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)       | Registriert eine Rückruffunktion, die aufgerufen wird, wenn ein Bluetooth Gerät die Authentifizierung an fordert.                                                                                      |
| [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex)   | Registriert eine Anwendung für eine Pinanforderung, einen numerischen Vergleich und eine Rückruffunktion.                                                                                                         |
| [**BluetoothRemoveDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothremovedevice)                                 | Entfernt die Authentifizierung zwischen einem Bluetooth und dem Computer und reikt alle zwischengespeicherten Informationen über das Gerät.                                                                          |
| [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes)                       | Durchzählt den SDP-Datensatzdatenstrom und ruft die Rückruffunktion für jedes Attribut im Datensatz auf.                                                                                    |
| [**BluetoothSdpGetAttributeValue**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetattributevalue)                 | Ruft den Attributwert für einen Attributbezeichner ab.                                                                                                                                    |
| [**BluetoothSdpGetContainerElementData**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata)     | Durch iteriert einen Containerstream und gibt jedes Element zurück, das im Containerelement enthalten ist.                                                                                     |
| [**BluetoothSdpGetElementData**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetelementdata)                       | Ruft ein einzelnes Element aus einem SDP-Stream ab und analysiert es.                                                                                                                                     |
| [**BluetoothSdpGetString**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetstring)                                 | Konvertiert eine unformatiert Zeichenfolge, die in den SDP-Datensatz eingebettet ist, in eine Unicode-Zeichenfolge.                                                                                                               |
| [**BluetoothSelectDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices)                               | Aktiviert Bluetooth Geräteauswahl.                                                                                                                                                           |
| [**BluetoothSelectDevicesFree**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevicesfree)                       | Gibt Ressourcen frei, die einem vorherigen Aufruf der [**BluetoothSelectDevices-Funktion zugeordnet**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices) sind.                                                                     |
| [**BluetoothSendAuthenticationResponse**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponse)     | Wird aufgerufen, wenn eine Authentifizierungsanforderung zum Senden der Hauptschlüsselantwort empfangen wird.                                                                                                               |
| [**BluetoothSendAuthenticationResponseEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponseex) | Wird aufgerufen, wenn eine Authentifizierungsanforderung zum Senden des Hauptschlüssels oder der Antwort auf einen numerischen Vergleich empfangen wird.                                                                                         |
| [**BluetoothSetLocalServiceInfo**](/previous-versions/windows/desktop/legacy/bb870603(v=vs.85))                   | Legt lokale Dienstinformationen für ein bestimmtes Bluetooth fest.                                                                                                                                |
| [**BluetoothSetServiceState**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsetservicestate)                           | Aktiviert oder deaktiviert Dienste für ein Bluetooth Gerät.                                                                                                                                          |
| [**BluetoothUnregisterAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothunregisterauthentication)         | Entfernt die Registrierung für eine Rückrufroutine, die zuvor mit einem Aufruf der [**BluetoothRegisterForAuthentication-Funktion registriert**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) wurde.      |
| [**BluetoothUpdateDeviceRecord**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothupdatedevicerecord)                     | Aktualisiert den Cache des lokalen Computers über ein Bluetooth Gerät.                                                                                                                                    |



 

 

 