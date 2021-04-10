---
title: /msc_ver Schalter
description: Der Schalter "/MSC \_ ver" wird verwendet, um es mittlerer l zu ermöglichen, Code zu generieren, der Optimierungen für verschiedene Versionen von Microsoft C/C++-Compilern enthält.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /msc_ver-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3620b3c8ffb1315a4d34eb0b4b2497c1cb3d805
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857544"
---
# <a name="msc_ver-switch"></a>/MSC \_ ver-Schalter

Der Schalter " **/MSC \_ ver** " wird verwendet, um es mittlerer l zu ermöglichen, Code zu generieren, der Optimierungen für verschiedene Versionen von Microsoft C/C++-Compilern enthält.

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*Versions \_ Nummer* 
</dt> <dd>

Gibt eine ganzzahlige Versionsnummer des Microsoft Visual C++ Compilers an, der verwendet wird, um die Client-und serverstubfunktionen der verteilten Anwendung zu kompilieren. Die Standard Versionsnummer ist 1100, was Visual C++ Version 5,0 entspricht. Die Versionsnummer 1200 entspricht Visual C++ Version 6,0 usw.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bestimmte Versions Werte von 1100 oder höher bewirken, dass der Mittell-Compiler Code mithilfe der **\_ \_ declspec (UUID ())** -Direktive generiert. Außerdem werden Makros aktiviert, die die Anweisungen **\_ \_ declspec (selectany)** und **\_ \_ declspec (novtable)** verwenden.

 

 




