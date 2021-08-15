---
title: ausgeblendetes Attribut
description: Das \hidden\-Attribut gibt an, dass das Element vorhanden ist, aber nicht in einem benutzerorientierten Browser angezeigt werden sollte.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- AUSGEBLENDETES ATTRIBUT MIDL
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a907a608376d9ad13f97427bd7a941b99221a0f14a6fa9fe35944ced10770b66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384045"
---
# <a name="hidden-attribute"></a>ausgeblendetes Attribut

Das **\[ ausgeblendete \]** Attribut gibt an, dass das Element vorhanden ist, aber nicht in einem benutzerorientierten Browser angezeigt werden sollte.

``` syntax
[
    other-attributes, 
    hidden
] 
element element-name
{
    definitions
}

[other-attributes, hidden] function-type function-name(optional-parameter-list);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*other-attributes* 
</dt> <dd>

Null oder mehr optionale MIDL-Attribute.

</dd> <dt>

*Element* 
</dt> <dd>

Eine der folgenden Direktiven: [**coclass**](coclass.md), [**dispinterface,**](dispinterface.md) [**interface**](interface.md)oder [**library**](library.md).

</dd> <dt>

*Elementname* 
</dt> <dd>

Der Name, den andere Softwarekomponenten verwenden können, um das aktuelle Element abzugrenzen.

</dd> <dt>

*Definitionen* 
</dt> <dd>

Gibt Anweisungen an, die die Elementdefinition bilden.

</dd> <dt>

*Funktionstyp* 
</dt> <dd>

Gibt den Typ der Funktion zurück.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Name, der zum Aufrufen der Funktion verwendet wird.

</dd> <dt>

*optional-parameter-list* 
</dt> <dd>

Null oder mehr Funktionsparameter.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Mit dem **\[ ausgeblendeten \]** Attribut können Sie Member aus ihrer Schnittstelle entfernen (indem Sie sie vor der weiteren Verwendung schützen), während gleichzeitig die Kompatibilität mit vorhandenem Code erhalten bleibt. Sie können das **\[ ausgeblendete \]** Attribut für Eigenschaften, Methoden und die [**Anweisungen coclass**](coclass.md), [**dispinterface,**](dispinterface.md) [**interface**](interface.md)und [**library**](library.md) verwenden.

Wenn es für eine Bibliothek angegeben wird, verhindert das **\[ ausgeblendete \]** Attribut, dass die gesamte Bibliothek angezeigt wird. Dies ist für die Verwendung mit Steuerelementen vorgesehen. Hosts müssen eine neue Typbibliothek erstellen, die das Steuerelement mit erweiterten Eigenschaften umschließt.

### <a name="flags"></a>Flags

VARFLAG \_ HBIDDEN, FUNCFLAG \_ HBIDDEN, TYPEFLAG \_ HBIDDEN

## <a name="examples"></a>Beispiele

``` syntax
[hidden, vararg] SAFEARRAY (int) SecretFunc(
    [in, out] SAFEARRAY (variant) *varP) ;

[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    hidden, 
    version (3.0)
] 
library HiddenLib 
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Dispatchschnittstelle**](dispinterface.md)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[**Bibliothek**](library.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 