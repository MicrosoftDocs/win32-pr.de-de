---
title: Bluetooth-Funktionen
description: Die Funktionen in diesem Abschnitt werden zum Verwalten von Bluetooth-Geräten und-Diensten verwendet.
ms.assetid: 5cd4a050-51f3-40f4-b434-be639e109f0f
keywords:
- Bluetooth, Reference, Functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad5343f0d609185f3bb472570b8454931fc6a18b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473244"
---
# <a name="bluetooth-functions"></a>Bluetooth-Funktionen

Die Funktionen in diesem Abschnitt werden zum Verwalten von Bluetooth-Geräten und-Diensten verwendet.

Bluetooth wird auch durch die Verwendung der Windows Sockets-Programmierschnittstelle unterstützt. Weitere Informationen zum Programmieren von Bluetooth mithilfe der Windows Sockets-Schnittstelle finden Sie [unter Windows Sockets-Unterstützung für Bluetooth](windows-sockets-support-for-bluetooth.md).



| `Section`                                                                                | Inhalt                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Bluetoothauthenticatedevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)                     | Sendet eine Authentifizierungsanforderung an ein Bluetooth-Remote Gerät.                                                                                                                                 |
| [**Bluetoothauthenticatedeviceex**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedeviceex)                 | Sendet eine Authentifizierungsanforderung an ein Bluetooth-Remote Gerät. Außerdem ermöglicht diese Funktion das Übertragen von Out-of-Band-Daten an den Funktions aufruffür das Gerät, das authentifiziert wird. |
| [**Bluetoothauthenticatemultipledevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatemultipledevices)   | Ermöglicht dem Aufrufer, bei einer einzelnen Instanz des Bluetooth-Verbindungs-Assistenten zum Authentifizieren mehrerer Geräte aufzufordern.                                                            |
| [**Bluetoothdisplaydeviceproperties**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothdisplaydeviceproperties)           | Ruft die System Steuerungs Eigenschaft Geräteinformationen-Eigenschaften Blatt auf.                                                                                                                                  |
| [**Bluetoothenablediscovery**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenablediscovery)                           | Ändert den Ermittlungs Status eines lokalen Bluetooth oder der Funk Radios.                                                                                                                             |
| [**Bluetoothenableincomingconnections**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenableincomingconnections)       | Ändert, ob ein lokales Bluetooth-Radio eingehende Verbindungen akzeptiert.                                                                                                                        |
| [**Bluetoothenumerateinstalledservices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenumerateinstalledservices)     | Listet die GUIDs (Global Unique Identifiers) der Dienste auf, die auf einem Bluetooth-Gerät aktiviert sind.                                                                                    |
| [**Bluetoothfindendviceclose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfinddeviceclose)                           | Schließt ein enumerationshandle, das einer Geräte Abfrage zugeordnet ist.                                                                                                                          |
| [**Bluetoothfindfirstdevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstdevice)                           | Startet die Enumeration der lokalen Bluetooth-Geräte.                                                                                                                                            |
| [**Bluetoothfindfirstradio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)                             | Startet die Enumeration von lokalen Bluetooth-Radios.                                                                                                                                             |
| [**Bluetoothfindnextdevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextdevice)                             | Sucht das nächste Bluetooth-Gerät.                                                                                                                                                              |
| [**Bluetoothfindnextradio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)                               | Sucht das nächste Bluetooth-Radio.                                                                                                                                                               |
| [**Bluetoothfindradioclose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)                             | Schließt das enumerationshandle, das dem Auffinden von Bluetooth-Radios zugeordnet ist.                                                                                                               |
| [**Bluetoothgetdebug-Info**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetdeviceinfo)                               | Ruft Informationen zu einem Bluetooth-Remote Gerät ab. Das Bluetooth-Gerät muss bereits durch einen erfolgreichen Geräte Abfrage Funktions-Rückruf identifiziert werden.                           |
| [**Bluetoothgetradioinfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetradioinfo)                                 | Ruft Informationen zu einem Bluetooth-Radio ab.                                                                                                                                                  |
| [**Bluetoothisconnectable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisconnectable)                               | Bestimmt, ob ein Bluetooth-Radio oder ein Funk Funk Gerät Verbindungs fähig ist.                                                                                                                                |
| [**Bluetoothisdiscoverable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisdiscoverable)                             | Bestimmt, ob ein Bluetooth-Radio oder ein Bluetooth-Radio erkannt werden kann.                                                                                                                               |
| [**Bluetoothregisterforauthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)       | Registriert eine Rückruffunktion, die aufgerufen wird, wenn ein bestimmtes Bluetooth-Gerät eine Authentifizierung anfordert.                                                                                      |
| [**Bluetoothregisterforauthenticationex**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex)   | Registriert eine Anwendung für eine PIN-Anforderung, einen numerischen Vergleich und eine Rückruffunktion.                                                                                                         |
| [**Blueabothremuvedevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothremovedevice)                                 | Entfernt die Authentifizierung zwischen einem Bluetooth-Gerät und dem Computer, wobei alle zwischengespeicherten Informationen über das Gerät gelöscht werden.                                                                          |
| [**Bluetoothsdpumschlag Attribute**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes)                       | Listet den SDP-Daten Satz Datenstrom auf und ruft die Rückruffunktion für jedes Attribut im Datensatz auf.                                                                                    |
| [**Bluetoothsdpgetattributevalue**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetattributevalue)                 | Ruft den Attribut Wert für einen Attribut Bezeichner ab.                                                                                                                                    |
| [**Bluetoothsdpgetcontainerelementdata**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata)     | Iteriert einen ContainerStream und gibt jedes Element zurück, das im Containerelement enthalten ist.                                                                                     |
| [**Bluetoothsdpgetelementdata**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetelementdata)                       | Ruft ein einzelnes Element aus einem SDP-Stream ab und analysiert es.                                                                                                                                     |
| [**Bluetoothsdpgetstring**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetstring)                                 | Konvertiert eine in den SDP-Datensatz eingebettete unformatierte Zeichenfolge in eine Unicode-Zeichenfolge.                                                                                                               |
| [**Bluetoothselectdevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices)                               | Aktiviert die Bluetooth-Geräteauswahl.                                                                                                                                                           |
| [**Bluetoothselectdebug**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevicesfree)                       | Gibt Ressourcen frei, die einem vorherigen aufrufsbefehl der [**bluetoothselectdevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices) -Funktion zugeordnet sind.                                                                     |
| [**Bluetoothsendauthenticationresponse**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponse)     | Wird aufgerufen, wenn eine Authentifizierungsanforderung zum Senden der Hauptschlüssel-Antwort empfangen wird.                                                                                                               |
| [**Bluetoothsendauthenticationresponabex**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponseex) | Wird aufgerufen, wenn eine Authentifizierungsanforderung zum Senden der Hauptschlüssel-oder numerischen Vergleichs Antwort empfangen wird.                                                                                         |
| [**Bluetoothsetlocalserviceingefo**](/previous-versions/windows/desktop/legacy/bb870603(v=vs.85))                   | Legt lokale Dienst Informationen für ein bestimmtes Bluetooth-Radio fest.                                                                                                                                |
| [**Bluetoothsetservicestate**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsetservicestate)                           | Aktiviert oder deaktiviert Dienste für ein Bluetooth-Gerät.                                                                                                                                          |
| [**Bluetoothunregisterauthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothunregisterauthentication)         | Entfernt die Registrierung für eine Rückruf Routine, die zuvor mit einem Aufrufen der [**bluetoothregisterforauthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) -Funktion registriert wurde.      |
| [**Bluetoothupdatedevicerecord**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothupdatedevicerecord)                     | Aktualisiert den Cache des lokalen Computers über ein Bluetooth-Gerät.                                                                                                                                    |



 

 

 