---
title: Serialisierung von Eigenschaftensatz
description: Es gibt zwei Versionen des Serialisierungsformats für Eigenschaftensatz.
ms.assetid: 10544118-5e80-47e2-b75b-c1a43be15b2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9412fd2a83ab7c71b97888d4ae7911a96fdc4cfe5a9ebbceb5d985b3a5e2b418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886475"
---
# <a name="property-set-serialization"></a>Serialisierung von Eigenschaftensatz

Es gibt zwei Versionen des Serialisierungsformats für Eigenschaftensatz. Die ursprüngliche Spezifikation beschreibt Version 0 des Formats. Weitere Informationen finden Sie unter [Formatversion.](format-version.md) Version 1 erweitert die ursprüngliche Version. Alle Eigenschaftensätze der Version 0 sind als Eigenschaftensätze der Version 1 gültig. Das Feld **Version formatieren** im Header eines serialisierten Eigenschaftensatzes gibt die Version an.

Die folgenden Elemente identifizieren die Unterschiede zwischen den Serialisierungsformaten für Eigenschaftensätze der Version 0 und Version 1.

-   Unterstützung für neue **VARTYPE-Werte.** Weitere Informationen zu **VARTYPE-Werten** und deren Verwendung finden Sie im Thema [IDispatch-Datentypen und -Strukturen]( /previous-versions/ms221600(v=vs.100)) und in der [**PROPVARIANT-Struktur.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

    Die folgenden **VARTYPE-Werte** werden in Eigenschaftssätzen der Version 0 nicht unterstützt, aber in Version 1:

    VT_I1

    VT_VECTOR \| VT_I1

    VT_INT

    VT_UINT

    VT_DECIMAL

    Darüber hinaus können SafeArrays in einem Eigenschaftensatz serialisiert werden. Das Vorhandensein eines SafeArray wird durch das VT_ARRAY Bit kombiniert, wobei ein **OR-Vorgang** mit den Arrayelementen im **vt-Member** der [**PROPVARIANT-Struktur**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) verwendet wird. Ein SafeArray mit 4-Byte-Ganzzahlen mit Vorzeichen hat beispielsweise den Typ VT_ARRAY \| VT_I4.

    Die folgenden Elementtypen sind für safeArray in einem serialisierten Eigenschaftensatz gültig:

    | <!--tabular list: col headers unnecessary-->  ||||
    |-------------|----------|-------------|-----------|
    | VT_I1       | VT_UI1   | VT_I2       | VT_UI2    |
    | VT_I4       | VT_UI4   | VT_INT      | VT_UINT   |
    | VT_R4       | VT_R8    | VT_CY       | VT_DATE   |
    | VT_BSTR     | VT_BOOL  | VT_DECIMAL  | VT_ERROR  |
    | VT_VARIANT  |          |             |           |
    |             |          |             |           |

    Wenn der VT_VARIANT Datentyp angegeben wird, gibt er an, dass safeArray selbst [**PROPVARIANT-Strukturen**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) enthält. Die Typen für diese Elemente müssen aus der vorherigen Liste stammen, es sei denn, sie dürfen keine geschachtelten VT_VARIANT Typen enthalten.
    
    Beachten Sie, dass Implementierungen von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) ordnungsgemäß wiederhergestellt werden können müssen, indem ein Fehler zurückgegeben wird, wenn ein neuer Typ auftritt. z. B. VARENUM-Typen.

-   Eigenschaftennamen, bei der die Groß-/Kleinschreibung beachtet wird. Bei Eigenschaftsnamen, z.B. den in der [**IPropertyStorage::WritePropertyNames-Methode angegebenen**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames) Namen, wird in Eigenschaftssätzen der Version 0 die Groß-/Kleinschreibung nicht beachtet. In Eigenschaftssätzen der Version 1 kann die Groß-/Kleinschreibung bei Eigenschaftsnamen abhängig vom Wert der neuen Behavior-Eigenschaft beachtet werden.

    Die Behavior-Eigenschaft ist [eigenschaften-ID 0x80000003](/windows/desktop/Stg/reserved-property-identifiers) mit dem Typ VT_UI4. Wenn das niedrigste Bit dieses Werts festgelegt ist, wird bei den Eigenschaftensatznamen die Groß-/Kleinschreibung beachtet. Legen Sie das PROPSETFLAG_CASE_SENSITIVE-Flag im *grfFlags-Parameter* der [**IPropertySetStorage::Create-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) fest, um einen Eigenschaftensatz anzugeben, bei dem die Groß-/Kleinschreibung beachtet wird.

-   Lange Eigenschaftsnamen. Eigenschaftsnamen für Eigenschaftssätze der Version 0 müssen kleiner als oder gleich 256 Zeichen sein, einschließlich des Zeichenfolgenabschlusszeichens, für Eigenschaftssätze auf der Unicode-Codepage. Wenn sie sich nicht auf der Unicode-Codepage befinden, müssen sie kleiner als 256 Bytes sein. Eigenschaftssätze der Version 1 können dagegen Eigenschaftsnamen mit unbegrenzter Länge aufweisen, obwohl sie weiterhin durch die Größenbeschränkung des gesamten Eigenschaftensatzes von 256 Kilobyte (KB) begrenzt sind.

Es wird empfohlen, dass Implementierungen von [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) eigenschaftssätze der Version 0 standardmäßig erstellen und verwalten. Wenn ein Aufrufer anschließend ein Feature anfordert, das für das Format version 1 spezifisch ist, sollte nur die Version des Eigenschaftensatzes aktualisiert werden. Wenn z. B. eine Eigenschaft vom Typ VT_ARRAY geschrieben wird oder wenn ein langer Eigenschaftenname geschrieben wird, sollte die Implementierung das Eigenschaftensatzformat auf Version 1 aktualisieren. Eine Ausnahme von dieser Richtlinie tritt auf, wenn der PROPSETFLAG_CASE_SENSITIVE Enumerationswert im Aufruf von [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)angegeben wird. In diesem Fall muss der Eigenschaftensatz als Eigenschaftensatz der Version 1 erstellt werden.

 

 