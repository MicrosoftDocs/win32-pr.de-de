---
title: id-Attribut
description: Das \id\-Attribut gibt eine DISPID für eine Memberfunktion an (entweder eine Eigenschaft oder eine Methode in einer Schnittstelle oder Dispinterface).
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- ID-Attribut MIDL
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4d783265ebfcf9dca454c80c39031dc0c37dfb63a8749b4d0e6299a510d91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643066"
---
# <a name="id-attribute"></a>id-Attribut

Das **\[ id-Attribut \]** gibt eine DISPID für eine Memberfunktion an (entweder eine Eigenschaft oder eine Methode in einer Schnittstelle oder Dispinterface).

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*id-num* 
</dt> <dd>

DISPID für die Funktion.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Gibt eine Liste von null oder mehr MIDL-Schnittstellenattributen an.

</dd> <dt>

*rückgabetyp* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion in der IDL-Datei an.

</dd> <dt>

*optional-parameter-list* 
</dt> <dd>

Null oder mehr Funktionsparameter.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie das **\[ \] id-Attribut,** wenn Sie einer Methode oder Eigenschaft eine Standard-DISPID (z.B. DISPID \_ VALUE, DISPID \_ NEWENUM usw.) zuweisen möchten oder wenn Sie Ihr eigenes **IDispatch::Invoke** implementieren, anstatt an **DispInvoke** / **ITypeInfo::Invoke** zu delegieren.

Wenn Sie das **\[ ID-Attribut \]** nicht für eine Schnittstelle verwenden, weist der MIDL-Compiler Ihnen eine DISPID zu. Wenn Sie jedoch eine Disp-Schnittstelle mithilfe von Eigenschaften und Methoden angeben, müssen Sie eine DISPID für jede Eigenschaft und Methode angeben.

*Id-num* ist ein positiver 32-Bit-Ganzzahlwert. Negative IDs sind für die Verwendung durch Automation reserviert.

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

[**Schnittstelle**](interface.md)
</dt> <dt>

[**Dispatchschnittstelle**](dispinterface.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 