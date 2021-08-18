---
title: Die named_type_free_local-Funktion
description: Die Stubs rufen die lokale Funktion type \_ free \_ auf, um den Arbeitsspeicher freizugeben, der durch einen Aufruf des benannten Typs an die lokale Routine belegt \_ \_ \_ wird.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 123e0eb12a187ee6a5b7665ec126ba98153638e9d766015a0c9e7b1c7aec7dee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924080"
---
# <a name="the-named_type_free_local-function"></a>Die lokale \_ \_ Funktion "Free" des \_ benannten Typs

Die Stubs rufen die **\_ \_ lokale Funktion type free** auf, um den Arbeitsspeicher freizugeben, der durch einen Aufruf des benannten Typs an die [ \_ \_ \_ lokale](the-named-type-to-local-function.md) Routine belegt wird. Der vom Stub belegte Arbeitsspeicher wird nicht freigegeben. Der Funktionsprototyp ist wie folgt definiert:

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

Der -Parameter ist ein Zeiger auf den Arbeitsspeicher, der vom **benannten \_ Typ dem \_ \_ lokalen** zugeordnet wird.

 

 




