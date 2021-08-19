---
description: 'Windows Wia-Funktionen und -Methoden (Image Acquisition) können Fehlercodes aus der folgenden Liste zurückgeben: FehlercodeMeaningCodeWIA ERROR BUSYDas Gerät \_ \_ ist ausgelastet.'
ms.assetid: 3abbe92b-32b7-4820-b208-45c847243078
title: Fehlercodes (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c782ae449a52ae0ff2b64f124609a3142f1dd457d74bdb82333502ef1868ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670273"
---
# <a name="error-codes-wia"></a>Fehlercodes (WIA)

Windows WIA-Funktionen und -Methoden (Image Acquisition) können Fehlercodes aus der folgenden Liste zurückgeben: 

| Fehlercode                                      | Bedeutung                                                                                                                                                                                                                             | Code       |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| \_WIA-FEHLER \_ AUSGELASTET                                | Das Gerät ist ausgelastet. Schließen Sie alle Apps, die dieses Gerät verwenden, oder warten Sie, bis es abgeschlossen ist, und versuchen Sie es dann erneut.                                                                                                                          | 0x80210006 |
| WIA \_ ERROR \_ COVER \_ OPEN                         | Mindestens eine Abdeckung des Geräts ist geöffnet.                                                                                                                                                                                          | 0x80210016 |
| \_WIA-FEHLER: \_ \_ GERÄTEKOMMUNIKATION               | Fehler bei der Kommunikation mit dem WIA-Gerät. Stellen Sie sicher, dass das Gerät eingeschaltet und mit dem PC verbunden ist. Wenn das Problem weiterhin besteht, trennen Sie das Gerät, und verbinden Sie es erneut.                                                            | 0x8021000A |
| \_WIA-FEHLERGERÄT \_ \_ GESPERRT                      | Das Gerät ist gesperrt. Schließen Sie alle Apps, die dieses Gerät verwenden, oder warten Sie, bis es abgeschlossen ist, und versuchen Sie es dann erneut.                                                                                                                        | 0x8021000D |
| \_ \_ WIA-FEHLERAUSNAHME \_ IM \_ TREIBER               | Der Gerätetreiber hat eine Ausnahme ausgelöst.                                                                                                                                                                                               | 0x8021000E |
| \_WIA-FEHLER: \_ ALLGEMEINER \_ FEHLER                      | Beim WIA-Gerät ist ein unbekannter Fehler aufgetreten.                                                                                                                                                                                  | 0x80210001 |
| \_WIA-FEHLER: \_ FALSCHE \_ \_ HARDWAREEINSTELLUNG        | Es gibt eine falsche Einstellung auf dem WIA-Gerät.                                                                                                                                                                                    | 0x8021000C |
| \_WIA-FEHLER: \_ UNGÜLTIGER \_ BEFEHL                    | Das Gerät unterstützt diesen Befehl nicht.                                                                                                                                                                                            | 0x8021000B |
| \_WIA-FEHLER: \_ \_ UNGÜLTIGE \_ TREIBERANTWORT           | Die Antwort des Treibers ist ungültig.                                                                                                                                                                                            | 0x8021000F |
| \_ \_ WIA-FEHLERELEMENT \_ GELÖSCHT                       | Das WIA-Gerät wurde gelöscht. Sie ist nicht mehr verfügbar.                                                                                                                                                                               | 0x80210009 |
| WIA \_ ERROR \_ LAMP \_ OFF                           | Die Lampe des Scanners ist ausgeschaltet.                                                                                                                                                                                                          | 0x80210017 |
| WIA \_ ERROR \_ MAXIMUM \_ PRINTER \_ ENDORSER \_ COUNTER | Ein Überprüfungsauftrag wurde unterbrochen, weil ein Element vom Art "Bewerter"/"Unterstützung" den maximal gültigen Wert für WIA IPS PRINTER ENDORSER COUNTER erreicht hat und auf 0 zurückgesetzt \_ \_ \_ \_ wurde. Dieses Feature ist mit Windows 8 und neueren Versionen von Windows. | 0x80210021 |
| \_WIA-FEHLER: \_ \_ MULTIFEED                         | Ein Scanfehler ist aufgrund einer Bedingung mit mehreren Seitenfeeds aufgetreten. Dieses Feature ist mit Windows 8 und neueren Versionen von Windows.                                                                                            | 0x80210020 |
| \_WIA-FEHLER \_ OFFLINE                             | Das Gerät ist offline. Stellen Sie sicher, dass das Gerät eingeschaltet und mit dem PC verbunden ist.                                                                                                                                                  | 0x80210005 |
| \_ \_ WIA-FEHLERDOKUMENT \_ LEER                        | Im Dokumentfeeder sind keine Dokumente enthalten.                                                                                                                                                                                      | 0x80210003 |
| \_WIA-FEHLER \_ \_ PAPIERSTAU                          | Papier ist im Dokumentfeeder des Scanners eingeklemmt.                                                                                                                                                                                   | 0x80210002 |
| PROBLEM MIT \_ DEM WIA-FEHLERDOKUMENT \_ \_                      | Beim Dokumentfeeder des Scanners ist ein nicht angegebenes Problem aufgetreten.                                                                                                                                                                 | 0x80210004 |
| \_WIA-FEHLER \_ BEIM \_ AUFWÄRMEN                         | Das Gerät wird aufwärmt.                                                                                                                                                                                                           | 0x80210007 |
| \_WIA-FEHLER: \_ \_ BENUTZEREINGRIFF                  | Es liegt ein Problem mit dem WIA-Gerät vor. Stellen Sie sicher, dass das Gerät eingeschaltet, online und alle Kabel ordnungsgemäß angeschlossen sind.                                                                                                      | 0x80210008 |
| WIA \_ S KEIN GERÄT \_ \_ \_ VERFÜGBAR                   | Es wurde kein Scannergerät gefunden. Stellen Sie sicher, dass das Gerät online ist, mit dem PC verbunden ist und der richtige Treiber auf dem PC installiert ist.                                                                                                   | 0x80210015 |



 

 

 



