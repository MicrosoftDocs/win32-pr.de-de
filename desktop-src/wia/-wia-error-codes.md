---
description: 'Funktionen und Methoden der Windows-Abbild Beschaffung (WIA) können Fehlercodes aus der folgenden Liste zurückgeben: Fehler codebedeutcodewia \_ Fehler-Fehlermeldung: \_ das Gerät ist ausgelastet.'
ms.assetid: 3abbe92b-32b7-4820-b208-45c847243078
title: Fehler Codes (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6025616d46a5973692bb3cafbcf88e18836ad0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863064"
---
# <a name="error-codes-wia"></a>Fehler Codes (WIA)

Funktionen und Methoden der Windows-Abbild Beschaffung (WIA) können Fehlercodes aus der folgenden Liste zurückgeben: 

| Fehlercode                                      | Bedeutung                                                                                                                                                                                                                             | Code       |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| WIA- \_ Fehler \_ ausgelastet                                | Das Gerät ist ausgelastet. Schließen Sie alle apps, die dieses Gerät verwenden, oder warten Sie, bis Sie abgeschlossen sind, und wiederholen Sie dann den Vorgang.                                                                                                                          | 0x80210006 |
| WIA- \_ Fehler \_ Abdeckung \_ geöffnet                         | Mindestens ein Geräte Abdeckung ist offen.                                                                                                                                                                                          | 0x80210016 |
| WIA-Fehler bei der \_ \_ Geräte \_ Kommunikation               | Fehler bei der Kommunikation mit dem WIA-Gerät. Stellen Sie sicher, dass das Gerät eingeschaltet und mit dem PC verbunden ist. Wenn das Problem weiterhin besteht, trennen Sie das Gerät, und verbinden Sie es erneut.                                                            | 0x8021000a |
| WIA- \_ Fehler \_ Gerät \_ gesperrt                      | Das Gerät ist gesperrt. Schließen Sie alle apps, die dieses Gerät verwenden, oder warten Sie, bis Sie abgeschlossen sind, und wiederholen Sie dann den Vorgang.                                                                                                                        | 0x8021000d |
| WIA- \_ Fehler \_ Ausnahme \_ in \_ Treiber               | Der Gerätetreiber hat eine Ausnahme ausgelöst.                                                                                                                                                                                               | 0x8021000e |
| Fehler beim \_ allgemeinen WIA-Fehler \_ \_                      | Unbekannter Fehler beim WIA-Gerät.                                                                                                                                                                                  | 0x80210001 |
| Fehler bei \_ \_ falscher \_ Hardware \_ Einstellung.        | Auf dem WIA-Gerät gibt es eine falsche Einstellung.                                                                                                                                                                                    | 0x8021000c |
| \_ \_ Ungültiger Befehl für WIA-Fehler \_                    | Das Gerät unterstützt diesen Befehl nicht.                                                                                                                                                                                            | 0x8021000b |
| Fehler beim Zurücksetzen eines \_ \_ ungültigen \_ Treibers. \_           | Die Antwort des Treibers ist ungültig.                                                                                                                                                                                            | 0x8021000f |
| WIA- \_ Fehler \_ Element \_ gelöscht                       | Das WIA-Gerät wurde gelöscht. Sie ist nicht mehr verfügbar.                                                                                                                                                                               | 0x80210009 |
| WIA- \_ Fehler- \_ Lamp deaktiviert \_                           | Die Lampe des Scanners ist deaktiviert.                                                                                                                                                                                                          | 0x80210017 |
| WIA- \_ Fehler beim \_ maximalen Drucker- \_ \_ Endorser- \_ Counter | Ein Überprüfungs Auftrag wurde unterbrochen, weil ein Imprinter/Endorser-Element den maximal zulässigen Wert für den Leistungsdaten-Leistungsempfänger des WIA- \_ IPS erreicht \_ \_ \_ hat und auf 0 zurückgesetzt wurde. Diese Funktion ist in Windows 8 und höheren Versionen von Windows verfügbar. | 0x80210021 |
| WIA- \_ Fehler bei \_ Multi- \_ Feed                         | Überprüfungs Fehler aufgrund einer multiseitenfeed-Bedingung. Diese Funktion ist in Windows 8 und höheren Versionen von Windows verfügbar.                                                                                            | 0x80210020 |
| WIA- \_ Fehler \_ Offline                             | Das Gerät ist offline. Stellen Sie sicher, dass das Gerät eingeschaltet und mit dem PC verbunden ist.                                                                                                                                                  | 0x80210005 |
| WIA- \_ Fehler \_ Papier \_ leer                        | Es sind keine Dokumente im Dokument-feedertyp vorhanden.                                                                                                                                                                                      | 0x80210003 |
| WIA- \_ Fehler \_ Papier \_ Stau                          | Das Papier wird in der Dokument-feederdatei des Scanners blockiert.                                                                                                                                                                                   | 0x80210002 |
| WIA- \_ Fehler \_ Papier \_ Problem                      | Es ist ein nicht angegebenes Problem mit der Dokument feederüberprüfung des Scanners aufgetreten.                                                                                                                                                                 | 0x80210004 |
| WIA- \_ Fehler beim \_ Aufwärmen \_                         | Das Gerät wird aufwärmt.                                                                                                                                                                                                           | 0x80210007 |
| WIA- \_ Fehler beim \_ Benutzer \_ Eingriff                  | Es ist ein Problem mit dem WIA-Gerät aufgetreten. Stellen Sie sicher, dass das Gerät eingeschaltet und Online ist und dass alle Kabel ordnungsgemäß verbunden sind.                                                                                                      | 0x80210008 |
| WIA \_ S \_ kein \_ Gerät \_ verfügbar                   | Es wurde kein Scannergerät gefunden. Stellen Sie sicher, dass das Gerät online ist, mit dem PC verbunden ist und dass der richtige Treiber auf dem PC installiert ist.                                                                                                   | 0x80210015 |



 

 

 



