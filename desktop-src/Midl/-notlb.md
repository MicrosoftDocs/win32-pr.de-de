---
title: Schalter "/notlb"
description: Der Schalter /notlb verhindert, dass der MIDL-Compiler eine Typbibliotheksdatei (TLB) generiert.
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- /notlb switch MIDL
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e309ed753d1549c31c9e3dea0a5c7aa87b32217aa12e5ee04934a183927adf87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067520"
---
# <a name="notlb-switch"></a>Schalter "/notlb"

Der **Schalter /notlb** verhindert, dass der MIDL-Compiler eine Typbibliotheksdatei (TLB) generiert.

``` syntax
midl /notlb
```

## <a name="switch-options"></a>Switch-Optionen

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Standardmäßig generiert der MIDL-Compiler immer dann eine TLB-Datei, wenn eine [**LIBRARY-Anweisung gefunden**](library.md) wird. Dieser Schalter überschreibt das Standardverhalten.

Wenn die **Option /notlb** angegeben wird, werden alle anderen Stubs, Header usw. wie gewohnt generiert.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**/tlb**](-tlb.md)
</dt> </dl>

 

 




