---
description: Erfahren Sie mehr über TSPI-Geräteklassen. Eine Geräteklasse ist eine Gruppe von Geräten oder Gerätetreibern, über die Anwendungen Anrufinformationen oder -daten senden und empfangen.
ms.assetid: b29ea789-d017-4e35-b77a-c0d54ac54c66
title: TSPI-Geräteklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd6d2e79e021b6b73bc24ef0edb5b343fb8487ced3ca414084c7f2ad23a6c48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975437"
---
# <a name="tspi-device-classes"></a>TSPI-Geräteklassen

Eine *Geräteklasse ist* eine Gruppe verwandter physischer Geräte oder Gerätetreiber, über die Anwendungen die Informationen oder Daten senden und empfangen, aus denen ein Aufruf besteht. Jede Geräteklasse  verfügt über einen Geräteklassennamen, der die Klasse eindeutig identifiziert und Informationen über die Programmierschnittstelle und Befehle enthält, die zum Öffnen und Kommunizieren mit den Geräten in der Klasse verwendet werden können.

Die Telefonieanwendungsprogrammierschnittstelle (Phoney Application Programming Interface, TAPI) ordnet Geräte aus mindestens einer Geräteklasse jeder Linie oder jedem Telefongerät zu. Sie greifen auf eines dieser Geräte zu, indem Sie die Geräte-ID für das Gerät mithilfe der [**LineGetID-**](/windows/win32/api/tapi/nf-tapi-linegetid) oder [**phoneGetID-Funktion**](/windows/win32/api/tapi/nf-tapi-phonegetid) abrufen. Sie geben den Geräteklassennamen an, und die Funktion gibt den spezifischen Portnamen, Gerätenamen, Gerätehand handle oder Gerätebezeichner zurück, den Sie zum Öffnen und Zugreifen auf das Gerät benötigen. Das Format der zurückgegebenen Informationen hängt von der Geräteklasse ab und wird in diesem Abschnitt beschrieben.

Sie verwenden auch Geräteklassennamen mit den [**Funktionen lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) und [**phoneConfigDialog,**](/windows/win32/api/tapi/nf-tapi-phoneconfigdialog) um dem Benutzer das Festlegen von Konfigurationsoptionen für das gegebene Gerät zu ermöglichen. mit den [**Funktionen lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon) und [**phoneGetIcon**](/windows/win32/api/tapi/nf-tapi-phonegeticon) zum Abrufen eines Symbols zur Darstellung des angegebenen Geräts; und mit den [**Funktionen lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) und [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) zum direkten Abrufen und Festlegen von Konfigurationsoptionen für das gegebene Gerät.

Im Folgenden finden Sie die Standardnamen der Geräteklasse.



| Geräteklassenname                                       | Beschreibung                                      |
|---------------------------------------------------------|--------------------------------------------------|
| [comm](/previous-versions/windows/desktop/legacy/ms725177(v=vs.85))                                       | Kommunikationsport                              |
| [comm/datamodem](/previous-versions/windows/desktop/legacy/ms725178(v=vs.85))                   | Modem über einen Kommunikationsport              |
| [comm/datamodem/portname](/previous-versions/windows/desktop/legacy/ms725179(v=vs.85)) | Name des Geräts, mit dem ein Modem verbunden ist |
| [wave/in](/previous-versions/windows/desktop/legacy/ms725990(v=vs.85))                                 | Waveaudiogerät (nur Eingabe)                   |
| [wave/out](/previous-versions/windows/desktop/legacy/ms725992(v=vs.85))                               | Wave-Audiogerät (nur Ausgabe)                  |
| [wave/in/out](/previous-versions/windows/desktop/legacy/ms725991(v=vs.85))                         | Wave-Audiogerät, Vollduplex                   |
| [keyboard/in](/previous-versions/windows/desktop/legacy/ms725244(v=vs.85))                                 | SEQUENCEr (nur Eingabe)                      |
| [ein- und aus](/previous-versions/windows/desktop/legacy/ms725245(v=vs.85))                               | SEQUENCEr (nur Ausgabe)                     |
| [tapi/line](/previous-versions/windows/desktop/legacy/ms725511(v=vs.85))                             | Liniengerät                                      |
| [tapi/phone](/previous-versions/windows/desktop/legacy/ms725512(v=vs.85))                           | Telefon Gerät                                     |
| [Ndis](/previous-versions/windows/desktop/legacy/ms725247(v=vs.85))                                       | Netzwerkgerät                                   |
| [tapi/terminal](/previous-versions/windows/desktop/legacy/ms725515(v=vs.85))                     | Terminalgerät                                  |



 

Bei diesen Namen wird die Groß-/Kleinschreibung nicht beachtet, sodass Sie eine beliebige Kombination aus Groß- und Kleinbuchstaben verwenden können.

Zusätzliche Geräteklassen und Geräteklassennamen sind möglicherweise auf einem bestimmten System verfügbar. Wenn ein Gerät nicht zu einer der Standardgeräteklassen gehört, definiert der Hersteller im Allgemeinen eine neue Geräteklasse und weist einen eindeutigen Geräteklassennamen zu. Sie müssen die Dokumentation für das Gerät überprüfen, um zu ermitteln, welche zusätzlichen Geräteklassen für das Gerät verfügbar sind. Beachten Sie jedoch, dass die Geräteklasse und der Medientyp zwar verknüpft sind, aber nicht identisch sind. Ein *Medientyp* beschreibt ein Format von Informationen  zu einem Aufruf, und eine Geräteklasse definiert die Programmierschnittstelle, die zum Verwalten dieser Informationen verwendet wird. Selbst wenn ein Hersteller einen neuen Medientyp definiert, ist es möglicherweise nicht wahr, dass der Hersteller auch eine neue Geräteklasse definieren muss, um den Modus zu unterstützen.

Das Format der Konfigurationsdaten, die mit den [**Funktionen lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig) und [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig) verwendet werden, hängt ebenfalls von der Geräteklasse ab. Im Allgemeinen verwenden Sie **lineGetDevConfig,** um eine Kopie der aktuellen Gerätekonfigurationsdaten zu speichern, und verwenden dann **später lineSetDevConfig mit** den gespeicherten Konfigurationsdaten, um den vorherigen Zustand der Gerätekonfiguration wiederherzustellen. Dies ist eine praktische Möglichkeit, die Konfiguration vorübergehend zu ändern, ohne dass der Benutzer sie manuell in den vorherigen Zustand wiederherstellen muss. Da das genaue Format der Gerätekonfigurationsdaten bei jedem Dienstanbieter unterschiedlich sein kann, verwenden Sie **lineSetDevConfig** und **lineGetDevConfig** nicht, um die Gerätekonfigurationsdaten direkt zu bearbeiten. Einige Formate werden nur zu Informationsinformationen bereitgestellt.

 

 
