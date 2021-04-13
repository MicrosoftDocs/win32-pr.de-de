---
title: Die named_type_from_local-Funktion
description: Die stubzeichen nennen den benannten \_ Typ \_ von der \_ lokalen Funktion.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94606a197f3763770db8e0d455a9d0b09f5dab0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309603"
---
# <a name="the-named_type_from_local-function"></a>Der benannte \_ Typ \_ aus der \_ lokalen Funktion.

Die stubzeichen nennen den benannten \_ Typ \_ von der \_ lokalen Funktion. Der Typ, der von der Anwendung verwendet wird, wird in den Typ konvertiert, den die stusb über das Netzwerk übertragen. Die-Funktion ist wie folgt definiert:

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

Der erste Parameter ist ein Zeiger auf die Anwendungsdaten. Der zweite Parameter ist ein Zeiger auf einen Zeiger. Die Funktion verweist auf die übertragenen Daten. Die Funktion muss Arbeitsspeicher für den übertragenen Typ zuweisen.

 

 




