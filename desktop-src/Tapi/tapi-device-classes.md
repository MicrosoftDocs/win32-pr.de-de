---
description: Erfahren Sie mehr über TAPI-Geräteklassen. Eine Geräteklasse ist eine Gruppe von Geräten oder Gerätetreibern, über die Anwendungen Anrufinformationen oder -daten senden und empfangen.
ms.assetid: 859979a8-0d16-4b7b-b183-d6e30f3e034d
title: TAPI-Geräteklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c16f5baf81bdc66d5110da2a1ac5127237738e
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011363"
---
# <a name="tapi-device-classes"></a>TAPI-Geräteklassen

Eine Geräteklasse ist eine Gruppe verwandter physischer Geräte oder Gerätetreiber, über die Anwendungen die Informationen oder Daten senden und empfangen, aus denen ein Aufruf besteht. Jede Geräteklasse  verfügt über einen Geräteklassennamen, der die Klasse eindeutig identifiziert, und stellt Informationen über die Programmierschnittstelle und Befehle bereit, die zum Öffnen und Kommunizieren mit den Geräten in der Klasse verwendet werden können.

Die Telefonieanwendungsprogrammierschnittstelle (Phoney Application Programming Interface, TAPI) ordnet Geräte aus mindestens einer Geräteklasse jeder Zeile oder jedem Telefongerät zu. Sie greifen auf eines dieser Geräte zu, indem Sie die Geräte-ID für das Gerät mithilfe der [**LineGetID-**](/windows/desktop/api/Tapi/nf-tapi-linegetid) oder [**phoneGetID-Funktion**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) abrufen. Sie geben den Geräteklassennamen an, und die Funktion gibt den spezifischen Portnamen, Gerätenamen, Gerätehand handle oder Gerätebezeichner zurück, den Sie zum Öffnen und Zugreifen auf das Gerät benötigen. Das Format der zurückgegebenen Informationen hängt von der Geräteklasse ab und wird in nachfolgenden Themen dieses Abschnitts beschrieben.

Sie verwenden auch Geräteklassennamen mit den Funktionen [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) und [**phoneConfigDialog,**](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) um dem Benutzer das Festlegen von Konfigurationsoptionen für das gegebene Gerät zu ermöglichen, mit den [**Funktionen lineGetIcon**](/windows/desktop/api/Tapi/nf-tapi-linegeticon) und [**phoneGetIcon**](/windows/desktop/api/Tapi/nf-tapi-phonegeticon) zum Abrufen eines Symbols zur Darstellung des angegebenen Geräts und mit den Funktionen [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) und [**lineSetDevConfig,**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) um Konfigurationsoptionen für das gegebene Gerät direkt abzurufen und zu festlegen.

Die folgende Liste enthält Geräteklassennamen.



| Geräteklassenname                                      | Beschreibung                                       |
|--------------------------------------------------------|---------------------------------------------------|
| [comm](comm.md)                                       | Kommunikationsport.                              |
| [comm/datamodem](comm-datamodem.md)                   | Modem über einen Kommunikationsport.              |
| [comm/datamodem/portname](comm-datamodem-portname.md) | Name des Geräts, mit dem ein Modem verbunden ist. |
| [wave/in](wave-in.md)                                 | Waveaudiogerät (nur Eingabe).                   |
| [wave/out](wave-out.md)                               | Wave-Audiogerät (nur Ausgabe).                  |
| [wave/in/out](wave-in-out.md)                         | Wave-Audiogerät, Vollduplex.                   |
| [keyboard/in](midi-in.md)                                 | SEQUENCEr (nur Eingabe).                      |
| [ein- und aus](midi-out.md)                               | SEQUENCE-Sequencer (nur Ausgabe).                     |
| [tapi/line](tapi-line.md)                             | Liniengerät.                                      |
| [tapi/phone](tapi-phone.md)                           | Telefongerät.                                     |
| [Ndis](ndis.md)                                       | Netzwerkgerät.                                   |
| [tapi/terminal](tapi-terminal.md)                     | Terminalgerät.                                  |



 

> [!Note]  
> Bei diesen Namen wird die Kleinschreibung nicht beachtet. Sie können eine beliebige Kombination aus Groß- und Kleinbuchstaben verwenden.

 

Zusätzliche Geräteklassen und Geräteklassennamen sind möglicherweise auf einem bestimmten System verfügbar. Wenn ein Gerät nicht zu einer der Standardgeräteklassen gehört, definiert der Hersteller im Allgemeinen eine neue Geräteklasse und weist einen eindeutigen Geräteklassennamen zu. Überprüfen Sie die Dokumentation für das Gerät, um zu ermitteln, welche zusätzlichen Geräteklassen für das Gerät verfügbar sind. Beachten Sie jedoch, dass die Geräteklasse und der Medientyp zwar verknüpft sind, aber nicht identisch sind. Ein Medientyp beschreibt das Aufrufinformationsformat, und eine Geräteklasse definiert die Programmierschnittstelle, die zum Verwalten dieser Informationen verwendet wird. Selbst wenn ein Hersteller einen neuen Medientyp definiert, ist es nicht unbedingt wahr, dass der Hersteller auch eine neue Geräteklasse definieren muss, um den Modus zu unterstützen.

Das Format der Konfigurationsdaten, die mit den [**Funktionen lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) und [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) verwendet werden, hängt ebenfalls von der Geräteklasse ab. Im Allgemeinen verwenden Sie **lineGetDevConfig,** um eine Kopie der aktuellen Gerätekonfigurationsdaten zu speichern, und verwenden dann **später lineSetDevConfig mit** den gespeicherten Konfigurationsdaten, um den vorherigen Zustand der Gerätekonfiguration wiederherzustellen. Dies ist eine praktische Möglichkeit, die Konfiguration vorübergehend zu ändern, ohne dass der Benutzer sie manuell in den vorherigen Zustand wiederherstellen muss. Da das genaue Format der Gerätekonfigurationsdaten bei jedem Dienstanbieter unterschiedlich sein kann, sollten Sie **lineSetDevConfig** und **lineGetDevConfig** nicht verwenden, um die Gerätekonfigurationsdaten direkt zu bearbeiten. Einige Formate werden nur zu Informationsinformationen bereitgestellt.

 

 



