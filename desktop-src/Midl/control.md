---
title: Control-Attribut
description: Das \ Control \-Attribut identifiziert eine Co-Klasse oder eine Bibliothek als com-Steuerelement, aus dem eine Container Site zusätzliche Typbibliotheken oder Komponenten Objektklassen ableitet.
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- Steuerelement Attribut-Mittel l
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982327d581ddb606f733e9efbbcb89e2f9972cf4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724953"
---
# <a name="control-attribute"></a>Control-Attribut

Das **\[ Control \]** -Attribut identifiziert eine [**Co-Klasse**](coclass.md) oder eine [**Bibliothek**](library.md) als com-Steuerelement, aus dem eine Container Site zusätzliche Typbibliotheken oder Komponenten Objektklassen ableitet.

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

*Attribut-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die [**Library**](library.md) -oder [**Co-Klasse**](coclass.md) -Anweisung gelten. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*lib-oder-CoClassname* 
</dt> <dd>

Gibt den Namen der [**Bibliothek**](library.md) oder der [**Co-Klasse**](coclass.md)an.

</dd> <dt>

*definiert* 
</dt> <dd>

Mittel l-Anweisungen, die die Member der [**Bibliothek**](library.md) oder der [**Co-Klasse**](coclass.md)angeben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit diesem Attribut können Sie Typbibliotheken markieren, die Steuerelemente beschreiben, sodass Sie nicht in Typbrowsern angezeigt werden, die für nicht visuelle Objekte bestimmt sind.

### <a name="flags"></a>Flags

TYPEFLAG-Steuerelement \_ , libflag \_ -Steuerelement

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

[Syntax der ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Beispiel für eine ODL-Datei](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Erstellen einer Typbibliothek mit "Mittel l"](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[FUNCFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**Bibliothek**](library.md)
</dt> </dl>

 

 