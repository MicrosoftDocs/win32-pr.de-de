---
title: Verwenden von Dred zum Diagnostizieren von GPU-Fehlern
description: Vom Gerät entfernte erweiterte Daten (Dred) ist ein weiterentwickelnder Satz von Diagnose Features, die Ihnen helfen, die Ursache unerwarteter Fehler beim Entfernen von Geräten zu ermitteln.
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: bbc754239210899e804d41a294e8c9f47967fb25
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2020
ms.locfileid: "104548667"
---
# <a name="use-dred-to-diagnose-gpu-faults"></a>Verwenden von Dred zum Diagnostizieren von GPU-Fehlern
Dred steht für vom Gerät entfernte erweiterte Daten. Dred ist ein weiterentwickelnder Satz von Diagnose Features, mit denen Sie die Ursache unerwarteter Fehler beim Entfernen von Geräten identifizieren können. Auf Hardware, die die erforderlichen Features unterstützt (wie unten definiert), übermittelt Dred sowohl Automatisches Brotkrümel als auch GPU-Seiten Fehlerberichte.

## <a name="auto-breadcrumbs"></a>Auto-breadkrümel
Um die Szene für Auto-breadkrümel festzulegen, nennen wir zuerst die manuelle Vielfalt. In Erwartung der Eventualität einer [Timeout Erkennung und-Wiederherstellung](/windows-hardware/drivers/display/timeout-detection-and-recovery)können Sie mit der [ID3D12GraphicsCommandList2:: schreitebufferimmediate-Methode](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate) *breadkrümel* in den GPU-Befehlsdaten Strom platzieren, um den GPU-Status zu verfolgen.

Dies ist ein sinnvoller Ansatz, wenn Sie eine benutzerdefinierte Implementierung mit geringem Aufwand erstellen möchten. Möglicherweise fehlen jedoch einige der Vielseitigkeit einer standardisierten Lösung, z. b. Debugger-Erweiterungen oder die Berichterstattung über [Windows-Fehlerberichterstattung (wer)](/windows/desktop/wer/windows-error-reporting) (auch als Watson bezeichnet).

Der automatische breadkrümel-Befehl von Dred ruft also " **Write-bufferimmediate** " auf, um Fortschrittsindikatoren in den GPU-Befehlsdaten Strom zu versetzen. Dred fügt einen Breadcrumb nach jedem *Rendering-op ein* &mdash; . Dies bedeutet, dass jeder Vorgang, der zu GPU führt, funktioniert (z. b. **Zeichnen**, verteilen, **Kopieren**, **Auflösen** und andere). Wenn das Gerät in der Mitte einer GPU-Arbeitsauslastung entfernt wird, ist der Dred Breadcrumb-Wert im Wesentlichen eine Auflistung der Rendering-OPS, die vor dem Fehler abgeschlossen wurden.

Der Breadcrumb-Verlaufs Ringpuffer behält bis zu 64kib-Vorgänge in einer bestimmten Befehlsliste bei. Wenn in einer Befehlsliste mehr als 65536 Vorgänge vorhanden sind, werden nur die letzten 64kib-Vorgänge gespeichert, &mdash; die zuerst die ältesten Vorgänge überschreiben. Der Breadcrumb-Zählerwert wird jedoch weiterhin bis zu gezählt `UINT_MAX` . Daher ist lastopindex = (breadcrumbcount-1) %65536.

