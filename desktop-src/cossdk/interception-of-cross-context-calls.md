---
description: Wenn ein Objekt in einem bestimmten Kontext aktiviert wird, werden nachfolgende Aufrufe von oder von ihm innerhalb des Kontexts anders behandelt als Aufrufe über die Kontext Grenze hinweg.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Abfangen von Kontext übergreifenden aufrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d70bc8bff83d02b13656f9854f0e6d16cd4e173
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342259"
---
# <a name="interception-of-cross-context-calls"></a>Abfangen von Kontext übergreifenden aufrufen

Wenn ein Objekt in einem bestimmten Kontext aktiviert wird, werden nachfolgende Aufrufe von oder von ihm innerhalb des Kontexts anders behandelt als Aufrufe über die Kontext Grenze hinweg. Aufrufe über die Kontext Grenze werden mit Lightweight-Proxys verarbeitet. Diese Proxys verarbeiten jede beliebige Vermittlung, die erforderlich ist, um die Laufzeitumgebung von einer zu ändern, die den Aufrufer an den aufgerufenen anpasst. Dieser Prozess wird als *Abfang* Funktion bezeichnet.

Eine Kontext übergreifende Aufruf Abfang Funktion ist erforderlich, da Objekte in verschiedenen Kontexten unterschiedliche Lauf Zeitanforderungen haben – dies ist genau der Grund für den Kontext. Com+ fängt alle Objekt Verweise ab, die Sie als Methoden Parameter übergeben, und konvertiert sie automatisch in Proxys, sodass Sie im neuen Kontext verwendbar sind.

Wenn Sie Objekt Verweise über Kontext Grenzen hinweg auf andere Weise freigeben, z. –. in globalen Variablen – sollten Sie immer [**comarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) und [**zählmarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)verwenden. Diese Funktionen können einen Objekt Verweis in einen Proxy übersetzen, der in einem anderen Kontext verwendbar ist. Geben Sie niemals einen Rohdaten Objekt Verweis über Kontext Grenzen hinweg frei.

Das Verhalten von Aufrufen über den Kontext hinweg kann bei Objekten, die Schnittstellen bereitstellen, die nicht gemarshallt werden können, unerwünschte Folgen haben. In diesem Fall möchten Sie wahrscheinlich darauf hinweisen, dass das Objekt, das nicht gemarshallt werden kann, nur im Kontext seines Aufrufers und nie in seinem eigenen Kontext aktiviert werden kann. Wählen Sie hierzu auf der Seite Komponenten **Eigenschaften** auf der Registerkarte **Aktivierung** die Option muss in der Kontext Option des **Aufrufers aktiviert sein** aus. (Eine Schritt-für-Schritt-Anleitung finden Sie [unter Erzwingen der Aktivierung im Kontext des Aufrufers](enforcing-activation-in-the-caller-s-context.md) .)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kontext Aktivierung](context-activation.md)
</dt> </dl>

 

 
