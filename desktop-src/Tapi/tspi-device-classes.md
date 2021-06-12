---
description: Erfahren Sie mehr über TSPI-Geräteklassen. Eine Geräteklasse ist eine Gruppe von Geräten oder Gerätetreibern, über die Anwendungen Anrufinformationen oder Daten senden und empfangen.
ms.assetid: b29ea789-d017-4e35-b77a-c0d54ac54c66
title: TSPI-Geräteklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6775e73df3914339edbdf791659de821855864dd
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011343"
---
# <a name="tspi-device-classes"></a>TSPI-Geräteklassen

Eine *Geräteklasse* ist eine Gruppe verwandter physischer Geräte oder Gerätetreiber, über die Anwendungen die Informationen oder Daten senden und empfangen, aus denen ein Anruf besteht. Jede Geräteklasse verfügt über einen *Geräteklassennamen,* der die Klasse eindeutig identifiziert und Informationen über die Programmierschnittstelle und Befehle bereitstellt, die zum Öffnen und Kommunizieren mit den Geräten in der Klasse verwendet werden können.

TapI (Telefonieanwendungsprogrammierschnittstelle) ordnet Geräte aus einer oder mehreren Geräteklassen jeder Zeile oder jedem Telefongerät zu. Sie greifen auf eines dieser Geräte zu, indem Sie den Gerätebezeichner für das Gerät mithilfe der [**funktion lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid) oder [**phoneGetID**](/windows/win32/api/tapi/nf-tapi-phonegetid) abrufen. Sie geben den Geräteklassennamen an, und die Funktion gibt den spezifischen Portnamen, Gerätenamen, Gerätehandle oder Gerätebezeichner zurück, den Sie zum Öffnen und Zugreifen auf das Gerät benötigen. Das Format der zurückgegebenen Informationen hängt von der Geräteklasse ab und wird in diesem Abschnitt beschrieben.

Sie verwenden auch Geräteklassennamen mit den Funktionen [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) und [**phoneConfigDialog,**](/windows/win32/api/tapi/nf-tapi-phoneconfigdialog) um dem Benutzer das Festlegen von Konfigurationsoptionen für das angegebene Gerät zu ermöglichen. mit den Funktionen [**lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon) und [**phoneGetIcon,**](/windows/win32/api/tapi/nf-tapi-phonegeticon) um ein Symbol abzurufen, das das angegebene Gerät darstellt. und mit den Funktionen [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) und [**lineSetDevConfig,**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) um Konfigurationsoptionen für das angegebene Gerät direkt abzurufen und festzulegen.

Im Folgenden werden die Standardnamen der Geräteklassen angezeigt.



| Name der Geräteklasse                                       | Beschreibung                                      |
|---------------------------------------------------------|--------------------------------------------------|
| [comm](/previous-versions/windows/desktop/legacy/ms725177(v=vs.85))                                       | Kommunikationsport                              |
| [comm/datamodem](/previous-versions/windows/desktop/legacy/ms725178(v=vs.85))                   | Modem über einen Kommunikationsport              |
| [comm/datamodem/portname](/previous-versions/windows/desktop/legacy/ms725179(v=vs.85)) | Name des Geräts, mit dem ein Modem verbunden ist |
| [wave/in](/previous-versions/windows/desktop/legacy/ms725990(v=vs.85))                                 | Wave-Audiogerät (nur Eingabe)                   |
| [Wave/Out](/previous-versions/windows/desktop/legacy/ms725992(v=vs.85))                               | Wave-Audiogerät (nur Ausgabe)                  |
| [Wave/In/Out](/previous-versions/windows/desktop/legacy/ms725991(v=vs.85))                         | Wave-Audiogerät, Vollduplex                   |
| [verzeichnis/in](/previous-versions/windows/desktop/legacy/ms725244(v=vs.85))                                 | MULTIPLIKATOR-Sequencer (nur Eingabe)                      |
| [und out](/previous-versions/windows/desktop/legacy/ms725245(v=vs.85))                               | LITER SEQUENCER (nur Ausgabe)                     |
| [tapi/line](/previous-versions/windows/desktop/legacy/ms725511(v=vs.85))                             | Line Device                                      |
| [tapi/phone](/previous-versions/windows/desktop/legacy/ms725512(v=vs.85))                           | Telefongerät                                     |
| [Ndis](/previous-versions/windows/desktop/legacy/ms725247(v=vs.85))                                       | Netzwerkgerät                                   |
| [tapi/terminal](/previous-versions/windows/desktop/legacy/ms725515(v=vs.85))                     | Terminalgerät                                  |



 

Bei diesen Namen wird die Groß-/Kleinschreibung nicht beachtet, sodass Sie eine beliebige Kombination aus Groß- und Kleinbuchstaben verwenden können.

Auf einem bestimmten System können zusätzliche Geräteklassen und Geräteklassennamen verfügbar sein. Wenn ein Gerät nicht zu einer der Standardgeräteklassen gehört, definiert der Hersteller in der Regel eine neue Geräteklasse und weist einen eindeutigen Geräteklassennamen zu. Sie müssen die Dokumentation für das Gerät überprüfen, um zu ermitteln, welche zusätzlichen Geräteklassen für das Gerät verfügbar sind. Beachten Sie jedoch, dass die Geräteklasse und der Medientyp zwar verknüpft sind, aber nicht identisch sind. Ein *Medientyp* beschreibt ein Format von Informationen zu einem Aufruf, und eine *Geräteklasse* definiert die Programmierschnittstelle, die zum Verwalten dieser Informationen verwendet wird. Selbst wenn ein Hersteller einen neuen Medientyp definiert, ist es möglicherweise nicht richtig, dass der Hersteller auch eine neue Geräteklasse definieren muss, um den Modus zu unterstützen.

Das Format der Konfigurationsdaten, die mit den Funktionen [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) und [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) verwendet werden, hängt auch von der Geräteklasse ab. Im Allgemeinen verwenden Sie **lineGetDevConfig,** um eine Kopie der aktuellen Gerätekonfigurationsdaten zu speichern, und später **lineSetDevConfig** mit den gespeicherten Konfigurationsdaten, um den vorherigen Zustand der Gerätekonfiguration wiederherzustellen. Dies ist eine praktische Möglichkeit, die Konfiguration vorübergehend zu ändern, ohne dass der Benutzer sie manuell in den vorherigen Zustand wiederherstellen muss. Da sich das genaue Format der Gerätekonfigurationsdaten bei jedem Dienstanbieter unterscheiden kann, verwenden Sie **nicht lineSetDevConfig** und **lineGetDevConfig,** um die Gerätekonfigurationsdaten direkt zu bearbeiten. Einige Formate werden nur zu Informationszwecken bereitgestellt.

 

 
