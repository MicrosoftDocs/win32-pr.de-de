---
title: Präsentationszeit
description: Präsentationszeit
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- Windows Medienformat-SDK, Präsentationszeiten
- Advanced Systems Format (ASF), Präsentationszeiten
- ASF (Advanced Systems Format), Präsentationszeiten
- Präsentationszeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2dea9181552b42508745b256768b2c5ceb4443a057fc5d7d7a5a44410c788fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807910"
---
# <a name="presentation-time"></a>Präsentationszeit

Eine Präsentationszeit ist eine Messung der Zeit ab dem ersten Beispiel des ersten Streams in einer ASF-Datei. Diese Messung sowie die meisten anderen Zeitmessungen, die von den Objekten dieses SDK verwendet werden, sind in Einheiten von 100 Nanosekunden enthalten. Präsentationszeiten sind wichtig, da sie die Synchronisierung der verschiedenen Datenströme in einer Datei ermöglichen. Sie müssen für jedes Eingabebeispiel, das Sie an den Writer übergeben, eine Präsentationszeit bereitstellen. Jedem Datenobjekt im Datenabschnitt einer ASF-Datei ist eine Präsentationszeit zugeordnet. Jedes vom Reader abgerufene Ausgabebeispiel verfügt auch über eine Präsentationszeit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](concepts.md)
</dt> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Medienbeispiele**](media-samples.md)
</dt> </dl>

 

 




