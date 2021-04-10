---
title: Daten werden von einem Format in ein anderes Format umgerechnet
description: Daten werden von einem Format in ein anderes Format umgerechnet
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- Audiokomprimierungs-Manager (ACM), Daten werden umgerechnet
- ACM (Audiokomprimierungs-Manager), Daten werden umgerechnet
- ACM-Beispiele, Daten werden umgerechnet
- Konvertieren von Daten
- acmstreamopen-Funktion
- acmstreamsize-Funktion
- acmStreamPrepareHeader-Funktion
- acmStreamConvert-Funktion
- acmstreamunprepareheader-Funktion
- acmstreamclose-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9645342aa9f19b2c31de77dc9d1031122ed0b2ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309919"
---
# <a name="converting-data-from-one-format-to-another"></a>Daten werden von einem Format in ein anderes Format umgerechnet

Der ACM verwendet Stream-Funktionen, um die Datenformat Konvertierung zu unterstützen. Konverter im ACM ändern das Format, jedoch nicht den Datentyp. Ein Konvertermodul kann z. b. 44-kHz-16-Bit-Daten in 44-kHz-, 8-Bit-Daten ändern.

Die folgenden ACM-Funktionen unterstützen die Datenformat Konvertierung. Sie werden in der Reihenfolge aufgelistet, in der Sie normalerweise verwendet werden.

-   Die [**acmstreamopen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) -Funktion öffnet einen konvertierungsstream.
-   Die [**acmstreamsize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) -Funktion berechnet die entsprechende Größe des Quell-oder Ziel Puffers.
-   Die [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) -Funktion bereitet Quell-und Ziel Puffer vor, die bei einer Konvertierung verwendet werden sollen.
-   Die [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) -Funktion konvertiert Daten in einem Quell Puffer in das Zielformat und schreibt die konvertierten Daten in den Ziel Puffer.
-   Die [**acmstreamunprepareheader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) -Funktion bereinigt den Quell-und Ziel Puffer, der von **acmStreamPrepareHeader** vorbereitet wurde. Sie müssen diese Funktion vor dem Freigeben des Quell-und Ziel Puffers abrufen.
-   Die [**acmstreamclose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) -Funktion schließt einen konvertierungsstream.

Wenn Sie Daten umrechnen, ermitteln Sie zunächst das Quellformat, und wählen Sie dann das Zielformat aus. Die einfachste Möglichkeit hierfür ist die Verwendung der [**acmformatchoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) -Funktion, die ein Dialogfeld für die Format Auswahl anzeigt und die Format Auswahl des Benutzers zurückgibt.

Wenn Sie das Quell-und das Zielformat kennen, können Sie mit [**acmstreamopen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) einen konvertierungsstream öffnen. Anschließend können Sie die [**acmstreamsize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) -Funktion verwenden, um die entsprechenden Puffergrößen zu bestimmen.

Der nächste Schritt besteht in der Vorbereitung der Puffer, die bei der Konvertierung mithilfe von [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)verwendet werden sollen.

Verwenden Sie zum Ausführen der Konvertierung [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) , bis alle Puffer verarbeitet wurden. Wenn die Konvertierung abgeschlossen ist, verwenden Sie [**acmstreamunprepareheader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) , um die Puffer zu bereinigen, und verwenden Sie dann [**acmstreamclose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) , um den Konvertierungsdaten Strom zu schließen.

 

 




