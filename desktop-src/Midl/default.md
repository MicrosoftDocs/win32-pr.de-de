---
title: Standardattribut
description: Das \ default \-Attribut gibt an, dass die Schnittstelle oder die dispinterface, die innerhalb einer Co-Klasse definiert ist, die standardmäßige Programmierbarkeits Schnittstelle darstellt Dieses Attribut ist für die Verwendung durch Makro Sprachen vorgesehen.
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- Standard Attribut-Mittell
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2171515bffc41abf2b5fe9a25826c2a71d3939c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472845"
---
# <a name="default-attribute"></a>Standardattribut

Das **\[ Default \]** -Attribut gibt an, dass die [**Schnitt**](interface.md) Stelle oder die in einer [**Co-Klasse**](coclass.md)definierte [**dispinterface**](dispinterface.md)die standardprogrammierbarkeits-Schnittstelle darstellt. Dieses Attribut ist für die Verwendung durch Makro Sprachen vorgesehen.

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

*UUID-Nummer* 
</dt> <dd>

Gibt eine universell eindeutige Identifikationsnummer für die [**Co-Klasse**](coclass.md)an.

</dd> <dt>

*Attribut-List* 
</dt> <dd>

Gibt zusätzliche [**Co-Klasse**](coclass.md) -Attribute an. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Name der Co-Klasse* 
</dt> <dd>

Gibt den Namen an, mit dem andere Softwarekomponenten auf diese [**Co-Klasse**](coclass.md)verweisen können.

</dd> <dt>

*optional-Interface-Attribute* 
</dt> <dd>

Das **\[** [**Quell**](source.md) **\]** Attribut, das angibt, dass eine Schnittstelle oder eine dispinterface ausgehend ist, ist das einzige andere Attribut, das hier verwendet werden kann.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine [**Co-Klasse**](coclass.md) kann höchstens zwei **\[ Standardmember \]** aufweisen. Eine stellt die ausgehende (Quell-) Schnittstelle oder dispinterface dar, während die andere die eingehende Schnittstelle (Senke) oder "dispinterface" darstellt. Wenn das **\[ Default \]** -Attribut für keinen Member der **Co-Klasse** oder des **cotype**-Elements angegeben ist, werden die ersten ausgehenden und eingehenden Member, die nicht über das restricted-Attribut verfügen, **\[** [](restricted.md) **\]** als Standardwerte behandelt.

### <a name="flags"></a>Flags

impltypeflag (Standardwert) \_

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

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**begrenz**](restricted.md)
</dt> <dt>

[**Ausgangs**](source.md)
</dt> </dl>

 

 