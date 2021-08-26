---
title: " in, string und out, string Prototype"
description: 'Der folgende Funktionsprototyp verwendet zwei Parameter: "\in", "string\parameter" und "\out", "string\".'
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498d12c85130bba8d7d8dcddfc400e2a90fa2d0e2c3cb11c4a7d89696cfe9aa4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073620"
---
# <a name="in-string-and-out-string-prototype"></a>\[in, string \] und \[ out, string \] Prototype

Der folgende Funktionsprototyp verwendet zwei Parameter: \[ [**einen in**](/windows/desktop/Midl/in), [**einen Zeichenfolgenparameter**](/windows/desktop/Midl/string) \] und einen \[ [**out-Zeichenfolgenparameter.**](/windows/desktop/Midl/out-idl)  \]

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

Der erste Parameter ist \[ [**nur in**](/windows/desktop/Midl/in) \] . Diese Eingabezeichenfolge wird nur vom Client an den Server übertragen. Der Server verwendet ihn als Grundlage für die weitere Verarbeitung. Die Zeichenfolge wird nicht geändert und wird vom Client nicht erneut benötigt, sodass sie nicht an den Client zurückgegeben werden muss.

Der zweite Parameter, der die Antwort des Ärztes darstellt, \[ [**ist nur**](/windows/desktop/Midl/out-idl) \] out. Diese Antwortzeichenfolge wird nur vom Server an den Client übertragen. Die Zuordnungsgröße wird bereitgestellt, damit die Serverstubs Arbeitsspeicher dafür zuordnen können. Da *pszOutput* ein \[ [**Verweiszeiger**](/windows/desktop/Midl/ref) ist, muss dem Client vor dem Aufruf ausreichend Arbeitsspeicher für die \] Zeichenfolge zugeordnet sein. Die Antwortzeichenfolge wird in diesen Speicherbereich geschrieben, wenn die Remoteprozedur zurückgegeben wird.

 

 