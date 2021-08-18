---
title: /mktyplib203 switch
description: Der Schalter /mktyplib203 zwingt den MIDL-Compiler, die Eingabedatei zu analysieren.
ms.assetid: e1eddf03-db42-426e-bdf1-b7122b862756
keywords:
- /mktyplib203 switch MIDL
topic_type:
- apiref
api_name:
- /mktyplib203
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc887560401986b9a7d5e0f0aa7c8b36d61874bf245a88ade7a149cd084f1ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014148"
---
# <a name="mktyplib203-switch"></a>/mktyplib203 switch

Der Schalter **/mktyplib203** zwingt den MIDL-Compiler, die Eingabedatei zu analysieren.

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Um den Schalter **/mktyplib203** zu verwenden, muss die Eingabedatei genau der ODL-Syntax folgen. Das bedeutet, dass Sie keine Anweisungen außerhalb des Bibliotheksblocks platzieren können. Beispiele

**midl /mktyplib203 myoldodl.odl**

**midl /mktyplib203 oldhabit.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[Generieren einer Typbibliothek mit MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 




