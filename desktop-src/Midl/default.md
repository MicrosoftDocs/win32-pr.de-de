---
title: Standardattribut
description: Das \default\-Attribut Gibt an, dass die schnittstelle oder dispinterface, die in einer Co-Klasse definiert ist, die Standardprogrammierbarkeitsschnittstelle darstellt. Dieses Attribut ist für die Verwendung durch Makrosprachen vorgesehen.
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- MIDL-Standardattribut
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea717048a89c626ef19d5b1c41fcd558a163f7b4ade9c05eee0e3ea362d50ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013938"
---
# <a name="default-attribute"></a>Standardattribut

Das **\[ Standardattribut \]** Gibt an, dass die [**Schnittstelle**](interface.md) oder [**Dispinterface,**](dispinterface.md)die in einer [**Co-Klasse**](coclass.md)definiert ist, die Standardprogrammierbarkeitsschnittstelle darstellt. Dieses Attribut ist für die Verwendung durch Makrosprachen vorgesehen.

``` syntax
[
    uuid(uuid-number) 
    [, attribute-list]
] 
coclass coclass-name
{
    [ default [, optional-interface-attribute] ]; 
    interface | dispinterface interface-name;
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*uuid-number* 
</dt> <dd>

Gibt eine universell eindeutige ID für die [**Co-Klasse**](coclass.md)an.

</dd> <dt>

*Attributliste* 
</dt> <dd>

Gibt zusätzliche [**Co-Klassenattribute**](coclass.md) an. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*coclass-name* 
</dt> <dd>

Gibt den Namen an, mit dem andere Softwarekomponenten auf diese [**Co-Klasse**](coclass.md)verweisen können.

</dd> <dt>

*optional-interface-attribute* 
</dt> <dd>

Das **\[** [](source.md) **\]** Quellattribut, das angibt, dass eine Schnittstelle oder Dispinterface ausgehend ist, ist das einzige andere Attribut, das hier verwendet werden kann.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine [**Co-Klasse**](coclass.md) kann höchstens zwei **\[ Standardmember \]** aufweisen. Eine stellt die ausgehende (Quell-)Schnittstelle oder Disp-Schnittstelle dar, die andere die eingehende Schnittstelle (Senke) oder Disp-Schnittstelle. Wenn das **\[ \] Standardattribut** für keinen Member der **Co-Klasse** oder des **Co-Datentyps** angegeben ist, werden die ersten ausgehenden und eingehenden Member, die nicht über das restricted-Attribut verfügen, **\[** [](restricted.md) **\]** als Standardwerte behandelt.

### <a name="flags"></a>Flags

IMPLTYPEFLAG \_ FDEFAULT

## <a name="examples"></a>Beispiele

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello Class"),appobject
]  
coclass Hello
{
    [default] interface IHello:IUnknown;
    interface IDispatch;
};
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Beschränkt**](restricted.md)
</dt> <dt>

[**Quelle**](source.md)
</dt> </dl>

 

 