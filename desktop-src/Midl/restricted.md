---
title: Eingeschränktes Attribut
description: Das Attribut \ restricted \ gibt an, dass eine Bibliothek oder ein Member eines Moduls, einer Schnittstelle oder einer dispinterface nicht willkürlich aufgerufen werden kann.
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- eingeschränkte Attribute-Mittell
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca610c0dcf29ebc3a767005b4c22e3231947e88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390250"
---
# <a name="restricted-attribute"></a>Eingeschränktes Attribut

Das **\[ restricted \]** -Attribut gibt an, dass eine Bibliothek oder ein Member eines Moduls, einer Schnittstelle oder einer dispinterface nicht willkürlich aufgerufen werden kann.

``` syntax
[
    restricted
    [, other-attributes]
] 
statement-type statement-name 
{
    definitions
};
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*andere-Attribute* 
</dt> <dd>

NULL oder mehr mittlere Attribute.

</dd> <dt>

*Anweisungstyp* 
</dt> <dd>

Eines der folgenden: [**Library**](library.md), [**Module**](module.md), [**Interface**](interface.md), [**dispinterface**](dispinterface.md).

</dd> <dt>

*Anweisungs Name* 
</dt> <dd>

Der Bezeichner, mit dem sich die Software auf diese Anweisung bezieht.

</dd> <dt>

*definiert* 
</dt> <dd>

Mittel l-Sprachelemente, die den Inhalt dieser Anweisung definieren.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit diesem Attribut können Sie den Zugriff auf Elemente von Schnittstellen, Bibliotheken, Modulen und dispinterfaces steuern. Beispielsweise kann verhindert werden, dass ein Datenelement von einem makroprogrammierer verwendet wird. Sie können dieses Attribut auf einen Member einer Co- [**Klasse**](coclass.md)anwenden, unabhängig davon, ob der Member eine dispinterface oder eine Schnittstelle ist, und unabhängig davon, ob der Member eine Senke (eingehend) oder eine Quelle (ausgehend) ist. Ein Member einer **Co-Klasse** kann nicht sowohl das **\[ restricted \]** -als auch das **\[ Default \]** -Attribut aufweisen.

### <a name="flags"></a>Flags

impltypeflag " \_ frestrihiert", funkflag " \_ frestrihiert"

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version (1.0), 
    restricted
] 
library MyLibrary
{
    // Library definition statements.
};

[propget, restricted] HRESULT MyProc(void);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Bibliothek**](library.md)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**Mond**](module.md)
</dt> <dt>

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 