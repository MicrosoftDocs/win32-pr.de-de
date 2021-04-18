---
title: benutzerdefiniertes Attribut
description: Das \ Custom \-Attribut erstellt ein benutzerdefiniertes Attribut.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- benutzerdefiniertes Attribut-Mittel l
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7c4210091cc028d7724cb40724f22a91eb7d74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340696"
---
# <a name="custom-attribute"></a>benutzerdefiniertes Attribut

Das benutzerdefinierte Attribut erstellt ein benutzerdefiniertes Attribut. **\[ \]**

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Attribut-ID* 
</dt> <dd>

Die GUID für das benutzerdefinierte Attribut.

</dd> <dt>

*Attribut-Wert* 
</dt> <dd>

Der Wert, den das Attribut enthält. Der Wert muss ein Typ sein, der in einen Variant-Typ eingefügt werden kann.

</dd> <dt>

*Attribut-List* 
</dt> <dd>

Andere Attribute, z **\[** . b. [**UUID**](uuid.md) **\]** und **\[** [**HelpString**](helpstring.md) **\]** , die auf dieses Element angewendet werden.

</dd> <dt>

*Elementtyp* 
</dt> <dd>

Der Typ des Elements, auf das das benutzerdefinierte Attribut angewendet wird. Dabei kann es sich um eine Bibliotheks Anweisung, Typinformationen, eine Variable, eine Funktion oder einen Parameter handeln. Ein benutzerdefiniertes Attribut kann nicht für einen Member einer Co-Klasse verwendet werden.

</dd> <dt>

*Elementname* 
</dt> <dd>

Der Name des Elements.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie das **\[ benutzerdefinierte \]** Attribut, um ein eigenes Attribut zu definieren. Beispielsweise können Sie ein Attribut mit Zeichen folgen Wert erstellen, das die ProgID für eine Klasse übergibt.

Um einen benutzerdefinierten Attribut Wert abzurufen, rufen Sie einen der folgenden Werte auf:

-   ITypeLib2:: GetCustData (rguid, pvarval)
-   ITypeInfo2:: GetCustData (rguid, pvarval)
-   ITypeInfo2:: GetFuncCustData (Index, rguid, pvarval)
-   ITypeInfo2:: GetVarCustData (Index, rguid, pvarval)
-   ITypeInfo2:: GetParamCustData (indexfunc, indexparam, rguid, pvarval)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Bibliothek**](library.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**UUID**](uuid.md)
</dt> </dl>

 

 