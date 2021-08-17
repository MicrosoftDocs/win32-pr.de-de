---
title: Konvertieren von Daten aus einem Format in ein anderes
description: Konvertieren von Daten aus einem Format in ein anderes
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- Audiokomprimierungs-Manager (ACM), Konvertieren von Daten
- ACM (Audiokomprimierungs-Manager),Konvertieren von Daten
- ACM-Beispiele,Konvertieren von Daten
- Konvertieren von Daten
- acmStreamOpen-Funktion
- acmStreamSize-Funktion
- acmStreamPrepareHeader-Funktion
- acmStreamConvert-Funktion
- acmStreamUnprepareHeader-Funktion
- acmStreamClose-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ec1050066b92a356067085b491f5ddbf4bded47789c6e15a5187ea74c47c0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144810"
---
# <a name="converting-data-from-one-format-to-another"></a>Konvertieren von Daten aus einem Format in ein anderes

Der ACM verwendet Streamfunktionen zur Unterstützung der Datenformatkonvertierung. Konverter im ACM ändern das Format, aber nicht den Datentyp. Beispielsweise kann ein Konvertermodul 44-kHz-Daten mit 16 Bit in 8-Bit-Daten mit 44 kHz ändern.

Die folgenden ACM-Funktionen unterstützen die Datenformatkonvertierung. Sie werden in der Reihenfolge aufgeführt, in der Sie sie normalerweise verwenden würden.

-   Die [**acmStreamOpen-Funktion**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) öffnet einen Konvertierungsstream.
-   Die [**acmStreamSize-Funktion**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) berechnet die entsprechende Größe des Quell- oder Zielpuffers.
-   Die [**acmStreamPrepareHeader-Funktion**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) bereitet Quell- und Zielpuffer für die Verwendung in einer Konvertierung vor.
-   Die [**acmStreamConvert-Funktion**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) konvertiert Daten in einem Quellpuffer in das Zielformat und schreibt die konvertierten Daten in den Zielpuffer.
-   Die [**acmStreamUnprepareHeader-Funktion**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) bereinigt die Quell- und Zielpuffer, die von **acmStreamPrepareHeader** vorbereitet wurden. Sie müssen diese Funktion aufrufen, bevor Sie die Quell- und Zielpuffer freigeben.
-   Die [**acmStreamClose-Funktion**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) schließt einen Konvertierungsstream.

Identifizieren Sie beim Konvertieren von Daten zunächst das Quellformat, und wählen Sie dann das Zielformat aus. Die einfachste Möglichkeit hierfür ist die Verwendung der [**acmFormatChoose-Funktion,**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) die ein Dialogfeld für die Formatauswahl anzeigt und die Formatauswahl des Benutzers zurückgibt.

Wenn Sie die Quell- und Zielformate kennen, können Sie [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) verwenden, um einen Konvertierungsstream zu öffnen. Anschließend können Sie die [**acmStreamSize-Funktion**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) verwenden, um die entsprechenden Puffergrößen zu bestimmen.

Der nächste Schritt besteht darin, die Puffer für die Konvertierung mithilfe von [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)vorzubereiten.

Verwenden Sie zum Durchführen der Konvertierung [**acmStreamConvert,**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) bis alle Puffer verarbeitet wurden. Wenn die Konvertierung abgeschlossen ist, verwenden Sie [**acmStreamUnprepareHeader,**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) um die Puffer zu bereinigen, und verwenden Sie dann [**acmStreamClose,**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) um den Konvertierungsstream zu schließen.

 

 




