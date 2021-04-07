---
title: defaultcollelem-Attribut
description: Das Attribut "\ Defaultcollelem \" markiert eine Eigenschaft als eine Accessorfunktion für ein Element der Standard Auflistung.
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- Defaultcollelem-Attribut-Mittel l
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038936"
---
# <a name="defaultcollelem-attribute"></a>defaultcollelem-Attribut

Das **\[ Defaultcollelem \]** -Attribut markiert eine Eigenschaft als eine Accessorfunktion für ein Element der Standard Auflistung.

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Property-Attribute-List* 
</dt> <dd>

Andere Attribute, die auf die-Eigenschaft angewendet werden.

</dd> <dt>

*Rückgabetyp* 
</dt> <dd>

Gibt den Rückgabetyp der Funktion an.

</dd> <dt>

*Eigenschaftsname* 
</dt> <dd>

Den Namen der Eigenschaft.

</dd> <dt>

*Prop-param-List* 
</dt> <dd>

Eine Liste von NULL oder mehr Parametern, die der-Eigenschaft zugeordnet sind.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ Defaultcollelem \]** -Attribut wird für die Codeoptimierung von Visual Basic® verwendet. Wenn ein Member einer Schnittstelle oder einer dispinterface als Accessorfunktion gekennzeichnet ist, wird der-Befehl direkt an diesen Member weitergeleitet.

Die Verwendung von **\[ Defaultcollelem \]** muss für eine Eigenschaft einheitlich sein. Wenn Sie z. b. das-Attribut für eine *Get* -Eigenschaft verwenden, muss es auch in einer *Let* -Eigenschaft vorhanden sein.

### <a name="typeflags-representation"></a>TYPEFLAGS-Darstellung

Das vorhanden sein von funkflag " \_ sdefaultcollelem" oder "varflag" mit dem Wert " \_ f".

## <a name="examples"></a>Beispiele

``` syntax
//A form has a button on it named Button1. 
//To enable use of the property syntax and efficient use of the !
//syntax, the form describes itself in type info this way.
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is IForm"),
    restricted
]
interface IForm1: IForm
{
    [propget, defaultcollelem] HRESULT Button1(
        [out, retval] Button *Value);
}

//User code may access the button using property syntax or ! syntax.

Sub Test()
Dim f as Form1
Dim b1 As Button
Dim b2 As Button

Set f = Form1

Set b1 = f.Button1        ' Property syntax
Set b = f!Button1        ' ! syntax
End Sub
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 