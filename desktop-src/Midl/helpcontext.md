---
title: helpcontext-Attribut
description: Das \helpcontext\-Attribut gibt einen Kontextbezeichner an, mit dem der Benutzer Informationen zu diesem Element in der Hilfedatei anzeigen kann.
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- helpcontext attribute MIDL
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3caa5dd32257fb5d75bbf77cde4ae5e71c6e97574cd1c263ead47aacedccadc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895250"
---
# <a name="helpcontext-attribute"></a>helpcontext-Attribut

Das \[ **helpcontext-Attribut** gibt einen Kontextbezeichner an, mit dem der Benutzer Informationen zu diesem \] Element in der Hilfedatei anzeigen kann.

``` syntax
[
    uuid(uuid-number), 
    helpcontext(helpcontext-value)
    [, attribute-list]
] 
element element-name
{
    definitions
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*uuid-number* 
</dt> <dd>

Gibt eine universell eindeutige ID für die Bibliothek [**,**](library.md) \[ [**importlib**](importlib.md) \] , [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **methods**, **\[ \] property** oder [**coclass an.**](coclass.md)

</dd> <dt>

*helpcontext-value* 
</dt> <dd>

Eine eindeutige ganze Zahl, die den Hilfetext identifiziert, der dem aktuellen MIDL-Element zugeordnet ist.

</dd> <dt>

*Attributliste* 
</dt> <dd>

Gibt eine Liste von Attributen an, die für das MIDL-Element als Ganzes gelten.

</dd> <dt>

*Element* 
</dt> <dd>

Eine der folgenden Anweisungen: [**Bibliothek**](library.md), \[ [**importlib**](importlib.md) \] , [**Schnittstelle**](interface.md), [**Dispinterface**](dispinterface.md), [**Modul**](module.md), [**Typedef**](typedef.md), **Methode**, Eigenschaft oder [**Co-Klasse**](coclass.md). 

</dd> <dt>

*Elementname* 
</dt> <dd>

Der Name, mit dem andere Softwarekomponenten das aktuelle Element abgrenzen können.

</dd> <dt>

*Definitionen* 
</dt> <dd>

Gibt Anweisungen an, die die Elementdefinition enthalten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das helpcontext-Attribut kann auf die folgenden Elemente angewendet \[  \] werden: [**Bibliothek**](library.md), \[ [**importlib**](importlib.md) \] , [**Schnittstelle**](interface.md), [**Dispinterface**](dispinterface.md), Modul [](module.md), [**Typedef**](typedef.md), **Methode**, **Eigenschaft** oder [**Co-Klasse**](coclass.md).

*Der helpcontext-value ist* ein 32-Bit-Kontextbezeichner in der Hilfedatei, der mit den [**GetDocumentation-Funktionen**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) in den [**Schnittstellen ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) und [**ITypeInfo abgerufen werden**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) kann.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpcontext(7035943),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default, helpcontext(3914972)] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**Dispatchschnittstelle**](dispinterface.md)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[**Bibliothek**](library.md)
</dt> <dt>

[**Modul**](module.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 