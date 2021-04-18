---
title: Präsentationszeit
description: Präsentationszeit
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- Windows Media-Format-SDK, Präsentations Zeiten
- Advanced Systems Format (ASF), Präsentations Zeiten
- ASF (Advanced Systems Format), Präsentations Zeiten
- Präsentations Zeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc88dbba93d1fc68905a4bfea92328a4ef600eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310895"
---
# <a name="presentation-time"></a>Präsentationszeit

Eine Präsentationszeit ist eine Zeitmessung aus dem ersten Beispiel des ersten Datenstroms in einer ASF-Datei. Diese Messung und die meisten anderen Messungen der Zeit, die von den Objekten dieses SDK verwendet werden, liegen in 100-Nanosecond-Einheiten. Präsentations Zeiten sind wichtig, da Sie ermöglichen, dass die verschiedenen Streams in einer Datei synchronisiert werden. Sie müssen für jedes Eingabe Beispiel, das Sie an den Writer übergeben, eine Präsentationszeit angeben. Jedem Datenobjekt im Daten Abschnitt einer ASF-Datei ist eine Präsentationszeit zugeordnet. Alle Ausgabe Beispiele, die vom Reader abgerufen werden, haben auch eine Präsentationszeit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](concepts.md)
</dt> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Medien Beispiele**](media-samples.md)
</dt> </dl>

 

 




