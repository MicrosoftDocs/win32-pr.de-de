---
title: pointer_default-Attribut
description: Das Attribut \pointer \_ default\ gibt das Standardzeigerattribut für alle Zeiger mit Ausnahme von Zeigern der obersten Ebene an, die in Parameterlisten angezeigt werden.
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- pointer_default-Attribut MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d246da98db6d3f98aa8c64e1316ee56648016402d1070ae571284148b8caf390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013768"
---
# <a name="pointer_default-attribute"></a>\_Zeigerstandardattribut

Das **\[ \_ \] Zeigerstandardattribut** gibt das Standardzeigerattribut für alle Zeiger mit Ausnahme von Zeigern der obersten Ebene an, die in Parameterlisten angezeigt werden.

``` syntax
pointer_default ( ptr | ref | unique )
```

## <a name="parameters"></a>Parameter

Dieses Attribut verfügt über keine Parameter.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(6B29FC40-CA47-1067-B31D-00DD010662DA), 
    version(3.3), 
    pointer_default(unique)
] 
interface dictionary 
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[Array- und Sized-Pointer attribute](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**Arrays**](arrays-1.md)
</dt> <dt>

[Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Einzigartige**](unique.md)
</dt> <dt>

[Standardzeigertypen](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 