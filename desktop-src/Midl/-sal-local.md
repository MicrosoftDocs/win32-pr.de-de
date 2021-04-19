---
title: /sal_local Schalter
description: Der \_ lokale Switch/SAL leitet die mittlere Anmerkung für Parameter von Schnittstellen Methoden, die als "\ local \" gekennzeichnet sind. Der Schalter/SAL muss ebenfalls vorhanden sein.
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /sal_local-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03263b94b809407d1c3e55c2f3dacc5e10684bc1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341487"
---
# <a name="sal_local-switch"></a>/SAL \_ lokaler Switch

Der **\_ lokale Switch/SAL** leitet die mittlere Anmerkung für Parameter von Schnittstellen Methoden, die als [**\[ \] local**](local.md)gekennzeichnet sind Der Schalter [**/SAL**](-sal.md) muss ebenfalls vorhanden sein.

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Ändert das Verhalten des [**/SAL**](-sal.md) -Schalters, damit auch Anmerkungen zu den Parametern von Schnittstellen Methoden bereitgestellt werden, die mit dem [**\[ lokalen \]**](local.md) -Attribut gekennzeichnet sind. Verwenden Sie das [**\[ kommentieren \]**](annotate.md)-Attribut, um die mit der Mitte generierte Anmerkung mit einer anderen Anmerkung der Anmerkung zu überschreiben.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**\[kommentieren\]**](annotate.md)
</dt> </dl>

 

 




