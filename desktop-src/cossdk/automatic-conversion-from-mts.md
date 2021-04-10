---
description: Automatische Konvertierung von MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Automatische Konvertierung von MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d424a443995c9fff9073878a43543d4c029a2445
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127165"
---
# <a name="automatic-conversion-from-mts"></a>Automatische Konvertierung von MTS

Die automatische Konvertierung erfolgt in zwei Schritten:

1.  Während des Windows-Setups. Die Konvertierung erfolgt durch den Windows-Setup Vorgang über das Dienstprogramm "mtstocom".
    > [!Note]  
    > Wenn Schritt 1 fehlschlägt, wurden möglicherweise einige oder alle der MTS-Pakete konvertiert, aber möglicherweise fehlen bestimmte Eigenschaften. Verwenden Sie in diesem Fall das Verwaltungs Programmkomponenten Dienste, um alle Attribute zu überprüfen. Die MTS-Attribute sind weiterhin auf dem Computer vorhanden (in der Systemregistrierung auf dem lokalen HKEY-Computer \_ \_ \\ Microsoft \\ Transaction Server), sind jedoch nur über das regedit.exe-Hilfsprogramm zugänglich.

     

2.  Nach dem letzten Neustart, bevor das Windows-Anmelde Dialogfeld angezeigt wird. In Schritt 2 werden diese Konvertierungs Aktionen behandelt, die den Netzwerk Zugriff erfordern (hauptsächlich Erstellung von Rollen Mitgliedern).
    > [!Note]  
    > Wenn Schritt 2 fehlschlägt (aufgrund von temporären Netzwerk-oder Domänen Controller Fehlern), ist es möglich, das mtstocom-Konvertierungsprogramm beliebig oft erneut auszuführen. Geben Sie dazu an der Eingabeaufforderung oder nach der Auswahl von **Ausführen** im **Startmenü** Folgendes ein: **% windir% \\ system32 \\mtstocom.exe**.

     

## <a name="mtstocom-log-file"></a>Mtstocom-Protokolldatei

Das Dienstprogramm mtstocom generiert eine Protokolldatei (mtstocom. log) im Windows-Verzeichnis. Diese Protokolldatei speichert einen Datensatz der Konvertierung von MTS-Paketen in com+-Anwendungen. Wenn während des Konvertierungs Vorgangs Fehler aufgetreten sind, ist es immer ratsam, die Protokolldatei zu überprüfen, um weitere Informationen zu erhalten. Die Protokolldatei fängt häufige Probleme, z. b. ungültige Benutzer oder Kennwort, ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ergebnisse und Probleme bei der com+-Konvertierung](com--conversion-results-and-issues.md)
</dt> <dt>

[Manuelle Konvertierung von MTS](manual-conversion-from-mts.md)
</dt> <dt>

[MTS-Verwaltungs Bibliothek](mts-administration-library.md)
</dt> </dl>

 

 



