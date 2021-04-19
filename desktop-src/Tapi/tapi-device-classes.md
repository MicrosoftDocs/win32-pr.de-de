---
description: Eine Geräteklasse ist eine Gruppe verwandter physischer Geräte oder Gerätetreiber, über die Anwendungen die Informationen oder Daten senden und empfangen, die einen-Rückruf bilden.
ms.assetid: 859979a8-0d16-4b7b-b183-d6e30f3e034d
title: TAPI-Geräteklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357d68e07359468e7a3ba3a1e73c3e0888076e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366334"
---
# <a name="tapi-device-classes"></a>TAPI-Geräteklassen

Eine Geräteklasse ist eine Gruppe verwandter physischer Geräte oder Gerätetreiber, über die Anwendungen die Informationen oder Daten senden und empfangen, die einen-Rückruf bilden. Jede Geräteklasse verfügt über einen *Geräteklassen Namen* , der die Klasse eindeutig identifiziert, und enthält Informationen über die Programmierschnittstelle und die Befehle, die zum Öffnen und kommunizieren mit den Geräten in der Klasse verwendet werden können.

Die Telefonie-Anwendungsprogrammierschnittstelle (Application Programming Interface, TAPI) ordnet Geräte aus einer oder mehreren Geräteklassen den einzelnen Zeilen-oder Telefongeräten zu. Sie greifen auf eines dieser Geräte zu, indem Sie den Geräte Bezeichner für das Gerät mithilfe der [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) -oder [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) -Funktion abrufen. Sie geben den Geräteklassen Namen an, und die Funktion gibt den spezifischen Port Namen, den Gerätenamen, das Geräte handle oder den Geräte Bezeichner zurück, den Sie öffnen und auf das Gerät zugreifen müssen. Das Format der zurückgegebenen Informationen hängt von der Geräteklasse ab und wird in den nachfolgenden Themen dieses Abschnitts beschrieben.

Außerdem verwenden Sie Geräteklassen Namen mit den Funktionen [**lineconfigdialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) und [**phoneconfigdialog**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) , um dem Benutzer das Festlegen von Konfigurationsoptionen für das jeweilige Gerät zu ermöglichen. mit den Funktionen [**linegeticon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon) und [**phonegeticon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon) zum Abrufen eines Symbols für das angegebene Gerät und mit den Funktionen [**linegetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) und [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) , um die Konfigurationsoptionen für das jeweilige Gerät direkt abzurufen und festzulegen.

In der folgenden Liste werden Geräteklassen Namen angezeigt.



| Geräteklassen Name                                      | BESCHREIBUNG                                       |
|--------------------------------------------------------|---------------------------------------------------|
| [Komm](comm.md)                                       | Kommunikationsport                              |
| [comm/datamoder](comm-datamodem.md)                   | Modem über einen Kommunikationsport.              |
| [comm/DataModem/Portname](comm-datamodem-portname.md) | Der Name des Geräts, mit dem ein Modem verbunden ist. |
| [Wave/in](wave-in.md)                                 | Wave-Audiogerät (nur Eingabe).                   |
| [Wave/Out](wave-out.md)                               | Wave-Audiogerät (nur Ausgabe).                  |
| [Wave/in/out](wave-in-out.md)                         | Wave-Audiogerät, Vollduplex Duplex.                   |
| [MIDI/in](midi-in.md)                                 | MIDI Sequencer (nur Eingabe).                      |
| ["MIDI/Out"](midi-out.md)                               | MIDI Sequencer (nur Ausgabe).                     |
| [TAPI/Linie](tapi-line.md)                             | Liniengerät.                                      |
| [TAPI/Telefon](tapi-phone.md)                           | Phone-Gerät.                                     |
| [NDIS](ndis.md)                                       | Netzwerkgerät                                   |
| [TAPI/Terminal](tapi-terminal.md)                     | Terminal Gerät.                                  |



 

> [!Note]  
> Bei diesen Namen wird die Groß-/Kleinschreibung beachtet. Sie können eine beliebige Kombination von Groß-und Kleinbuchstaben verwenden.

 

Weitere Geräteklassen und Geräteklassen Namen sind möglicherweise auf einem bestimmten System verfügbar. Im allgemeinen definiert der Hersteller, wenn ein Gerät nicht zu einer der Standardgeräte Klassen gehört, in der Regel eine neue Geräteklasse und weist einen eindeutigen Geräteklassen Namen zu. Überprüfen Sie die Dokumentation für das Gerät, um zu bestimmen, welche zusätzlichen Geräteklassen für das Gerät verfügbar sind. Beachten Sie jedoch, dass die Geräteklasse und der Medientyp zwar verwandt sind, aber nicht identisch sind. Ein Medientyp beschreibt das Telefon informationsformat, und eine Geräteklasse definiert die Programmierschnittstelle, mit der diese Informationen verwaltet werden. Selbst wenn ein Hersteller einen neuen Medientyp definiert, ist es nicht unbedingt true, dass der Hersteller auch eine neue Geräteklasse definieren muss, um den Modus zu unterstützen.

Das Format der Konfigurationsdaten, die mit den Funktionen [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) und [**linegetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) verwendet werden, hängt auch von der Geräteklasse ab. Im Allgemeinen verwenden Sie **linegetdevconfig** , um eine Kopie der aktuellen Geräte Konfigurationsdaten zu speichern und später **linesetdevconfig** mit den gespeicherten Konfigurationsdaten zu verwenden, um die Gerätekonfiguration im vorherigen Zustand wiederherzustellen. Dies ist eine bequeme Möglichkeit, die Konfiguration vorübergehend zu ändern, ohne dass der Benutzer Sie manuell im vorherigen Zustand wiederherstellen muss. Da sich das genaue Format der Geräte Konfigurationsdaten bei den einzelnen Dienstanbietern unterscheiden kann, sollten Sie **linesetdevconfig** und **linegetdevconfig** nicht verwenden, um die Geräte Konfigurationsdaten direkt zu bearbeiten. Einige Formate werden nur für Informationen bereitgestellt.

 

 



