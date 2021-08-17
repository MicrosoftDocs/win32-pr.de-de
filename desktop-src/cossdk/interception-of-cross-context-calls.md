---
description: Wenn ein Objekt in einem bestimmten Kontext aktiviert wird, werden nachfolgende Aufrufe von oder von ihm innerhalb des Kontexts anders behandelt als Aufrufe über die Kontextgrenze hinweg.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Abfangen kontextübergreifender Aufrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a969479419b75313f8b439f3cf9ffc7b94946e9007752ccc4e99a54cd6ad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547837"
---
# <a name="interception-of-cross-context-calls"></a>Abfangen kontextübergreifender Aufrufe

Wenn ein Objekt in einem bestimmten Kontext aktiviert wird, werden nachfolgende Aufrufe von oder von ihm innerhalb des Kontexts anders behandelt als Aufrufe über die Kontextgrenze hinweg. Aufrufe über die Kontextgrenze hinweg werden mit einfachen Proxys verarbeitet. Diese Proxys verarbeiten alles, was erforderlich ist, um die Laufzeitumgebung von einer Umgebung, die den Aufrufer aufnehmen kann, auf einen für den Aufrufer anzupassen. Dieser Prozess wird als *Abfangen bezeichnet.*

Kontextübergreifendes Abfangen von Aufrufen ist erforderlich, da Objekte in unterschiedlichen Kontexten unterschiedliche Laufzeitanforderungen haben. Dies ist genau der Grund für Kontexte. COM+ fängt alle Objektverweise ab, die Sie als Methodenparameter übergeben, und konvertiert sie automatisch in Proxys, damit sie im neuen Kontext verwendet werden können.

Wenn Sie Objektverweise über Kontextgrenzen hinweg auf andere Mittel freigeben , z. B. in globalen Variablen, sollten Sie immer [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) und [**CoUnmarshalInterface verwenden.**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) Diese Funktionen können einen Objektverweis in einen Proxy übersetzen, der in einem anderen Kontext verwendet werden kann. Geben Sie niemals einen unformatten Objektverweis über Kontextgrenzen hinweg weiter.

Das kontextübergreifende Verhalten von Aufrufen kann unerwünschte Folgen haben, wenn Objekte Schnittstellen verfügbar machen, die nicht gemarshallt werden können. In diesem Fall möchten Sie wahrscheinlich dazu kommen, dass das Objekt, das nicht gemarshallt werden kann, nur im Kontext des Aufrufers und nie in seinem eigenen Kontext aktiviert werden kann. Wählen Sie hierzu auf der Registerkarte Aktivierung der Eigenschaftenseite der  Komponente die Option Muss **im** Kontext des Aufrufers **aktiviert werden** aus. (Eine [Schritt-für-Schritt-Anleitung finden](enforcing-activation-in-the-caller-s-context.md) Sie unter Erzwingen der Aktivierung im Kontext des Aufrufers.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kontextaktivierung](context-activation.md)
</dt> </dl>

 

 
