---
title: ausgeblendetes Attribut
description: Das Attribut \ Hidden \ gibt an, dass das Element vorhanden ist, aber nicht in einem benutzerorientierten Browser angezeigt werden sollte.
ms.assetid: bf1f9270-fb93-4421-804e-d56e2c863bbd
keywords:
- Hidden-Attribut, Mittel
topic_type:
- apiref
api_name:
- hidden
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1718351ef84199b60ba720ed2f3569cfa78a0a50
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337645"
---
# <a name="hidden-attribute"></a>ausgeblendetes Attribut

Das **\[ Hidden \]** -Attribut gibt an, dass das Element vorhanden ist, aber nicht in einem benutzerorientierten Browser angezeigt werden sollte.

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

*andere-Attribute* 
</dt> <dd>

NULL oder mehr optionale Mittelwert Attribute.

</dd> <dt>

*gewisses* 
</dt> <dd>

Eine der folgenden Direktiven: " [**Co-Klasse**](coclass.md)", " [**dispinterface**](dispinterface.md)", " [**Interface**](interface.md)" oder " [**Library**](library.md)".

</dd> <dt>

*Elementname* 
</dt> <dd>

Der Name, den andere Softwarekomponenten verwenden können, um das aktuelle Element zu definieren.

</dd> <dt>

*definiert* 
</dt> <dd>

Gibt die-Anweisungen an, die die Element Definition bilden.

</dd> <dt>

*Funktionstyp* 
</dt> <dd>

Der Rückgabetyp der Funktion.

</dd> <dt>

*function-name* 
</dt> <dd>

Der Name, der zum Aufrufen der Funktion verwendet wird.

</dd> <dt>

*Optional-Parameter-List* 
</dt> <dd>

NULL oder mehr Funktionsparameter.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit dem ausgeblendeten Attribut können Sie Elemente aus der Schnittstelle entfernen (indem Sie Sie vor der weiteren Verwendung schützen) und gleichzeitig die Kompatibilität mit vorhandenem Code beibehalten **\[ \]** Sie können das **\[ Hidden \]** -Attribut für Eigenschaften, Methoden und die Anweisungen [**Co-Klasse**](coclass.md), [**dispinterface**](dispinterface.md), [**Interface**](interface.md)und [**Library**](library.md) verwenden.

Wenn es für eine Bibliothek angegeben ist, verhindert das **\[ Hidden \]** -Attribut, dass die gesamte Bibliothek angezeigt wird. Dies ist für die Verwendung mit Steuerelementen vorgesehen. Hosts müssen eine neue Typbibliothek erstellen, die das Steuerelement mit erweiterten Eigenschaften umschließt.

### <a name="flags"></a>Flags

varflag, ausgeblendetes funkflag, ausgeblendetes " \_ \_ TYPEFLAG" \_

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

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[**Bibliothek**](library.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> </dl>

 

 