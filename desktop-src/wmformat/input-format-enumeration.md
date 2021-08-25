---
title: Eingabeformatenumeration
description: Eingabeformatenumeration
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- Windows Medienformat-SDK, Eingabeformatenumerationen
- Windows Medienformat-SDK, Aufzählen von Eingabeformaten
- Advanced Systems Format (ASF), Eingabeformatenumerationen
- ASF (Advanced Systems Format), Eingabeformatenumerationen
- Advanced Systems Format (ASF), Aufzählen von Eingabeformaten
- ASF (Advanced Systems Format), Aufzählen von Eingabeformaten
- Eingabeformatenumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a261b2edae285a970bead5d039c4e85076530eb363aa025289b75ec56618406
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809040"
---
# <a name="input-format-enumeration"></a>Eingabeformatenumeration

Das Writer-Objekt ruft Streamformatinformationen aus dem Profil ab, das Sie ihm geben. Streamkonfigurationsinformationen in einem Profil geben dem Writer alle Benötigten Informationen darüber, wie die Daten in die Datei geschrieben werden sollen. Das Profil stellt dem Writer keine Informationen zum Format der Eingabebeispiele bereit, die Ihre Anwendung bereitstellt. Eingabeformate sind nur für Streams unbekannt, die mit einem der Windows Mediencodecs komprimiert sind. Eingaben für beliebige Streamtypen sind basierend auf den Informationen im Profil vorhersagbar.

Das Writer-Objekt kann mit dem Codec für einen Stream kommunizieren, um die Eingabetypen zu bestimmen, die verwendet werden können. Methoden werden bereitgestellt, um die möglichen Eingabetypen aufzuzählen. Sie sollten immer den Eingabetyp ermitteln, der Ihren Eingabemedien entspricht, indem Sie die unterstützten Typen aufzählen, anstatt die Eingabemedieneigenschaften manuell festzulegen. Weitere Informationen finden Sie unter [Aufzählen von Eingabeformaten.](to-enumerate-input-formats.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen zum Schreiben von Dateien**](file-writing-features.md)
</dt> <dt>

[**Arbeiten mit Eingaben**](working-with-inputs.md)
</dt> </dl>

 

 




