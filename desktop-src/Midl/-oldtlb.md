---
title: /oldtlb-Switch
description: Der Schalter /oldtlb weist den MIDL-Compiler an, eine Typbibliothek im alten Format zu generieren.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- /oldtlb switch MIDL
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b30a7bc905645523a81287eea2dfcdc408b8a4d172cc84282e0f1538e12cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895990"
---
# <a name="oldtlb-switch"></a>/oldtlb-Switch

Der Schalter **/oldtlb** weist den MIDL-Compiler an, eine Typbibliothek im alten Format zu generieren.

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Der Schalter **/oldtlb** überschreibt den Standardwert und weist den MIDL-Compiler an, Typbibliotheken im alten Format auch in aktuellen Versionen von Windows zu generieren, indem [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) anstelle von [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2)verwendet wird.

## <a name="examples"></a>Beispiele

**midl /oldtlb filename.idl**

**midl /oldtlb myoldodl.odl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/newtlb**](-newtlb.md)
</dt> </dl>

 

 