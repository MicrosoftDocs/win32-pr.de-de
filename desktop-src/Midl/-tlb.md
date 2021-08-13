---
title: /tlb-Schalter
description: Der Schalter /tlb gibt einen Dateinamen für die vom MIDL-Compiler generierte Typbibliothek an.
ms.assetid: 7d5d9f92-ed1a-46bc-beb1-4be70d0a4813
keywords:
- /tlb switch MIDL
topic_type:
- apiref
api_name:
- /tlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 081723648788ec51fa65a4770deb336f665804a9527dc223000826870dbe1ee0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643750"
---
# <a name="tlb-switch"></a>/tlb-Schalter

Der Schalter **/tlb** gibt einen Dateinamen für die vom MIDL-Compiler generierte Typbibliothek an.

``` syntax
midl /tlb filename
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*filename* 
</dt> <dd>

Gibt den Namen der Ausgabetypbibliotheksdatei (TLB) an. Wenn der Schalter **/tlb** nicht verwendet wird, hat die TLB-Datei standardmäßig den gleichen Namen wie die IDL-Datei mit der Erweiterung . Tlb.

</dd> </dl>

## <a name="examples"></a>Beispiele

**midl /tlb newname.tlb**

## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/notlb**](-notlb.md)
</dt> </dl>

 

 