Dred 1,0 war zum ersten Mal in Windows 10, Version 1809 (Windows 10-Update vom Oktober 2018) verfügbar, und Sie stellte rudimentäre Auto-breadkrümel zur Verfügung. Es gab jedoch keine APIs dafür, und die einzige Möglichkeit zum Aktivieren von Dred 1,0 war die Verwendung von **Feedback-Hub** , um eine TDR-Reproduktion (Repro) für apps zu erfassen, **& Spiele** \> **Leistung und Kompatibilität**. Der primäre Zweck für Dred 1,0 war, das Auftreten von Spiel abstürzen über Kundenfeedback zu erleichtern.
### <a name="caveats"></a>Vorbehalte
- Da eine GPU stark Pipelines umfasst, gibt es keine Garantie dafür, dass der Breadcrumb-Counter den genauen Vorgang angibt, bei dem ein Fehler aufgetreten ist. Tatsächlich ist es bei einigen auf Kacheln basierenden verzögerten Rendering-Geräten möglich, dass der Breadcrumb-Counter eine vollständige Ressource oder eine UAV-Barriere (unsortierter Zugriffs Ansicht) hinter dem tatsächlichen GPU-Fortschritt ist.
- Ein Anzeigetreiber kann Befehle neu anordnen, vor dem Ausführen eines Befehls vor dem Ausführen eines Befehls vor dem Ausführen eines Befehls vorab aus dem Ressourcen Speicher abrufen oder den zwischengespeicherten Speicher nach Abschluss eines Befehls leeren. Jeder dieser Fehler kann einen GPU-Fehler verursachen. In solchen Fällen sind die Auto-Breadcrumb-Leistungsindikatoren möglicherweise weniger hilfreich oder irreführend.
### <a name="performance"></a>Leistung
Obwohl Auto-breadkrümel so konzipiert sind, dass der Aufwand gering ist, sind Sie nicht kostenlos. Empirische Messungen zeigen einen Leistungsverlust von 2-5% auf einer typischen Grafik Spiel-Engine von AAA Direct3D 12. Aus diesem Grund sind Auto-breadkrümel standardmäßig deaktiviert.
### <a name="hardware-requirements"></a>Hardwareanforderungen
Da die Breadcrumb-Werte nach dem Entfernen des Geräts beibehalten werden müssen, muss die Ressource, die breadkrümel enthält, im Systemspeicher vorhanden sein, und Sie muss im Fall der Entfernung des Geräts beibehalten werden. Dies bedeutet, dass der Anzeigetreiber [**D3D12_FEATURE_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)unterstützen muss. Dies ist für die meisten Direct3D 12-Anzeigetreiber unter Windows 10, Version 1903, der Fall.
## <a name="gpu-page-fault-reporting"></a>GPU-Seiten Fehlerberichterstattung
Ein neues Feature für Dred 1,1 ist die Dred GPU Page Fault Reporting. Ein GPU-Seiten Fehler tritt in der Regel unter einer der folgenden Bedingungen auf.

1. Eine Anwendung führt versehentlich arbeiten an der GPU aus, die auf ein gelöschtes Objekt verweist. Dies ist einer der wichtigsten Gründe für eine unerwartete Entfernung von Geräten.
2. Eine Anwendung führt versehentlich Arbeit auf der GPU aus, die auf eine entfernte Ressource zugreift, oder auf eine nicht residente Kachel.
3. Ein Shader verweist auf einen nicht initialisierten oder veralteten Deskriptor.
3. Ein shaderindex über das Ende einer Stamm Bindung hinaus.

Dred versucht, einige dieser Szenarien zu beheben, indem die Namen und Typen vorhandener oder kürzlich frei gegebener API-Objekte gemeldet werden, die der virtuellen Adresse (VA) des von GPU gemeldeten Seiten Fehlers entsprechen.

### <a name="caveat"></a>Nachteil
Nicht alle GPUs unterstützen Seiten Fehler (obwohl dies viele tun). Einige GPUs reagieren durch Bitbucket Schreibvorgänge auf Speicherfehler. Lesen von simulierten Daten (z. b. Nullen); oder einfach hängend. In Fällen, in denen die GPU nicht sofort reagiert, kann es vorkommen, dass eine [Timeout Erkennung und-Wiederherstellung (TDR)](/windows-hardware/drivers/display/timeout-detection-and-recovery) zu einem späteren Zeitpunkt in der Pipe durchgeführt werden kann, was die Suche nach der Ursache noch erschwert.

### <a name="performance"></a>Leistung
Die Direct3D 12-Laufzeit muss eine Auflistung vorhandener und vor kurzem gelöschter API-Objekte, die von der virtuellen Adresse (VA) indiziert werden können, aktiv durchsetzen. Dadurch erhöht sich der Systemspeicher Aufwand und führt zu einer geringen Leistungssteigerung bei der Objekt Erstellung und-Zerstörung. Aus diesem Grund ist dieses Verhalten standardmäßig deaktiviert.

