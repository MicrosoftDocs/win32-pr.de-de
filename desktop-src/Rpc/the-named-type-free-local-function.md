---
title: Die named_type_free_local-Funktion
description: Der stubspeicher Ruft den Typ " \_ freie \_ lokale Funktion" auf, um den von einem Aufrufen des benannten Typs zugeordneten Arbeitsspeicher \_ für die \_ \_ lokale Routine freizugeben.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f2796f33e9dc60364b6afda244d8dae47eef0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709089"
---
# <a name="the-named_type_free_local-function"></a>Die benannte \_ \_ typfreie \_ lokale Funktion

Der stubspeicher Ruft den **Typ " \_ freie \_ lokale** Funktion" auf, um den von einem Aufrufen des benannten Typs zugeordneten Arbeitsspeicher [ \_ für die \_ \_ lokale](the-named-type-to-local-function.md) Routine freizugeben. Der vom Stub zugeordnete Arbeitsspeicher wird nicht freigegeben. Der Funktionsprototyp wird wie folgt definiert:

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

Der-Parameter ist ein Zeiger auf den Arbeitsspeicher **, der vom benannten \_ Typ \_ zu \_ local** zugeordnet wird.

 

 




