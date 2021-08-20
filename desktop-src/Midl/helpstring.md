---
title: helpstring-Attribut
description: Das \helpstring\-Attribut gibt eine Zeichenfolge an, die verwendet wird, um das Element zu beschreiben, auf das es angewendet wird.
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- HELPSTRING-Attribut MIDL
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7abb433d7112bc4c3257345d086ccf308cc1892b61a99991b485ce4962b5851e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013868"
---
# <a name="helpstring-attribute"></a>helpstring-Attribut

Das **\[ \] helpstring-Attribut** gibt eine Zeichenfolge an, die verwendet wird, um das Element zu beschreiben, auf das es angewendet wird. Sie können das **\[ \] helpstring-Attribut** auf Bibliotheks-, Importlib-, Schnittstellen-, Dispinterface-, Modul- oder Coclass-Anweisungen, TypeDefs, Eigenschaften und Methoden anwenden.

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

*help-text-string* 
</dt> <dd>

Eine auf null endende Zeichenfolge von Zeichen, die Hilfetext enthält.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Null oder mehr MIDL-Attributanweisungen.

</dd> <dt>

*Element* 
</dt> <dd>

Eine der folgenden Direktiven: [**bibliothek,**](library.md) **\[** [**importlib,**](importlib.md) **\]** [**interface,**](interface.md) [**dispinterface,**](dispinterface.md) [**module,**](module.md) [**typedef,**](typedef.md) **method,** **property** oder [**coclass**](coclass.md).

</dd> <dt>

*Elementname* 
</dt> <dd>

Der Name, den andere Softwarekomponenten verwenden können, um das aktuelle Element abzugrenzen

</dd> <dt>

*Definition* 
</dt> <dd>

Gibt Anweisungen an, die die Elementdefinition bilden.

</dd> <dt>

*idl-statement* 
</dt> <dd>

Eine MIDL-Schnittstellendefinitions-Anweisung wie [**propget**](propget.md) oder [**propput**](propput.md).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie die [**GetDocumentation-Funktionen**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) in den [**Schnittstellen ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) und [**ITypeInfo,**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) um die Hilfezeichenfolge abzurufen.

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

[**Schnittstelle**](interface.md)
</dt> <dt>

[**Dispatchschnittstelle**](dispinterface.md)
</dt> <dt>

[**Modul**](module.md)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[BEISPIEL FÜR ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 