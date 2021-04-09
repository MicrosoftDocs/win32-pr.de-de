---
title: helpcontext-Attribut
description: Das Attribut \ HelpContext \ gibt einen Kontext Bezeichner an, mit dem der Benutzerinformationen zu diesem Element in der Hilfedatei anzeigen kann.
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- HelpContext-Attribut-Mittel l
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a8811a73515528981a8214caba3fe2778e2ea9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948643"
---
# <a name="helpcontext-attribute"></a>helpcontext-Attribut

Das \[ **HelpContext** - \] Attribut gibt einen Kontext Bezeichner an, mit dem der Benutzerinformationen zu diesem Element in der Hilfedatei anzeigen kann.

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

*UUID-Nummer* 
</dt> <dd>

Gibt eine universell eindeutige ID für die [**Bibliothek**](library.md), die \[ [**importlib**](importlib.md) \] , die [**Schnittstelle**](interface.md), die [**dispinterface**](dispinterface.md), das [**Modul**](module.md), die [**typedef**](typedef.md), die **Methoden**, die **\[ Eigenschaft \]** oder die Co- [**Klasse**](coclass.md)an.

</dd> <dt>

*HelpContext-Wert* 
</dt> <dd>

Eine eindeutige ganze Zahl, die den Hilfetext identifiziert, der dem aktuellen Mittel l-Element zugeordnet ist.

</dd> <dt>

*Attribut-List* 
</dt> <dd>

Gibt eine Liste mit einem oder mehreren Attributen an, die auf das Mittel l-Element als Ganzes angewendet werden.

</dd> <dt>

*gewisses* 
</dt> <dd>

Eine der folgenden Direktiven: [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**Interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **method**, **Property** oder [**Co-Klasse**](coclass.md).

</dd> <dt>

*Elementname* 
</dt> <dd>

Der Name, den andere Softwarekomponenten verwenden können, um das aktuelle Element zu definieren.

</dd> <dt>

*definiert* 
</dt> <dd>

Gibt die-Anweisungen an, die die Element Definition bilden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das \[ **HelpContext** - \] Attribut kann auf die folgenden Elemente angewendet werden: [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**Interface**](interface.md), [**dispinterface**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **method**, **Property** oder [**Co-Klasse**](coclass.md).

Der *HelpContext-Wert* ist ein 32-Bit-Kontext Bezeichner in der Hilfedatei, der mit den [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) -Funktionen in der [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) -Schnittstelle und der [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) -Schnittstelle abgerufen werden kann.

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

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[**Bibliothek**](library.md)
</dt> <dt>

[**Mond**](module.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 