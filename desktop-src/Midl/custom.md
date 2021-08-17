---
title: benutzerdefiniertes Attribut
description: Das Attribut \custom\ erstellt ein benutzerdefiniertes Attribut.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- MIDL des benutzerdefinierten Attributs
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace6a558da428da07a432653391e0e48b7a5545bb1a83eb40d9c950abfa9d9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643669"
---
# <a name="custom-attribute"></a>benutzerdefiniertes Attribut

Das **\[ benutzerdefinierte \]** Attribut erstellt ein benutzerdefiniertes Attribut.

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*attribute-id* 
</dt> <dd>

Die GUID für das benutzerdefinierte Attribut.

</dd> <dt>

*attribut-value* 
</dt> <dd>

Der Wert, den das Attribut enthält. Der Wert muss ein Wert sein, der in einen VARIANT-Typ verwendet werden kann.

</dd> <dt>

*Attributliste* 
</dt> <dd>

Andere Attribute wie **\[** [**uuid**](uuid.md) **\]** und **\[** [**helpstring**](helpstring.md) **\]** , die für dieses Element gelten.

</dd> <dt>

*element-type* 
</dt> <dd>

Der Typ des Elements, auf das das benutzerdefinierte Attribut angewendet wird. Dies kann eine Bibliotheks-Anweisung, Typinformationen, eine Variable, eine Funktion oder ein Parameter sein. Sie können kein benutzerdefiniertes Attribut für einen Member einer Co-Klasse verwenden.

</dd> <dt>

*Elementname* 
</dt> <dd>

Der Name des Elements.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie das **\[ benutzerdefinierte \]** Attribut, um Ihr eigenes Attribut zu definieren. Beispielsweise können Sie ein Zeichenfolgenwertattribut erstellen, das die ProgID für eine Klasse angibt.

Um einen benutzerdefinierten Attributwert abzurufen, rufen Sie einen der folgenden Aufrufe auf:

-   ITypeLib2::GetCustData(rguid, pvarVal)
-   ITypeInfo2::GetCustData(rguid, pvarVal)
-   ITypeInfo2::GetFuncCustData(index, rguid, pvarVal)
-   ITypeInfo2::GetVarCustData(index, rguid, pvarval)
-   ITypeInfo2::GetParamCustData(indexFunc, indexParam, rguid, pvarVal)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Bibliothek**](library.md)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 