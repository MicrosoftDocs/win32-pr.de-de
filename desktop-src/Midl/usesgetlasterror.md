---
title: usesgetlasterror-Attribut
description: Das Attribut \usesgetlasterror\ signalisiert dem Aufrufer, dass er GetLastError aufrufen kann, um den Fehlercode abzurufen.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- usesgetlasterror attribute MIDL
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239486792eb218d51c305f9955331e90c6c165586153dab167f2e19d3a0324e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641035"
---
# <a name="usesgetlasterror-attribute"></a>usesgetlasterror-Attribut

Das **\[ usesgetlasterror-Attribut \]** signalisiert dem Aufrufer, dass er [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen kann, um den Fehlercode abzurufen.

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*module-attributes* 
</dt> <dd>

Null oder mehr MIDL-Attribute, die auf das Modul angewendet [**werden.**](module.md)

</dd> <dt>

*Modulname* 
</dt> <dd>

Der Bezeichnername des [**Moduls**](module.md).

</dd> <dt>

*entry-id* 
</dt> <dd>

Gibt den Moduleinstiegspunkt–Funktionsnamen oder die Ganzzahl-ID an.

</dd> <dt>

*other-attributes* 
</dt> <dd>

Null oder mehr MIDL-Attribute, die auf die Remoteprozedur angewendet werden.

</dd> <dt>

*return-type* 
</dt> <dd>

Der Typ der Daten, die von der Remoteprozedur nach Abschluss des Vorgangs zurückgeben werden.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Der Name der Remoteprozedur, wie in der IDL-Datei definiert.

</dd> <dt>

*param-list* 
</dt> <dd>

Null oder mehr Parameter für die Remoteprozedur.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ usesgetlasterror-Attribut \]** kann für einen Moduleinstiegspunkt festgelegt werden, wenn dieser Einstiegspunkt die Windows [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) verwendet, um Fehlercodes zurück zu geben. Das -Attribut teilt dem Aufrufer mit, dass der Aufrufer [**getLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen kann, wenn beim Aufrufen dieser Funktion ein Fehler auftritt, um den Fehlercode abzurufen.

## <a name="examples"></a>Beispiele

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 