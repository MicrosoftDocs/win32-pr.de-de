---
description: Eine Geräteklasse ist eine Gruppe verwandter physischer Geräte oder Gerätetreiber, über die Anwendungen die Informationen oder Daten senden und empfangen, die einen-Rückruf bilden.
ms.assetid: b29ea789-d017-4e35-b77a-c0d54ac54c66
title: TSPI-Geräteklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10392487657e8190052546605c54bed8cc0ccf4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349649"
---
# <a name="tspi-device-classes"></a>TSPI-Geräteklassen

Eine *Geräteklasse* ist eine Gruppe verwandter physischer Geräte oder Gerätetreiber, über die Anwendungen die Informationen oder Daten senden und empfangen, die einen-Rückruf bilden. Jede Geräteklasse verfügt über einen *Geräteklassen Namen* , der die Klasse eindeutig identifiziert und Informationen über die Programmierschnittstelle und Befehle bereitstellt, die zum Öffnen und kommunizieren mit den Geräten in der Klasse verwendet werden können.

Die Telefonie-Anwendungsprogrammierschnittstelle (Application Programming Interface, TAPI) ordnet Geräte aus einer oder mehreren Geräteklassen den einzelnen Zeilen-oder Telefongeräten zu. Sie greifen auf eines dieser Geräte zu, indem Sie den Geräte Bezeichner für das Gerät mithilfe der [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid) -oder [**phonegetid**](/windows/win32/api/tapi/nf-tapi-phonegetid) -Funktion abrufen. Sie geben den Geräteklassen Namen an, und die Funktion gibt den spezifischen Port Namen, den Gerätenamen, das Geräte handle oder den Geräte Bezeichner zurück, den Sie öffnen und auf das Gerät zugreifen müssen. Das Format der zurückgegebenen Informationen hängt von der Geräteklasse ab und wird in diesem Abschnitt beschrieben.

Außerdem verwenden Sie Geräteklassen Namen mit den Funktionen [**lineconfigdialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) und [**phoneconfigdialog**](/windows/win32/api/tapi/nf-tapi-phoneconfigdialog) , um dem Benutzer das Festlegen von Konfigurationsoptionen für das jeweilige Gerät zu ermöglichen. mit den Funktionen [**linegeticon**](/windows/win32/api/tapi/nf-tapi-linegeticon) und [**phonegeticon**](/windows/win32/api/tapi/nf-tapi-phonegeticon) zum Abrufen eines Symbols, das das angegebene Gerät darstellt. und mit den Funktionen [**linegetdevconfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) und [**linesetdevconfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) zum direkten Abrufen und Festlegen von Konfigurationsoptionen für das angegebene Gerät.

Im folgenden finden Sie die standardmäßigen Geräteklassen Namen.



| Geräteklassen Name                                       | BESCHREIBUNG                                      |
|---------------------------------------------------------|--------------------------------------------------|
| [Komm](/previous-versions/windows/desktop/legacy/ms725177(v=vs.85))                                       | Kommunikationsport                              |
| [comm/datamoder](/previous-versions/windows/desktop/legacy/ms725178(v=vs.85))                   | Modem über einen Kommunikationsport              |
| [comm/DataModem/Portname](/previous-versions/windows/desktop/legacy/ms725179(v=vs.85)) | Name des Geräts, mit dem ein Modem verbunden ist |
| [Wave/in](/previous-versions/windows/desktop/legacy/ms725990(v=vs.85))                                 | Wave-Audiogerät (nur Eingabe)                   |
| [Wave/Out](/previous-versions/windows/desktop/legacy/ms725992(v=vs.85))                               | Wave-Audiogerät (nur Ausgabe)                  |
| [Wave/in/out](/previous-versions/windows/desktop/legacy/ms725991(v=vs.85))                         | Wave-Audiogerät, Vollduplex Duplex                   |
| [MIDI/in](/previous-versions/windows/desktop/legacy/ms725244(v=vs.85))                                 | MIDI Sequencer (nur Eingabe)                      |
| ["MIDI/Out"](/previous-versions/windows/desktop/legacy/ms725245(v=vs.85))                               | MIDI Sequencer (nur Ausgabe)                     |
| [TAPI/Linie](/previous-versions/windows/desktop/legacy/ms725511(v=vs.85))                             | Liniengerät                                      |
| [TAPI/Telefon](/previous-versions/windows/desktop/legacy/ms725512(v=vs.85))                           | Telefongerät                                     |
| [NDIS](/previous-versions/windows/desktop/legacy/ms725247(v=vs.85))                                       | Netzwerkgerät                                   |
| [TAPI/Terminal](/previous-versions/windows/desktop/legacy/ms725515(v=vs.85))                     | Terminal Gerät                                  |



 

Bei diesen Namen wird die Groß-/Kleinschreibung nicht beachtet, sodass Sie eine beliebige Kombination von Groß-und Kleinbuchstaben verwenden können.

Weitere Geräteklassen und Geräteklassen Namen sind möglicherweise auf einem bestimmten System verfügbar. Im allgemeinen definiert der Hersteller, wenn ein Gerät nicht zu einer der Standardgeräte Klassen gehört, in der Regel eine neue Geräteklasse und weist einen eindeutigen Geräteklassen Namen zu. Sie müssen die Dokumentation für das Gerät überprüfen, um zu ermitteln, welche zusätzlichen Geräteklassen für das Gerät verfügbar sind. Beachten Sie jedoch, dass die Geräteklasse und der Medientyp zwar verwandt sind, aber nicht identisch sind. Ein *Medientyp* beschreibt das Format der Informationen für einen-Befehl, und eine *Geräteklasse* definiert die Programmierschnittstelle, die zum Verwalten dieser Informationen verwendet wird. Auch wenn ein Hersteller einen neuen Medientyp definiert, ist es möglicherweise nicht wahr, dass der Hersteller auch eine neue Geräteklasse definieren muss, um den Modus zu unterstützen.

Das Format der Konfigurationsdaten, die mit den Funktionen [**linesetdevconfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) und [**linegetdevconfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) verwendet werden, hängt auch von der Geräteklasse ab. Im Allgemeinen verwenden Sie **linegetdevconfig** , um eine Kopie der aktuellen Geräte Konfigurationsdaten zu speichern und später **linesetdevconfig** mit den gespeicherten Konfigurationsdaten zu verwenden, um die Gerätekonfiguration im vorherigen Zustand wiederherzustellen. Dies ist eine bequeme Möglichkeit, die Konfiguration vorübergehend zu ändern, ohne dass der Benutzer Sie manuell im vorherigen Zustand wiederherstellen muss. Da sich das genaue Format der Geräte Konfigurationsdaten bei den einzelnen Dienstanbietern unterscheiden kann, verwenden Sie **linesetdevconfig** und **linegetdevconfig** nicht, um die Geräte Konfigurationsdaten direkt zu bearbeiten. Einige Formate werden nur für Informationen bereitgestellt.

 

 
