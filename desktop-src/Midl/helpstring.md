---
title: HelpString-Attribut
description: Das Attribut \ HelpString \ gibt eine Zeichenfolge an, mit der das Element beschrieben wird, auf das es angewendet wird.
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- HelpString-Attribut-Mittel l
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c58bbe61b10e2f223cf9f662f10d95ca72819b02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948630"
---
# <a name="helpstring-attribute"></a>HelpString-Attribut

Das **\[ HelpString \]** -Attribut gibt eine Zeichenfolge an, die verwendet wird, um das Element zu beschreiben, auf das es angewendet wird. Sie können das **\[ HelpString \]** -Attribut auf die Anweisungen Library, importlib, Interface, dispinterface, Module oder Co-Klasse, Typedefs, Properties und Methods anwenden.

``` syntax
[
    helpstring(help-text-string)
    [, optional-attribute-list]
] 
element element-name
{
    definition
}

[idl-statement, helpstring(help-text-string)]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Hilfe-Text Zeichenfolge* 
</dt> <dd>

Eine mit NULL endend beendete Zeichenfolge, die Hilfetext enthält.

</dd> <dt>

*optional-Attribut-List* 
</dt> <dd>

NULL oder mehr Mittelwert-Attribut Anweisungen.

</dd> <dt>

*gewisses* 
</dt> <dd>

Eine der folgenden Direktiven: [**Library**](library.md), **\[** [**importlib**](importlib.md) **\]** , [**Interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **method**, **Property** oder [**Co-Klasse**](coclass.md).

</dd> <dt>

*Elementname* 
</dt> <dd>

Der Name, den andere Softwarekomponenten verwenden können, um das aktuelle Element zu definieren.

</dd> <dt>

*Definition* 
</dt> <dd>

Gibt die-Anweisungen an, die die Element Definition bilden.

</dd> <dt>

*IDL-Anweisung* 
</dt> <dd>

Eine Anweisung der Mittell-Schnittstellen Definition, z. b. [**propget**](propget.md) oder [**PROPPUT**](propput.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) -Funktionen in den Schnittstellen [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) und [**itypeingefo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) , um die Hilfe Zeichenfolge abzurufen.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Lines 1.0 Type Library"),
    version(1.0)
]
library Lines
{
     [
         uuid(1e123456-1f3c-1069-996b-00dd010fe676), 
         helpstring("Line object."),
         oleautomation,
         dual
     ]
     interface ILine : IDispatch                         
     {
         [propget, helpstring("Returns and sets RGB color.")]
         HRESULT Color([out, retval] long* ReturnVal); 
         [propput, helpstring("Returns and sets RGB color.")]
         HRESULT Color([in] long rgb);
     }
};
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Bibliothek**](library.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**Mond**](module.md)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 