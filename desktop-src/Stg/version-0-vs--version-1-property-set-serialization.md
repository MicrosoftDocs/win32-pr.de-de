---
title: Eigenschaftensetserialisierung
description: Es gibt zwei Versionen des Eigenschaften Satz-Serialisierungsformats.
ms.assetid: 10544118-5e80-47e2-b75b-c1a43be15b2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c635728e169cdddb20437323a49a18496b3459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209276"
---
# <a name="property-set-serialization"></a>Eigenschaftensetserialisierung

Es gibt zwei Versionen des Eigenschaften Satz-Serialisierungsformats. Die ursprüngliche Spezifikation beschreibt Version 0 des Formats. Weitere Informationen finden Sie unter [Format Version](format-version.md) . In Version 1 wird die ursprüngliche Version erweitert. Alle Eigenschaften Sätze der Version 0 sind als Eigenschaften Sätze der Version 1 gültig. Das Feld **Format Version** in der Kopfzeile eines serialisierten Eigenschaften Satzes gibt die Version an.

In den folgenden Elementen werden die Unterschiede zwischen den Eigenschaften Satz-Serialisierungsformaten der Versionen 0 und Version 1 identifiziert.

-   Unterstützung für neue **VarType** -Werte. Weitere Informationen zu **VarType** -Werten und deren Verwendung finden Sie im Thema [IDispatch-Datentypen und-Strukturen]( /previous-versions/ms221600(v=vs.100)) und die [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur.

    Die folgenden **VarType** -Werte werden in den Eigenschaften Sätzen der Version 0 nicht unterstützt, werden jedoch in Version 1 unterstützt:

    VT \_ I1

    VT \_ Vector \| VT \_ I1

    VT \_ int

    VT \_ uint

    VT ( \_ dezimal)

    Außerdem können SAFEARRAYs in einem Eigenschaften Satz serialisiert werden. Das vorhanden sein eines SAFEARRAY wird durch das VT- \_ Array Bit in Kombination mit einem **or** -Vorgang und den Array Elementen im **VT** -Member der [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur angegeben. Ein SafeArray von 4-Byte-Ganzzahlen mit Vorzeichen weist z. b. den Typ "VT \_ array \| VT I4" auf \_ .

    Die folgenden Elementtypen sind für ein SAFEARRAY in einem serialisierten Eigenschaften Satz gültig:



|             |          |             |           |
|-------------|----------|-------------|-----------|
| VT \_ I1      | VT \_ UI1  | VT \_ I2      | VT \_ UI2   |
| VT \_ I4      | VT \_ UI4  | VT \_ int     | VT \_ uint  |
| VT \_ R4      | VT \_ R8   | VT- \_ CY      | VT- \_ Datum  |
| VT \_ BSTR    | VT \_ bool | VT ( \_ dezimal) | VT- \_ Fehler |
| VT- \_ Variante |          |             |           |



 

Wenn der \_ Datentyp VT Variant angegeben ist, weist dies darauf hin, dass das SAFEARRAY selbst [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Strukturen enthält. Die Typen für diese Elemente müssen aus der vorangehenden Liste bestehen, mit dem Unterschied, dass Sie keine geschposteten VT-Typen enthalten können \_ .

Beachten Sie, dass Implementierungen von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) in der Lage sein müssen, ordnungsgemäß wiederherzustellen, indem ein Fehler zurückgegeben wird, wenn ein neuer Typ gefunden wird. beispielsweise varenumerationstypen.

-   Die Groß-/Kleinschreibung beachten Eigenschaftsnamen, z. b. die in der [**IPropertyStorage:: schreitepropertynames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames) -Methode angegebenen, unterliegen in den Eigenschaften Sätzen der Version 0 nicht zwischen Groß-und Kleinschreibung. In Eigenschaften Sätzen der Version 1 kann für Eigenschaftsnamen die Groß-/Kleinschreibung beachtet werden, abhängig vom Wert der neuen Behavior-Eigenschaft.

    Die Behavior-Eigenschaft ist die eigen [schafts-ID 0x80000003](/windows/desktop/Stg/reserved-property-identifiers) mit dem Typ VT \_ UI4. Wenn das niedrigste Bit dieses Werts festgelegt ist, wird bei den Eigenschaften Satz Namen die Groß-/Kleinschreibung beachtet. Legen Sie das Flag propsetflag \_ für die Groß-/Kleinschreibung \_ im *grfFlags* -Parameter der [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) -Methode fest, um einen Eigenschaften Satz mit Berücksichtigung von Groß-/Kleinschreibung

-   Lange Eigenschaftsnamen. Eigenschaftsnamen für Eigenschaften Sätze der Version 0 müssen kleiner oder gleich 256 Zeichen (einschließlich des Zeichen folgen Abschluss Zeichens) für Eigenschaften Sätze in der Unicode-Codepage sein. Wenn Sie sich nicht auf der Unicode-Codepage befinden, müssen Sie weniger als 256 Bytes aufweisen. Die Eigenschaften Sätze der Version 1 können auf der anderen Seite Eigenschaftsnamen mit unbegrenzter Länge aufweisen, obwohl Sie weiterhin durch die Gesamtgröße des Eigenschaften Satzes von 256 Kilobyte (KB) beschränkt sind.

Es wird empfohlen, dass Implementierungen von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) standardmäßig Standardeigenschaften Sätze von Version 0 erstellen und verwalten. Wenn ein Aufrufer anschließend eine bestimmte Funktion für das Format Version 1 anfordert, sollte die Version des Eigenschaften Satzes nur dann aktualisiert werden. Wenn z. b. eine Eigenschaft vom Typ "VT \_ Array" geschrieben wird oder wenn ein Name für eine lange Eigenschaft geschrieben wird, sollte die Implementierung das Eigenschaften Satz Format auf Version 1 aktualisieren. Eine Ausnahme von dieser Richtlinie tritt auf, wenn der Wert "propsetflag \_ Case \_ sensitive Enumeration" im [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)-Befehl angegeben wird. In diesem Fall muss der Eigenschaften Satz als Eigenschaften Satz der Version 1 erstellt werden.

 

 