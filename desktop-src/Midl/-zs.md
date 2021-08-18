---
title: /Zs-Schalter
description: Der Schalter /Zs gibt an, dass der Compiler nur die Syntax überprüft und keine Ausgabedateien generiert.
ms.assetid: 5ff44607-12c3-4a2d-8a7f-2056504990e2
keywords:
- /Zs switch MIDL
topic_type:
- apiref
api_name:
- /Zs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92bd2321567bbc565d3198fe5ebf5c98a3d8df440ea967409830c8e73488609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014018"
---
# <a name="zs-switch"></a>/Zs-Schalter

Der **Schalter /Zs** gibt an, dass der Compiler nur die Syntax überprüft und keine Ausgabedateien generiert.

``` syntax
midl /Zs
midl /syntax_check
```

## <a name="switch-options"></a>Switch-Optionen

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Dieser Schalter überschreibt alle anderen Schalter, die Informationen zu Ausgabedateien angeben.

Sie können den Syntaxüberprüfungsmodus auch mit dem MIDL-Compilerschalter [**/syntax \_ check angeben.**](-syntax-check.md)

## <a name="examples"></a>Beispiele

**midl /Zs filename.idl**

**midl /syntax \_ check filename.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/syntax \_ check**](-syntax-check.md)
</dt> </dl>

 

 




