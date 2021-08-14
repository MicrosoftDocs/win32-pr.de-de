---
title: dispinterface-Attribut
description: Die dispinterface-Anweisung definiert eine Reihe von Eigenschaften und Methoden, für die Sie IDispatch Invoke aufrufen können.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- MIDL des Dispinterface-Attributs
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3df65adc3bfa486907df0465f2fca5a1427f6d0b1eb89b5c02e6f199be71e9e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384667"
---
# <a name="dispinterface-attribute"></a>dispinterface-Attribut

Die **dispinterface-Anweisung** definiert einen Satz von Eigenschaften und Methoden, für die Sie **IDispatch::Invoke** aufrufen können. Eine Disp-Schnittstelle kann durch explizites Auflisten der unterstützten Methoden und Eigenschaften (Syntax 1) oder durch Auflisten einer einzelnen Schnittstelle (Syntax 2) definiert werden.

``` syntax
[
    [attributes]
]
dispinterface dispinterface-name
{
    properties:
        property-list
    methods:
        method-list
};

[
  [attributes]
]
dispinterface dispinterface-name
{
    interface interface-name
};
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*attributes* 
</dt> <dd>

Gibt Attribute an, die für die gesamte **Disp-Schnittstelle** gelten. Die folgenden Attribute werden akzeptiert: **\[** [**helpstring**](helpstring.md) **\]** , **\[** [**helpcontext**](helpcontext.md) **\]** , **\[** [**helpfile**](helpfile.md), **\]** **\[** [**hidden**](hidden.md), **\]** **\[** [**nonextensible**](nonextensible.md), **\]** **\[** [**oleautomation**](oleautomation.md), **\]** **\[** [**restricted**](restricted.md) **\]** , **\[** [**uuid**](uuid.md)und **\]** **\[** [**version**](version.md) **\]** .

</dd> <dt>

*dispinterface-name* 
</dt> <dd>

Der Name, mit dem die **Disp-Schnittstelle** in der Typbibliothek bekannt ist. Dieser Name muss innerhalb der Typbibliothek eindeutig sein.

</dd> <dt>

*property-list* 
</dt> <dd>

(Syntax 1) Eine optionale Liste von Eigenschaften, die vom -Objekt unterstützt werden und in Form von Variablen deklariert werden. Dies ist die Kurzform zum Deklarieren der Eigenschaftenfunktionen in der Methodenliste. Weitere Informationen finden Sie im Abschnitt "Kommentare".

</dd> <dt>

*Methodenliste* 
</dt> <dd>

(Syntax 1) Eine Liste, die einen Funktionsprototyp für jede Methode und Eigenschaft in der **Disp-Schnittstelle** enthält. Eine beliebige Anzahl von Funktionsdefinitionen kann in *methlist* angezeigt werden. Eine Funktion in *methlist* hat die folgende Form:

**\[**_Attribute_ *_\]_* *returntype methname type paramname***(**_params_*_);_*

Die folgenden Attribute werden für eine Methode in einer **Dispinterface** akzeptiert: **\[ helpstring \]**, **\[ helpcontext \]**, **\[** [**propget**](propget.md) **\]** , **\[** [**propput**](propput.md), **\]** **\[** [**propputref**](propputref.md), **\]** **\[** [**string**](string.md)und **\]** **\[** [**lvarg**](vararg.md) **\]** . Wenn **\[ lvarg \]** angegeben wird, muss der letzte Parameter ein **sicheres** Array vom Variant-Typ sein.

Die Parameterliste ist eine durch Kommas getrennte Liste, von der jedes Element die folgende Form hat:

**\[**_Attribute_*_\]_*

Der *Typ* kann ein beliebiger deklarierter oder integrierter Typ oder ein Zeiger auf einen beliebigen Typ sein. Attribute für Parameter sind:

**\[**[**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** , **\[** [**optional,**](optional.md) **\]** **\[ Zeichenfolge \]**

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

(Syntax 2) Der Name der Schnittstelle, die als IDispatch-Schnittstelle deklariert werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der MIDL-Compiler akzeptiert die folgende Parameterreihenfolge (von links nach rechts):

1.  Erforderliche Parameter (Parameter ohne \[ defaultvalue- \] oder \[ optionale \] Attribute)
2.  optionale Parameter mit oder ohne das \[ \] defaultvalue-Attribut,
3.  Parameter mit dem \[ optionalen \] Attribut und ohne das \[ \] defaultvalue-Attribut,
4.  \[[](lcid.md) \] lcid-Parameter, falls vorhanden,
5.  \[[**retval**](retval.md) \] Parameter

Methodenfunktionen werden genau wie auf der Referenzseite für [**das Modul**](module.md) beschrieben angegeben, mit der Ausnahme, dass das \[ [](entry.md) \] Eintragsattribut nicht zulässig ist. Beachten Sie, dass STDOLE32. TLB (STDOLE. TLB auf 16-Bit-Systemen) muss importiert werden, da eine **Disp-Schnittstelle** von IDispatch erbt.

Sie können Eigenschaften entweder in den Eigenschaften- oder Methodenlisten deklarieren. Das Deklarieren von Eigenschaften in der Eigenschaftenliste gibt nicht den Typ des Zugriffs an, der von der Eigenschaft unterstützt wird (also get, put oder putref). Geben Sie das \[ [**schreibgeschützte**](readonly.md) \] Attribut für Eigenschaften an, die put oder putref nicht unterstützen. Wenn Sie die Eigenschaftenfunktionen in der Methodenliste deklarieren, weisen Alle Funktionen für eine Eigenschaft den gleichen Bezeichner auf.

Mit der ersten Syntax sind die Eigenschaften und Methoden: Tags erforderlich. Das \[ [**ID-Attribut**](id.md) \] ist auch für jedes Element erforderlich. Beispiel:

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

Im Gegensatz zu Schnittstellenmembern können dispinterface-Member das [**Attribut retval**](retval.md) nicht verwenden, um zusätzlich zu einem HRESULT-Fehlercode einen Wert zurückzugeben. Das \[ [**lcid-Attribut**](lcid.md) \] ist für dispinterfaces ebenfalls ungültig, da IDispatch::Invoke eine LCID übergibt. Es ist jedoch möglich, eine Schnittstelle erneut zu deklarieren, die diese Attribute verwendet.

Mit der zweiten Syntax können Schnittstellen, die IDispatch unterstützen und zuvor in einem ODL-Skript deklariert wurden, wie folgt als IDispatch-Schnittstellen erneut deklariert werden:

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

Im vorherigen Beispiel werden alle Member von hello und alle Member, die hello erbt, als unterstützend für IDispatch deklariert. Wenn hello in diesem Fall zuvor mit \[ \] lcid- und \[ retval-Membern deklariert wurde, die \] HRESULTs zurückgegeben haben, entfernt MkTypLib jeden \[ lcid-Parameter \] und HRESULT-Rückgabetyp und markiert den Rückgabetyp stattdessen als den des \[ retval-Parameters. \]

> [!Note]  
> Das Mktyplib.exe Tool ist veraltet. Verwenden Sie stattdessen den MIDL-Compiler.

 

Die Eigenschaften und Methoden einer Disp-Schnittstelle sind nicht Teil der VTBL der Disp-Schnittstelle. Daher können [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) und [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) nicht zum Implementieren von IDispatch::Invoke verwendet werden. Die Disp-Schnittstelle wird verwendet, wenn eine Anwendung vorhandene Nicht-VTBL-Funktionen über Automation verfügbar machen muss. Diese Anwendungen können IDispatch::Invoke implementieren, indem sie den dispidMember-Parameter untersuchen und die entsprechende Funktion direkt aufrufen.

## <a name="examples"></a>Beispiele

``` syntax
[ 
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("Useful help string."), 
    helpcontext(2480)
] 
dispinterface MyDispatchObject 
{ 
    properties: 
        [id(1)] int x;    //An integer property named x 
        [id(2)] BSTR y;   //A string property named y 
    methods: 
        [id(3)] HRESULT show();    //No arguments, no result 
        [id(11)] int computeit(int inarg, double *outarg); 
}; 
 
[
    uuid(1e123456-1f3c-1069-996b-00dd010fe676)
] 
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
 
        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**defaultbind**](defaultbind.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Versteckte**](hidden.md)
</dt> <dt>

[**In**](in.md)
</dt> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Optional**](optional.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**nonextensible**](nonextensible.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**Propput**](propput.md)
</dt> <dt>

[**Propputref**](propputref.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**Beschränkt**](restricted.md)
</dt> <dt>

[**Schnur**](string.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 