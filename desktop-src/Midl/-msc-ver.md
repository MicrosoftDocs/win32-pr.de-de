---
title: /msc_ver Switch
description: Der Schalter /msc \_ ver wird verwendet, damit MIDL Code generieren kann, der Optimierungen für verschiedene Versionen von Microsoft C/C++-Compilern enthält.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /msc_ver Switch MIDL
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f010224e5339ef89e05d1d96630dbedc0cb453eb8dafb4dd5e9c6edb3c24cc00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811370"
---
# <a name="msc_ver-switch"></a>\_/msc ver switch

Der Schalter **/msc \_ ver** wird verwendet, damit MIDL Code generieren kann, der Optimierungen für verschiedene Versionen von Microsoft C/C++-Compilern enthält.

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*\_Versionsnummer* 
</dt> <dd>

Gibt eine ganzzahlige Versionsnummer des Microsoft Visual C++ Compilers an, der zum Kompilieren der Client- und Serverstubs der verteilten Anwendung verwendet wird. Die Standardversionsnummer ist 1100, was Visual C++ Version 5.0 entspricht. Die Versionsnummer 1200 entspricht Visual C++ Version 6.0 usw.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Insbesondere die Versionswerte 1100 oder höher bewirken, dass der MIDL-Compiler Code mithilfe der **\_ \_ declspec(uuid())-Direktive** generiert. Außerdem werden Makros aktiviert, die die Anweisungen **\_ \_ declspec(selectany)** und **\_ \_ declspec(novtable)** verwenden.

 

 




