---
title: immediatebind-Attribut
description: Das Attribut \immediatebind\ gibt an, dass die Datenbank sofort über alle Änderungen an einer Eigenschaft eines datengebundenen Objekts benachrichtigt wird.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- immediatebind-Attribut MIDL
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40396343177da07a2747c79473cdc52f2d665fea8411f4d6f117a5032d66707a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642976"
---
# <a name="immediatebind-attribute"></a>immediatebind-Attribut

Das **\[ immediatebind-Attribut \]** gibt an, dass die Datenbank sofort über alle Änderungen an einer Eigenschaft eines datengebundenen Objekts benachrichtigt wird.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Gibt eine Liste mit einem oder mehr Attributen an, die für die Schnittstelle als Ganzes gelten.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Gibt den Namen der Schnittstelle [**oder**](interface.md) [**dispinterface an.**](dispinterface.md)

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Null oder mehr Funktionsattribute.

</dd> <dt>

*returntype* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion in der IDL-Datei an.

</dd> <dt>

*params* 
</dt> <dd>

Null oder mehr Funktionsparameter.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Mit **\[ dem \] Attribut immediatebind** können Steuerelemente zwischen Eigenschaften unterscheiden, die die Datenbank über jede Änderung benachrichtigen müssen, und eigenschaften, die dies nicht tun. Beispielsweise sollte jede Änderung eines Kontrollkästchen-Steuerelements sofort an die zugrunde liegende Datenbank gesendet werden, auch wenn das Steuerelement den Fokus nicht verloren hat. Bei einem Listbox-Steuerelement tritt jedoch eine Änderung auf, wenn eine andere Auswahl hervorgehoben wird. Eine Benachrichtigung der Datenbank über eine Änderung, bevor das Steuerelement den Fokus verliert, wäre ineffizient und unnötig. Mit **\[ dem \] Immediatebind-Attribut** können Sie durch Festlegen des ImmediateBind-Bits einzelne Eigenschaften für ein Formular angeben, dessen Änderungen sofort gemeldet werden sollen.

Eigenschaften, die über das **\[ immediatebind-Attribut \]** verfügen, müssen auch über das **\[** [**bindbare Attribut**](bindable.md) **\]** verfügen.

### <a name="flags"></a>Flags

FUNCFLAG \_ FIMMEDIATEBIND, VARFLAG \_ FIMMEDIATEBIND

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**Typeflags**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[**Dispatchschnittstelle**](dispinterface.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 