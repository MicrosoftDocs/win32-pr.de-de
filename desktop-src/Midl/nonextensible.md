---
title: nonextensible-Attribut
description: Das \nonextensible\-Attribut gibt an, dass die IDispatch-Implementierung nur die In der Schnittstellenbeschreibung aufgeführten Eigenschaften und Methoden enthält und zur Laufzeit nicht mit zusätzlichen Membern erweitert werden kann.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- Nicht überdehnbares Attribut MIDL
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96c4e55cf5cf2c05ff9c3619b19e7a9b0582f3cf64bc0f9a711fb1af274bfb9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066879"
---
# <a name="nonextensible-attribute"></a>nonextensible-Attribut

Das **\[ nicht erweiterbare \]** Attribut gibt an, dass die [**IDispatch-Implementierung**](/windows/win32/api/oaidl/nn-oaidl-idispatch) nur die In der Schnittstellenbeschreibung aufgeführten Eigenschaften und Methoden enthält und zur Laufzeit nicht mit zusätzlichen Membern erweitert werden kann. (Standardmäßig geht Automation davon aus, dass Schnittstellen zur Laufzeit Member hinzufügen können, d. h., sie sind erweiterbar.)

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

*uuid-number* 
</dt> <dd>

Gibt eine universell eindeutige ID für die [**Schnittstelle an.**](interface.md)

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Gibt eine Liste von null oder mehr MIDL-Schnittstellenattributen an.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Gibt den Namen der [**Schnittstelle**](interface.md) oder [**Disp-Schnittstelle**](dispinterface.md)an.

</dd> <dt>

*Schnittstellendefinition* 
</dt> <dd>

Gibt IDL-Anweisungen an, die die Definition der [**Schnittstelle**](interface.md) oder [**Dispinterface**](dispinterface.md)bilden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können das **\[ nicht erweiterbare \]** Attribut entweder auf eine Schnittstelle oder eine Disp-Schnittstelle anwenden. Eine Schnittstelle muss jedoch auch über die Attribute **\[** [**dual**](dual.md) **\]** und **\[** [**oleautomation**](oleautomation.md) **\]** verfügen.

### <a name="flags"></a>Flags

TYPEFLAG \_ FNONEXTENSIBLE

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

[**Dispatchschnittstelle**](dispinterface.md)
</dt> <dt>

[**Dual**](dual.md)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**Typeflags**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 