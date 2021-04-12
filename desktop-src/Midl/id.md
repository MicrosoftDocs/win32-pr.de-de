---
title: id-Attribut
description: Das Attribut \ ID \ gibt eine DISPID für eine Element Funktion an (entweder eine Eigenschaft oder eine Methode in einer Schnittstelle oder einer dispinterface).
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- ID-Attribut-Mittel l
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c57d8ea818bbd7b8fd5bd35816e6b7227eb917
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390175"
---
# <a name="id-attribute"></a>id-Attribut

Das **\[ ID \]** -Attribut gibt eine DISPID für eine Element Funktion an (entweder eine Eigenschaft oder eine Methode in einer Schnittstelle oder einer dispinterface).

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*ID-num* 
</dt> <dd>

DISPID für die Funktion.

</dd> <dt>

*optional-Attribut-List* 
</dt> <dd>

Gibt eine Liste von 0 (null) oder mehr Attributen der Mittelwert Schnittstelle an.

</dd> <dt>

*Rückgabetyp* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion in der IDL-Datei an.

</dd> <dt>

*Optional-Parameter-List* 
</dt> <dd>

NULL oder mehr Funktionsparameter.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie das **\[ ID \]** -Attribut, wenn Sie einer Methode oder Eigenschaft eine Standard-DISPID (z. b. DISPID- \_ Wert, DISPID-Diagramm \_ usw.) zuweisen möchten, oder wenn Sie einen eigenen **IDispatch::** -Aufruf implementieren, anstatt zu delegieren, um / **ITypeInfo:: Aufrufen** zu lösen.

Wenn Sie das **\[ ID \]** -Attribut nicht für eine Schnittstelle verwenden, weist der mittlerer l-Compiler eine "DISPID" zu. Wenn Sie jedoch eine dispinterface mithilfe von Eigenschaften und Methoden angeben, müssen Sie für jede Eigenschaft und Methode eine DISPID angeben.

Die *ID-num* ist ein positiver ganzzahliger Wert von 32 Bit. Negative IDs sind für die Verwendung durch Automation reserviert.

## <a name="examples"></a>Beispiele

``` syntax
interface IKnown : IUnknown
{
    properties:
        [id(90), propget, 
         helpstring("A meaningful comment."] long Func1(void);

    /* Other interface statements */
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 