---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: In den Schlüsselwörtern des Druck Schemas definierte Objekte und Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2347c73dd647f90a88821658cdcf9e2ed846e83
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219053"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a>In den Schlüsselwörtern des Druck Schemas definierte Objekte und Namen

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Das Print Schema-Framework definiert einen Namespace, der die in den Schlüsselwörtern des Druck Schemas definierten Elemente und XML-Attribute enthält. Dies schließt Elemente wie "Feature", "Option" und "ScoredProperty;" ein. Attributnamen wie "Name" und "propagieren" und Werte für XML-Attribute wie z. b. eingeschränkt. Anders ausgedrückt: jede Verwendung eines Namens, der in den Schlüsselwörtern des Druck Schemas definiert ist, muss explizit mit diesem Namespace qualifiziert werden oder implizit mit diesem Namespace verknüpft werden, indem ein xmlns-Standard Attribut verwendet wird. Das Dokument mit dem Schlüsselwort "Print Schema" definiert die öffentlichen Element Instanzen, die möglicherweise in einem beliebigen Kontext oder Speicherort vorkommen. Element Instanzen dürfen nur innerhalb des Kontexts oder des Speicher Orts angezeigt werden, der im Druck Schema Framework festgelegt ist. Beispielsweise muss die <PSF: Option Name = "PSK: Letter" > Instanz, die in den Schlüsselwörtern des Druck Schemas definiert ist, innerhalb der <PSF: Feature Name = "PSK: PageMediaSize" >-Instanz (auch in den Schlüsselwörtern des Druck Schemas definiert) angezeigt werden. Sie haben keine Möglichkeit, eine angegebene Options Instanz außerhalb des angegebenen Kontexts zu verwenden.

Privat definierte Element Instanzen können beliebig angezeigt werden, solange der Elementtyp in einem Kontext angezeigt wird, der vom Druck Schema Framework zugelassen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



