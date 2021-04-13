---
title: Fehlerbehandlung in com (com)
description: Fehlerbehandlung in com
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19af496eabf50833c99d462ff074254bc39bb7a0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104475009"
---
# <a name="error-handling-in-com-com"></a>Fehlerbehandlung in com (com)

Fast alle com-Funktionen und Schnittstellen Methoden geben einen Wert vom Typ **HRESULT** zurück. Das **HRESULT** (für das *Ergebnis Handle*) ist eine Möglichkeit, Erfolgs-, Warnungs-und Fehler Werte zurückzugeben. **HRESULT** s werden für nichts behandelt. Dabei handelt es sich nur um Werte, deren Felder im-Wert codiert sind. Gemäß der com-Spezifikation gibt das Ergebnis 0 (null) einen Erfolg an, und ein Ergebnis ungleich NULL weist auf einen Fehler hin.

Auf Quell Code Ebene bestehen alle Fehler Werte aus drei Teilen, die durch Unterstriche voneinander getrennt sind. Der erste Teil ist das Präfix, das die dem Fehler zugeordnete Anlage identifiziert, der zweite Teil "E" für "Error" und der dritte Teil eine Zeichenfolge, die die tatsächliche Bedingung beschreibt. Beispielsweise wird **STG \_ E \_ mediüberfull** zurückgegeben, wenn auf einer Festplatte kein Speicherplatz mehr vorhanden ist. Das **STG** -Präfix gibt den Speicherplatz an, der **E** gibt an, dass der Statuscode einen Fehler darstellt und der **mediumfull** bestimmte Informationen über den Fehler enthält. Viele der Werte, die Sie möglicherweise von einer Schnittstellen Methode oder Funktion zurückgeben möchten, sind in WinError. h definiert.

Weitere Informationen zur Fehlerbehandlung finden Sie in den folgenden Abschnitten:

-   [Struktur von com-Fehler Codes](structure-of-com-error-codes.md)
-   [Codes in der \_ Einrichtung der Einrichtung](codes-in-facility-itf.md)
-   [Verwenden von Makros für die Fehlerbehandlung](using-macros-for-error-handling.md)
-   [COM-Fehlerbehandlung in Java und Visual Basic](com-error-handling-in-java-and-visual-basic.md)
-   [Fehlerbehandlungsstrategien](error-handling-strategies.md)
-   [Behandeln von unbekannten Fehlern](handling-unknown-errors.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Fehler Codes](com-error-codes.md)
</dt> </dl>

 

 




