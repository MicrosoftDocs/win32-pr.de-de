---
title: Co-Klasse-Attribut
description: Die Co-Klasse-Anweisung stellt eine Auflistung der unterstützten Schnittstellen für ein Komponenten Objekt bereit.
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- Co-Klasse-Attribut-Mittel l
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390252"
---
# <a name="coclass-attribute"></a>Co-Klasse-Attribut

Die **Co-Klasse** -Anweisung stellt eine Auflistung der unterstützten Schnittstellen für ein Komponenten Objekt bereit.

``` syntax
[
    coclass-attribute-list
]
coclass classname
{
    [
        interface-attributes
    ] 
    [interface | dispinterface] interfacename 
    {
  . . . 
    }
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*coclass-Attribute-List* 
</dt> <dd>

Das **\[** [**UUID**](uuid.md) - **\]** Attribut ist für eine **Co-Klasse** erforderlich. Dabei handelt es sich um dieselbe **\[ UUID \]** , die in der System Registrierungsdatenbank als CLSID registriert ist. Die **\[** Attribute [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**lizenzierte**](licensed.md) **\]** , **\[** [**Version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** und **\[** [**appobject**](appobject.md) **\]** werden vor einer **Co-Klassen** Definition akzeptiert, jedoch nicht erforderlich.

</dd> <dt>

*classname* 
</dt> <dd>

Der Name, mit dem das allgemeine Objekt in der Typbibliothek bekannt ist.

</dd> <dt>

*Interface-Attribute* 
</dt> <dd>

Optionale Attribute für die Schnittstelle oder die dispinterface. Die **\[** Attribute [**Quelle**](source.md) **\]** , **\[** [**default**](default.md) **\]** und **\[** [**restricted**](restricted.md) **\]** werden für eine Schnittstelle oder eine dispinterface innerhalb einer **Co-Klasse** akzeptiert.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Entweder eine Schnittstelle, die mit dem Schlüsselwort " [**Interface**](interface.md) " deklariert wurde, oder eine mit dem Schlüsselwort " [**dispinterface**](dispinterface.md) " deklarierte

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Microsoft-Component Object Model definiert eine Klasse als eine-Implementierung, die **QueryInterface** zwischen einem Satz von Schnittstellen zulässt.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("A class"), 
    helpcontext(2481), appobject
] 
coclass myapp 
{ 
    [source] interface IMydocfuncs : IUnknown; 
    dispinterface DMydocfuncs; 
}; 
 
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
coclass mycoclass 
{ 
    [restricted] interface iface1; 
    interface iface2; 
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**appobject**](appobject.md)
</dt> <dt>

[**Steuerelement**](control.md)
</dt> <dt>

[**vorgegebene**](default.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**verbirgt**](hidden.md)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[**lizenziert**](licensed.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**begrenz**](restricted.md)
</dt> <dt>

[**Ausgangs**](source.md)
</dt> <dt>

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**UUID**](uuid.md)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 