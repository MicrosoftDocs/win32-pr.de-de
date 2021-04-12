---
title: Eingabe Format-Enumeration
description: Eingabe Format-Enumeration
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- Windows Media-Format-SDK, Eingabe Format-Enumerationen
- Windows Media-Format-SDK, Aufzählen von Eingabe Formaten
- Advanced Systems Format (ASF), Eingabe Format-Enumerationen
- ASF (Advanced Systems Format), Eingabe formatenumerationen
- Advanced Systems Format (ASF), Aufzählen von Eingabe Formaten
- ASF (Advanced Systems Format), Aufzählen von Eingabe Formaten
- Eingabe formatenumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e853aeeac5ca470f1b33b611b287cba8fa025dc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471693"
---
# <a name="input-format-enumeration"></a>Eingabe Format-Enumeration

Das Writer-Objekt ruft streamformatinformationen aus dem Profil ab, das Sie ihm vergeben. Die Datenstrom-Konfigurationsinformationen in einem Profil geben dem Writer alle Informationen, die er benötigt, um zu erfahren, wie die Daten in die Datei geschrieben werden sollen. Das Profil stellt dem Writer keine Informationen über das Format der Eingabe Beispiele zur Verfügung, die von der Anwendung bereitgestellt werden. Eingabeformate sind nur für Datenströme unbekannt, die mit einem der Windows Media-Codecs komprimiert werden. Eingaben für beliebige Streamtypen sind auf der Grundlage der Informationen im Profil vorhersagbar.

Das Writer-Objekt kann mit dem Codec für einen Stream kommunizieren, um die Eingabetypen zu bestimmen, die verwendet werden können. Zum Auflisten der möglichen Eingabetypen werden Methoden bereitgestellt. Sie sollten immer den Eingabetyp ermitteln, der mit den Eingabemedien übereinstimmt, indem Sie die unterstützten Typen auflisten, anstatt die Eingabemedien Eigenschaften manuell festzulegen. Weitere Informationen finden [Sie unter so zählen Sie Eingabeformate auf](to-enumerate-input-formats.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen zum Schreiben von Dateien**](file-writing-features.md)
</dt> <dt>

[**Arbeiten mit Eingaben**](working-with-inputs.md)
</dt> </dl>

 

 