### <a name="hardware-requirements"></a>Hardwareanforderungen
Eine GPU, die Seiten Fehler nicht unterstützt, kann weiterhin von der Funktion für automatisches Brotkrümel profitieren.

## <a name="setting-up-dred-in-code"></a>Einrichten von Dred in Code
Dred-Einstellungen sind für den Prozess Global, und Sie müssen Sie konfigurieren, bevor Sie ein Direct3D 12-Gerät erstellen. Rufen Sie dazu die [**D3D12GetDebugInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) -Funktion auf, um ein [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings)-Zeichen abzurufen.

```cpp
CComPtr<ID3D12DeviceRemovedExtendedDataSettings> pDredSettings;
VERIFY_SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&pDredSettings)));

// Turn on auto-breadcrumbs and page fault reporting.
pDredSettings->SetAutoBreadcrumbsEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
pDredSettings->SetPageFaultEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
```

> [!NOTE]
> Änderungen an den Dred-Einstellungen wirken sich nicht auf bereits erstellte Geräte aus. Bei nachfolgenden Aufrufen von [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) werden jedoch die aktuellsten Dred-Einstellungen verwendet.

## <a name="accessing-dred-data-in-code"></a>Zugreifen auf Dred-Daten im Code
Nachdem die Geräte Entfernung erkannt wurde (z. b **.** gibt [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/com/com-error-codes-10)zurück), verwenden Sie die Methoden der [**ID3D12DeviceRemovedExtendedData**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) -Schnittstelle, um auf die Dred-Daten für das entfernte Gerät zuzugreifen.

Rufen Sie zum Abrufen der **ID3D12DeviceRemovedExtendedData** -Schnittstelle [QueryInterface](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)) für eine [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) (oder abgeleitete) Schnittstelle auf, und übergeben Sie dabei den Schnittstellen Bezeichner (IID) von **ID3D12DeviceRemovedExtendedData**.

```cpp
void MyDeviceRemovedHandler(ID3D12Device * pDevice)
{
    CComPtr<ID3D12DeviceRemovedExtendedData> pDred;
    VERIFY_SUCCEEDED(pDevice->QueryInterface(IID_PPV_ARGS(&pDred)));
    D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT DredAutoBreadcrumbsOutput;
    D3D12_DRED_PAGE_FAULT_OUTPUT DredPageFaultOutput;
    VERIFY_SUCCEEDED(pDred->GetAutoBreadcrumbsOutput(&DredAutoBreadcrumbsOutput));
    VERIFY_SUCCEEDED(pDred->GetPageFaultAllocationOutput(&DredPageFaultOutput));
    // Custom processing of DRED data can be done here.
    // Produce telemetry...
    // Log information to console...
    // break into a debugger...
}
```

## <a name="debugger-access-to-dred"></a>Debugger-Zugriff auf Dred
-Debug-Dateien haben Zugriff auf die Dred-Daten über **d3d12! D3D12DeviceRemovedExtendedData** Daten exportieren.

## <a name="dred-telemetry"></a>Dred-Telemetrie
Die Anwendung kann die Dred-APIs zum Steuern der Dred-Features und zum Sammeln von Telemetriedaten für die Analyse von Problemen verwenden. Dadurch erhalten Sie ein viel breiteres Netzwerk für das Abfangen dieser schwer zu reproduzieren TDRS.

Ab Windows 10, Version 1903, werden alle Ereignisse, die vom Benutzermodus entfernt wurden, an [Windows-Fehlerberichterstattung (wer)](/windows/desktop/wer/windows-error-reporting)gemeldet, auch als Watson bezeichnet. Wenn eine bestimmte Kombination aus Anwendung, GPU und Anzeigetreiber eine ausreichende Anzahl von Ereignissen entfernt, die von einem Gerät entfernt werden, ist es möglich, dass Dred vorübergehend für Kunden aktiviert ist, die dieselbe Anwendung in einer ähnlichen Konfiguration starten.
