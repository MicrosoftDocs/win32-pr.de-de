---
title: Steuerelementattribut
description: Das Attribut \control\ identifiziert eine Co-Klasse oder Bibliothek als COM-Steuerelement, von dem eine Containerwebsite zusätzliche Typbibliotheken oder Komponentenobjektklassen ableiten wird.
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- Steuerelementattribut MIDL
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6372ffb7f7d9f19769e419b12c0b109736a9867360224e023f1b622c653854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643679"
---
# <a name="control-attribute"></a>Steuerelementattribut

Das **\[ \] Steuerelementattribut** identifiziert [](library.md) eine [**Co-Klasse**](coclass.md) oder Bibliothek als COM-Steuerelement, von dem eine Containerwebsite zusätzliche Typbibliotheken oder Komponentenobjektklassen ableiten wird.

``` syntax
[
    uuid, 
    control 
    [, attribute-list]
] 
library | coclass lib-or-coclassname 
{ 
    definitions 
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Attributliste* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für die Bibliothek oder [**coclass-Anweisung gelten.**](coclass.md) [](library.md) Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*lib-or-coclassname* 
</dt> <dd>

Gibt den Namen der Bibliothek oder [**Co-Klasse**](library.md) [**an.**](coclass.md)

</dd> <dt>

*Definitionen* 
</dt> <dd>

MIDL-Anweisungen, die die Member der Bibliothek [**oder**](library.md) [**Co-Klasse angeben.**](coclass.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Mit diesem Attribut können Sie Typbibliotheken markieren, die Steuerelemente beschreiben, sodass sie nicht in Typbrowsern angezeigt werden, die für nichtvisuelle Objekte vorgesehen sind.

### <a name="flags"></a>Flags

TYPEFLAG \_ FCONTROL, LIBFLAG \_ FCONTROL

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("Hello 2.1 COM Control Library"), 
    control,version(2.1)
] 
library Hello 
{ 
    /* library definitions */
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ODL-Dateisyntax](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL-Dateibeispiel](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**Bibliothek**](library.md)
</dt> </dl>

 

 