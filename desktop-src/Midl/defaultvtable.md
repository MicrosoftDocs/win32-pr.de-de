---
title: defaultvtable-Attribut
description: Das Attribut \defaultvtable\ definiert eine Schnittstelle als Vtable-Standardschnittstelle.
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- defaultvtable-Attribut MIDL
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffebc5907072f7fdfc539bbc2b06bf1e4ad9fb667826c6c3c5a96121b106326e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067340"
---
# <a name="defaultvtable-attribute"></a>defaultvtable-Attribut

Das **\[ \] defaultvtable-Attribut** definiert eine Schnittstelle als VTable-Standardschnittstelle.

``` syntax
[
    coclass-attribute-list, 
    defaultvtable
]
coclass coclass-name
{
    coclass-interface-list
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*coclass-attribute-list* 
</dt> <dd>

Andere Attribute, die für die -Klasse gelten. Die **\[** [**Attribute source**](source.md) **\]** und **\[** [**uuid**](uuid.md) sind **\]** erforderlich.

</dd> <dt>

*coclass-name* 
</dt> <dd>

Der Name der Klasse.

</dd> <dt>

*coclass-interface-list* 
</dt> <dd>

Eine Liste der Schnittstellen für die -Klasse.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine VTable-Standardschnittstelle kann keine Disp-Schnittstelle sein– sie muss eine duale, Vtable- oder -Schnittstelle sein. Wenn es sich bei der Schnittstelle um eine duale Schnittstelle handelt, können Senken davon ausgehen, dass sie Ereignisse über Vtable empfangen.

Eine Klasse kann sowohl eine Standardquellschnittstelle als auch eine VTable-Standardquellschnittstelle sein, wie im Beispiel gezeigt. In diesem Fall sollte eine Empfehlungssenke IID \_ IDISPATCH verwenden, um Dispatchereignisse zu empfangen, und den Schnittstellenbezeichner zum Empfangen von Vtable-Ereignissen verwenden.

### <a name="typeflag-representation"></a>Typflagdarstellung

Das Vorhandensein von IMPLTYPEFLAG \_ FDEFAULTVTABLE.

## <a name="examples"></a>Beispiele

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget] HRESULT Backcolor([out, retval] long *Value);
    [propput] HRESULT Backcolor([in] long Value);
    [propget] HRESULT Name([out, retval] BSTR *Value);
    [propput] HRESULT Name([in] BSTR Value);}

[
    dual,
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    restricted
]
interface IFormEvents: IDispatch
{
    HRESULT Click();
    HRESULT Resize();}

    [
        uuid(1e123456-1f3c-1069-996b-123456789ABC)
    ]
    coclass Form
    {
        [default] interface IForm;
        [default, defaultvtable, source] interface IFormEvents;
    }
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Quelle**](source.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 