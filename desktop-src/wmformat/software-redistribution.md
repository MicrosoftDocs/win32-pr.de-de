---
title: Software Verteilung
description: Software Verteilung
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- Windows Media-Format-SDK, Software Verteilung
- Advanced Systems Format (ASF), Software Verteilung
- ASF (Advanced Systems Format), Software Verteilung
- SDK für Windows Media-Format, Neuverteilung
- Advanced Systems Format (ASF), Verteilung
- ASF (Advanced Systems Format), Verteilung
- Software Verteilung, Informationen zu
- Weiterverteilung, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d51f332f5b0e038293a1dbe1dbf59015931d67e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709474"
---
# <a name="software-redistribution"></a>Software Verteilung

Die Einbindung von Software im Windows Media-Format in eine Anwendungs Einrichtung wird als Neuverteilung bezeichnet. Das Windows Media-Format SDK enthält ein Installationspaket, das in das Anwendungs Setup aufgenommen werden kann. Das Installationspaket ist eine ausführbare Datei mit dem Namen wmfdist95.exe. Wenn Sie das Windows Media-Format-SDK installieren, wird das Installationspaket in den \\ Ordner "Redist" des Installationsverzeichnisses ( \\ standardmäßig "c: wmsdk \\ wmfsdk") kopiert.

In den folgenden Abschnitten finden Sie Prozeduren und weitere Informationen zum Setup für die Software Verteilung.



| `Section`                                                                            | BESCHREIBUNG                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [So erstellen Sie eine weitergabeeinrichtung](to-create-a-redistribution-setup.md)           | Beschreibt das Verfahren zum Erstellen eines Anwendungs Setups.                                                                                                                       |
| [Ermitteln des Setup Status](detecting-setup-status.md)                               | Stellt Beispielcode bereit, mit dem die Registrierung auf den Installationsstatus überprüft wird, um zu bestimmen, ob das Verteilungs Paket installiert werden muss.                                    |
| [Beispiel Code für die weitergabeeinrichtung](example-code-for-redistribution-setup.md) | Bietet Beispielcode, der in der Setup Routine verwendet werden kann, um die weitergabepakete im stillen Modus auszuführen und die Setup Routine zu benachrichtigen, wenn der Computer neu gestartet werden muss. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Überlegungen zu Projekten**](project-considerations.md)
</dt> </dl>

 

 




