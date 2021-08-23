---
title: Eingeschränktes Attribut
description: Das Attribut \restricted\gibt an, dass eine Bibliothek oder ein Member eines Moduls, einer Schnittstelle oder einer Disp-Schnittstelle nicht willkürlich aufgerufen werden kann.
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- restricted attribute MIDL
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc68bbea9e1834fd1b1953f8dbf16a79e5356f49bf6058615904d78c244668a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822090"
---
# <a name="restricted-attribute"></a>Eingeschränktes Attribut

Das **\[ eingeschränkte \]** Attribut gibt an, dass eine Bibliothek oder ein Member eines Moduls, einer Schnittstelle oder einer Disp-Schnittstelle nicht willkürlich aufgerufen werden kann.

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

*other-attributes* 
</dt> <dd>

Null oder mehr MIDL-Attribute.

</dd> <dt>

*statement-type* 
</dt> <dd>

Eine der folgenden: [**Bibliothek,**](library.md) [**Modul,**](module.md) [**Schnittstelle,**](interface.md) [**Dispinterface**](dispinterface.md).

</dd> <dt>

*Anweisungsname* 
</dt> <dd>

Der Bezeichner, mit dem die Software auf diese Anweisung verweist.

</dd> <dt>

*Definitionen* 
</dt> <dd>

MIDL-Sprachelemente, die den Inhalt dieser Anweisung definieren.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Mit diesem Attribut können Sie den Zugriff auf Elemente von Schnittstellen, Bibliotheken, Modulen und Disp-Schnittstellen steuern. So kann beispielsweise verhindert werden, dass ein Datenelement von einem Makroprogrammierer verwendet wird. Sie können dieses Attribut auf einen Member einer Co-Klasse [**anwenden,**](coclass.md)unabhängig davon, ob der Member eine Disp-Schnittstelle oder -Schnittstelle ist, und unabhängig davon, ob der Member eine Senke (eingehend) oder eine Quelle (ausgehend) ist. Ein Member einer **Co-Klasse kann** nicht sowohl das eingeschränkte als **\[ auch \]** das **\[ Standardattribut \]** haben.

### <a name="flags"></a>Flags

IMPLTYPEFLAG \_ FRESTRICTED, FUNCFLAG \_ FRESTRICTED

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

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Bibliothek**](library.md)
</dt> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[**Dispatchschnittstelle**](dispinterface.md)
</dt> <dt>

[**Modul**](module.md)
</dt> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 