---
title: /notlb-Schalter
description: Der/notlb-Schalter verhindert, dass der Mittell-Compiler eine Typbibliotheks Datei (TLB-Datei) erzeugt.
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- /notlb-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81911b6afb00d61713f966ba9e1981b979e51008
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471965"
---
# <a name="notlb-switch"></a>/notlb-Schalter

Der **/notlb** -Schalter verhindert, dass der Mittell-Compiler eine Typbibliotheks Datei (TLB-Datei) erzeugt.

``` syntax
midl /notlb
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Standardmäßig generiert der mittlerer l-Compiler eine TLB-Datei, wenn eine [**Library**](library.md) -Anweisung gefunden wird. Dieser Schalter überschreibt das Standardverhalten.

Wenn die **/notlb** -Option angegeben wird, werden alle anderen Stub-, Header-usw. wie üblich generiert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/TLB**](-tlb.md)
</dt> </dl>

 

 




