---
title: defaultbind-Attribut
description: Das Attribut \defaultbind\ gibt die einzelne bindbare Eigenschaft an, die das Objekt am besten darstellt.
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- DEFAULTBIND-Attribut MIDL
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a981d0469219a32b5931507f5df6d742e84fa67e6676e44c24edfb823f521a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807296"
---
# <a name="defaultbind-attribute"></a>defaultbind-Attribut

Das **\[ defaultbind-Attribut \]** gibt die einzelne bindbare Eigenschaft an, die das Objekt am besten darstellt.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Gibt eine Liste mit einem oder mehr Attributen an, die für die Schnittstelle als Ganzes gelten. Wenn mindestens zwei Schnittstellenattribute vorhanden sind, müssen sie durch Kommas getrennt werden.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Attributliste* 
</dt> <dd>

Gibt eine Liste von Attributen an, die für die Funktion gelten. Wenn mindestens zwei Schnittstellenattribute vorhanden sind, müssen sie durch Kommas getrennt werden.

</dd> <dt>

*returntype* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion an, auf die **\[ das defaultbind-Attribut \]** angewendet wird.

</dd> <dt>

*params* 
</dt> <dd>

Funktionsparameterliste.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eigenschaften, die über das **\[ defaultbind-Attribut \]** verfügen, müssen auch über das **\[** [**bindbare Attribut**](bindable.md) **\]** verfügen. Nur eine Eigenschaft in einer Schnittstelle oder Disp-Schnittstelle kann das **\[ defaultbind-Attribut \]** haben.

Dieses Attribut wird von Containern verwendet, die über ein Benutzermodell mit Bindung an ein Objekt verfügen, anstatt an eine Eigenschaft eines Objekts zu binden. Ein Objekt kann die Datenbindung unterstützen, aber nicht über dieses Attribut verfügen.

### <a name="flags"></a>Flags

FUNCFLAG \_ FDEFAULTBIND, VARFLAG \_ FDEFAULTBIND

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 