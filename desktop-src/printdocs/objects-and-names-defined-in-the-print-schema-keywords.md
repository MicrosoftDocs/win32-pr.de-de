---
description: Das Druckschemaframework definiert einen Namespace, der die in den Druckschemaschlüsselwörtern definierten Elemente und XML-Attribute enthält.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: In den Druckschemaschlüsselwörtern definierte Objekte und Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aabdac90de6743388ca1f4d44e1ad52c020dbd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408553"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a>In den Druckschemaschlüsselwörtern definierte Objekte und Namen

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Das Druckschemaframework definiert einen Namespace, der die in den Druckschemaschlüsselwörtern definierten Elemente und XML-Attribute enthält. Dies schließt Elemente wie Feature, Option und ScoredProperty ein. Attributnamen wie name und propagate; - und -Werte für XML-Attribute, z. B. eingeschränkt. Anders ausgedrückt: Jede Verwendung eines Namens, der in den Schlüsselwörtern des Druckschemas definiert ist, sollte explizit mit diesem Namespace qualifiziert werden oder diesem Namespace implizit durch die Verwendung eines xmlns-Standardattributs zugeordnet werden. Das Dokument Print Schema Keywords definiert die öffentlichen Elementinstanzen, die in einem kontext- oder orts angegebenen Kontext angezeigt werden können. Elementinstanzen dürfen nur innerhalb des Kontexts oder der Position angezeigt werden, der bzw. der im Druckschemaframework festgelegt ist. Beispielsweise muss die <psf:Option name= "psk:Letter">-Instanz, die in den Schlüsselwörtern des Druckschemas definiert ist, in der <psf:Featurename = "psk:PageMediaSize">-Instanz (auch in den Schlüsselwörtern für Druckschemas definiert) angezeigt werden. Sie haben nicht die Möglichkeit, eine bestimmte Option-Instanz außerhalb des angegebenen Kontexts zu verwenden.

Privat definierte Elementinstanzen können an beliebiger Stelle angezeigt werden, solange der Elementtyp in einem vom Druckschemaframework zugelassenen Kontext angezeigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



