---
title: nonextensible-Attribut
description: Das \ nonextensible \-Attribut gibt an, dass die IDispatch-Implementierung nur die Eigenschaften und Methoden enthält, die in der Schnittstellen Beschreibung aufgeführt sind, und kann zur Laufzeit nicht mit zusätzlichen Elementen erweitert werden.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- nicht erweiterbares Attribut, Mittel l
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e591ea4ab0647449ca9296b3b14a4aab9fff6991
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339057"
---
# <a name="nonextensible-attribute"></a>nonextensible-Attribut

Das **\[ nonextensible \]** -Attribut gibt an, dass die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Implementierung nur die Eigenschaften und Methoden enthält, die in der Schnittstellen Beschreibung aufgeführt sind, und kann zur Laufzeit nicht mit zusätzlichen Elementen erweitert werden. (In der Standardeinstellung geht es bei der Automatisierung davon aus, dass Schnittstellen Elemente zur Laufzeit hinzufügen können, d. h., Sie sind erweiterbar.)

``` syntax
[
    uuid(uuid-number), 
    nonextensible 
    [, optional-attribute-list]
] 
interface | dispinterface interface-name 
{
    interface-definition
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*UUID-Nummer* 
</dt> <dd>

Gibt eine universell eindeutige Identifikationsnummer für die [**Schnittstelle**](interface.md)an.

</dd> <dt>

*optional-Attribut-List* 
</dt> <dd>

Gibt eine Liste von 0 (null) oder mehr Attributen der Mittelwert Schnittstelle an.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der [**Schnittstelle**](interface.md) oder der " [**dispinterface**](dispinterface.md)" an.

</dd> <dt>

*Schnittstellen Definition* 
</dt> <dd>

Gibt IDL-Anweisungen an, die die Definition der- [**Schnittstelle**](interface.md) oder der [**dispinterface**](dispinterface.md)bilden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können das **\[ nonextensible \]** -Attribut entweder auf eine Schnittstelle oder eine dispinterface anwenden. Eine Schnittstelle muss jedoch auch über die **\[** [**Dual**](dual.md) **\]** -und **\[** [**oleautomation**](oleautomation.md) - **\]** Attribute verfügen.

### <a name="flags"></a>Flags

TYPEFLAG- \_ nicht erweiterbar

## <a name="examples"></a>Beispiele

``` syntax
library Hello
{
    [
        uuid(12345678-1234-1234-1234-123456789ABC), 
        helpstring("A helpful description."),
        oleautomation, 
        dual, 
        nonextensible
    ] 
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Inhalt einer Typbibliothek](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**Ales**](dual.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**FUNCFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 