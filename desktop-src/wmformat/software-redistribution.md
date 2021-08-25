---
title: Softwareverteilung
description: Softwareverteilung
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- Windows Medienformat-SDK, Softwareverteilung
- Advanced Systems Format (ASF), Softwareverteilung
- ASF (Advanced Systems Format), Softwareverteilung
- Windows Medienformat-SDK, Neuverteilung
- Advanced Systems Format (ASF), Redistribution
- ASF (Advanced Systems Format), Redistribution
- Softwareverteilung, Informationen
- redistribution,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b933df9319c342d8ed3502fc66757df2e6d8fd6e8d60309023ced6ffa042d5b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807890"
---
# <a name="software-redistribution"></a>Softwareverteilung

Die Einbeziehung Windows Medienformat-Software in ein Anwendungssetup wird als Weiterverteilung bezeichnet. Das Windows Media Format SDK enthält ein Installationspaket, das in der Anwendungseinrichtung enthalten sein kann. Das Installationspaket ist eine ausführbare Datei mit dem Namen wmfdist95.exe. Wenn Sie das Windows Media Format SDK installieren, wird das Installationspaket in den \\ Redist-Ordner des Installationsverzeichnisses kopiert \\ (standardmäßig c: wmsdk \\ wmfsdk).

Die folgenden Abschnitte enthalten Verfahren und andere Informationen zum Setup der Softwareverteilung.



| `Section`                                                                            | BESCHREIBUNG                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [So erstellen Sie ein Neuverteilungssetup](to-create-a-redistribution-setup.md)           | Beschreibt das Verfahren zum Erstellen eines Anwendungssetups.                                                                                                                       |
| [Ermitteln des Setupstatus](detecting-setup-status.md)                               | Stellt Beispielcode bereit, der die Registrierung auf den Installationsstatus überprüft, um zu bestimmen, ob das Weiterverteilungspaket installiert werden muss.                                    |
| [Beispielcode für das Setup der Neuverteilung](example-code-for-redistribution-setup.md) | Stellt Beispielcode bereit, der in der Setuproutine verwendet werden kann, um die Weiterverteilungspakete im stillen Modus auszuführen und die Setuproutine zu benachrichtigen, wenn der Computer neu gestartet werden muss. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Project Überlegungen**](project-considerations.md)
</dt> </dl>

 

 




