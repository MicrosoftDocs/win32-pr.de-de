---
description: Automatische Konvertierung von MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Automatische Konvertierung von MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02cc3889c479d829290b22b71edf13cc4ebc8f419c333d5e99390d47c01da65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549487"
---
# <a name="automatic-conversion-from-mts"></a>Automatische Konvertierung von MTS

Die automatische Konvertierung erfolgt in zwei Schritten:

1.  Während Windows Setup. Die Konvertierung wird vom Setupprozess Windows MTSTOCOM-Hilfsprogramm verarbeitet.
    > [!Note]  
    > Wenn Schritt 1 fehlschlägt, wurden möglicherweise einige oder alle MTS-Pakete tatsächlich konvertiert, es fehlen jedoch möglicherweise bestimmte Eigenschaften. Verwenden Sie in diesem Fall das Verwaltungstool Komponentendienste, um alle Attribute zu überprüfen. Die MTS-Attribute sind weiterhin auf dem Computer (in der Systemregistrierung unter HKEY LOCAL MACHINE Microsoft Transaction Server) vorhanden, aber nur über das Hilfsprogramm regedit.exe \_ \_ \\ \\ verfügbar.

     

2.  Nach dem letzten Neustart vor dem Windows das Anmeldedialogfeld angezeigt. Schritt 2 behandelt die Konvertierungsaktionen, die Netzwerkzugriff erfordern (in erster Linie erstellung von Rollenmitglied).
    > [!Note]  
    > Wenn Schritt 2 fehlschlägt (aufgrund von temporären Netzwerk- oder Domänencontrollerfehlern), ist es möglich, das MTSTOCOM-Konvertierungs-Hilfsprogramm so oft wie möglich erneut ausführen. Geben Sie hierzu an der Eingabeaufforderung oder nach dem Auswählen von Ausführen im **Startmenü** Folgendes ein: **%windir% \\ system32 \\mtstocom.exe.** 

     

## <a name="mtstocom-log-file"></a>MTSTOCOM-Protokolldatei

Das MTSTOCOM-Hilfsprogramm generiert eine Protokolldatei (Mtstocom.log) im Windows Verzeichnis. Diese Protokolldatei speichert einen Datensatz der Konvertierung von MTS-Paketen in COM+-Anwendungen. Wenn während des Konvertierungsprozesses Fehler aufgetreten sind, ist es immer eine gute Idee, die Protokolldatei auf weitere Informationen zu überprüfen. Die Protokolldatei fängt häufige Probleme ab, z. B. ungültige Benutzer oder Kennwörter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Konvertierungsergebnisse und -probleme](com--conversion-results-and-issues.md)
</dt> <dt>

[Manuelle Konvertierung von MTS](manual-conversion-from-mts.md)
</dt> <dt>

[MTS-Verwaltungsbibliothek](mts-administration-library.md)
</dt> </dl>

 

 



