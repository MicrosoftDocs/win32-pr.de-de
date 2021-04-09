---
title: dispinterface-Attribut
description: Die dispinterface-Anweisung definiert einen Satz von Eigenschaften und Methoden, auf die Sie IDispatch aufrufen können.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- Attribut für Dispinterface-Attribut
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858241"
---
# <a name="dispinterface-attribute"></a>dispinterface-Attribut

Die **dispinterface** -Anweisung definiert einen Satz von Eigenschaften und Methoden, auf die Sie **IDispatch:: Aufrufen** aufrufen können. Eine dispinterface kann definiert werden, indem der Satz unterstützter Methoden und Eigenschaften (Syntax 1) explizit aufgelistet oder eine einzelne Schnittstelle aufgelistet wird (Syntax 2).

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

Gibt Attribute an, die auf die gesamte **dispinterface** angewendet werden. Die folgenden Attribute werden akzeptiert: **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**nonextensible**](nonextensible.md) **\]** , **\[** [**oleautomation**](oleautomation.md) **\]** , **\[** [**restricted**](restricted.md) **\]** , **\[** [**UUID**](uuid.md) **\]** und **\[** [**Version**](version.md) **\]** .

</dd> <dt>

*dispinterface-Name* 
</dt> <dd>

Der Name, mit dem die **dispinterface** in der Typbibliothek bekannt ist. Dieser Name muss innerhalb der Typbibliothek eindeutig sein.

</dd> <dt>

*Eigenschaften Liste* 
</dt> <dd>

(Syntax 1) Eine optionale Liste der Eigenschaften, die vom-Objekt unterstützt und in Form von Variablen deklariert werden. Dies ist die Kurzform zum Deklarieren der Eigenschafts Funktionen in der Methoden Liste. Weitere Informationen finden Sie im Abschnitt "Kommentare".

</dd> <dt>

*Methoden Liste* 
</dt> <dd>

(Syntax 1) Eine Liste, die einen Funktionsprototyp für jede Methode und Eigenschaft in der **dispinterface** enthält. Eine beliebige Anzahl von Funktionsdefinitionen kann in " *methlist*" angezeigt werden. Eine Funktion in " *methlist* " weist die folgende Form auf:

**\[  Attribute \]** *returnType methname Type paramName ***(*** Parametern * * *);**

Die folgenden Attribute werden für eine Methode in einer " **dispinterface**"-Methode akzeptiert: **\[ HelpString \]**, **\[ HelpContext \]**, **\[** [**propget**](propget.md) **\]** , **\[** [**PROPPUT**](propput.md) **\]** , **\[** [**PROPPUTREF**](propputref.md) **\]** , **\[** [**String**](string.md) **\]** und **\[** [**vararg**](vararg.md) **\]** . Wenn **\[ vararg \]** angegeben ist, muss der letzte Parameter ein sicheres Array vom **Variant** -Typ sein.

Die Parameterliste ist eine durch Trennzeichen getrennte Liste, von der jedes Element die folgende Form aufweist:

**\[***legt***\]**

Der *Typ* kann ein beliebiger deklarierter oder integrierter Typ oder ein Zeiger auf einen beliebigen Typ sein. Attribute für Parameter sind:

**\[**[**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** , **\[** [**optional**](optional.md) **\]** , **\[ Zeichen \] Folge**

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

(Syntax 2) Der Name der Schnittstelle, die als IDispatch-Schnittstelle deklariert werden soll.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der mittlerer l-Compiler akzeptiert die folgende Parameter Reihenfolge (von links nach rechts):

1.  Erforderliche Parameter (Parameter, die nicht über das \[ DefaultValue \] - \[ Attribut oder optionale \] Attribute verfügen)
2.  optionale Parameter mit oder ohne das \[ DefaultValue- \] Attribut
3.  Parameter mit dem \[ optionalen \] -Attribut und ohne das \[ DefaultValue- \] Attribut
4.  \[[**LCID**](lcid.md) - \] Parameter (falls vorhanden)
5.  \[[**retval**](retval.md) \] Parame

Methoden Funktionen werden genau so angegeben, wie Sie auf der Referenzseite für das [**Modul**](module.md) beschrieben werden, außer dass das \[ Attribut [**Entry**](entry.md) \] nicht zulässig ist. Beachten Sie, dass STDOLE32. TLB (stdole). TLB auf 16-Bit-Systemen) muss importiert werden, da eine **dispinterface** von IDispatch erbt.

Sie können Eigenschaften in den Listen Eigenschaften oder Methoden deklarieren. Das Deklarieren von Eigenschaften in der Eigenschaften Liste gibt nicht den Zugriffstyp an, den die Eigenschaft unterstützt (d. h. Get, Put oder PutRef). Geben Sie das Attribut "schreibgeschützt" \[ [](readonly.md) \] für Eigenschaften an, die Put oder PutRef nicht unterstützen. Wenn Sie die Eigenschaften Funktionen in der Liste der Methoden deklarieren, haben Funktionen für eine Eigenschaft alle denselben Bezeichner.

Mithilfe der ersten Syntax sind die-und-Methoden: Tags erforderlich. Das \[ [**ID**](id.md) - \] Attribut ist auch für jedes Element erforderlich. Beispiel:

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

Anders als bei Schnittstellenmembern können dispinterface-Member das [**retval**](retval.md) -Attribut nicht verwenden, um einen Wert zusätzlich zu einem HRESULT-Fehlercode zurückzugeben. Das \[ [**LCID**](lcid.md) - \] Attribut ist für dispinterfaces ebenso ungültig, da IDispatch:: Aufrufen eine LCID übergibt. Es ist jedoch möglich, eine Schnittstelle, die diese Attribute verwendet, erneut zu deklarieren.

Mithilfe der zweiten Syntax können Schnittstellen, die IDispatch unterstützen und zuvor in einem ODL-Skript deklariert wurden, wie folgt als IDispatch-Schnittstellen neu deklariert werden:

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

Im vorherigen Beispiel werden alle Member von Hello und alle Member deklariert, die Hello als Unterstützung von IDispatch erbt. In diesem Fall \[ \] \[ \] würde MkTypLib jeden \[ LCID- \] Parameter und den HRESULT-Rückgabetyp entfernen und stattdessen den Rückgabetyp als den \[ retval- \] Parameter markieren, wenn Hello früher mit LCID-und retval-Membern deklariert wurde, die HRESULTs zurückgegeben haben.

> [!Note]  
> Das Mktyplib.exe Tool ist veraltet. Verwenden Sie stattdessen den Mittel l-Compiler.

 

Die Eigenschaften und Methoden einer dispinterface sind nicht Teil der VTBL von dispinterface. Folglich können [](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) mit "" "" " [](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) " "" "" "" "" "" "" mit "" "" "" " Die dispinterface wird verwendet, wenn eine Anwendung vorhandene nicht-VTBL-Funktionen über Automation verfügbar machen muss. Diese Anwendungen können IDispatch:: Call implementieren, indem Sie den dispidmember-Parameter untersuchen und die entsprechende Funktion direkt aufrufen.

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

[**verbirgt**](hidden.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**optionale**](optional.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**nonextensible**](nonextensible.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**begrenz**](restricted.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> <dt>

[**UUID**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 