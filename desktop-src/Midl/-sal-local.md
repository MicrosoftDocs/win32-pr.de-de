---
title: /sal_local Switch
description: Der lokale Schalter /sal \_ weist MIDL an, auch SAL-Anmerkungen für Parameter von Schnittstellenmethoden zu generieren, die mit \local\ gekennzeichnet sind. Der Schalter /sal muss ebenfalls vorhanden sein.
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /sal_local Switch MIDL
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666401cca482846fc2e6a9d5851a4da9d2d362279c9bc1496ab672a94ac9b9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014088"
---
# <a name="sal_local-switch"></a>Lokaler \_ Schalter "/sal"

Der lokale Schalter **/sal \_** weist MIDL an, auch SAL-Anmerkungen für Parameter von Schnittstellenmethoden zu generieren, die als [**\[ lokal \]**](local.md)gekennzeichnet sind. Der Schalter [**/sal**](-sal.md) muss ebenfalls vorhanden sein.

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Ändert das Verhalten des Schalters [**/sal,**](-sal.md) um auch Anmerkungen zu den Parametern von Schnittstellenmethoden bereitzustellen, die mit dem [**\[ lokalen \]**](local.md) Attribut markiert sind. Verwenden Sie das [**\[ Attribut annotate, \]**](annotate.md)um die midl-generierte Anmerkung mit einer anderen Anmerkungszeichenfolge zu überschreiben.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**\[Kommentieren\]**](annotate.md)
</dt> </dl>

 

 




