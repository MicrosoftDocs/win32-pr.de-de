---
title: Die named_type_free_inst-Funktion
description: Die Stubs rufen die benannte Funktion vom Typ free inst auf, um Arbeitsspeicher frei zu \_ \_ \_ geben, der dem übertragenen Typ zugeordnet ist.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa55e896b89fccc513795a62634e805c2ad6e21b7bdecdd99a0b9cfe2d71cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016889"
---
# <a name="the-named_type_free_inst-function"></a>Die funktion \_ \_ "free \_ inst" des benannten Typs

Die Stubs rufen die benannte Funktion **\_ vom Typ free \_ \_ inst** auf, um Arbeitsspeicher frei zu geben, der dem übertragenen Typ zugeordnet ist. Die Funktion ist wie die folgenden definiert:

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

Der -Parameter verweist auf die Instanz des übertragenen Typs. Dieses Objekt sollte nicht frei werden. Eine Diskussion darüber, wann die Funktion aufruft werden soll, finden Sie unter [Der als \_ Attribut darstellende](the-represent-as-attribute.md).

 

 




