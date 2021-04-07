---
description: Manuelle Konvertierung von MTS
ms.assetid: 7ecc64a8-783d-4238-8b63-8e9c76382723
title: Manuelle Konvertierung von MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5fab25721738d497c943a166f899c73927b13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748297"
---
# <a name="manual-conversion-from-mts"></a>Manuelle Konvertierung von MTS

Möglicherweise möchten Sie die Konvertierung von MTS-Paketen in com+-Anwendungen isolieren, sodass diese außerhalb des Windows-Setup Vorgangs ausgeführt werden. Das folgende Verfahren bietet einen alternativen Ansatz:

1.  Exportieren Sie die MTS-Pakete mit dem Paket Export Feature "MTS 2,0" (was zu einer MTS-Paketdatei und einer Sammlung anderer Dateien führt).
2.  Löschen Sie die MTS-Pakete und die upgradefenster, oder führen Sie eine Neuinstallation von Windows aus.
3.  Installieren Sie die MTS-Paketdateien (. Pak) auf einem System unter Windows 2000 oder höher, indem Sie den Anwendungsinstallations-Assistenten des Verwaltungs Tools des Komponenten Diensts verwenden. Außerdem müssen Sie die "Run as"-Identität der Anwendung in der Systemregistrierung unter **HKEY \_ Local Machine Machines \_ " \\ \\ \\ AppID \\ runas**" zurücksetzen.

> [!Note]  
> Nur bei der automatischen Konvertierung (über Windows Setup oder durch Ausführen des Dienstprogramms mtstocom) wird die mtstocom-Protokolldatei generiert. Diese Datei wird nicht generiert, wenn die manuelle Konvertierung durchgeführt wird.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Automatische Konvertierung von MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Ergebnisse und Probleme bei der com+-Konvertierung](com--conversion-results-and-issues.md)
</dt> <dt>

[MTS-Verwaltungs Bibliothek](mts-administration-library.md)
</dt> </dl>

 

 



