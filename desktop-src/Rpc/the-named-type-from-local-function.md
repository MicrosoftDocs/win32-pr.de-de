---
title: Die named_type_from_local-Funktion
description: Die Stubs rufen den benannten \_ Typ aus der lokalen Funktion \_ \_ auf.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c294398913a3bf6fe8b88eed5c42ceec84abf6b23ed994c85ff0fae8f21f2e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127620"
---
# <a name="the-named_type_from_local-function"></a>Der benannte \_ Typ aus der lokalen \_ \_ Funktion

Die Stubs rufen den benannten \_ Typ aus der lokalen Funktion \_ \_ auf. Sie konvertiert den Typ, den die Anwendung verwendet, in den Typ, den die Stubs über das Netzwerk übertragen. Die Funktion ist wie folgt definiert:

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

Der erste Parameter ist ein Zeiger auf die Anwendungsdaten. Der zweite Parameter ist ein Zeiger auf einen Zeiger. Die Funktion verweist sie auf die übertragenen Daten. Die Funktion muss Speicher für den übertragenen Typ zuordnen.

 

 




