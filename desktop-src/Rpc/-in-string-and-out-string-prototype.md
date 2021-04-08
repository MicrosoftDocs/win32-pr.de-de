---
title: " in, String und Out, Zeichen folgen Prototyp"
description: Der folgende Funktionsprototyp verwendet die beiden Parameter a \ in, String \ Parameter und a \ Out, String \ Parameter.
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c216197fb33a666029429d98761b3219b27b176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949056"
---
# <a name="in-string-and-out-string-prototype"></a>\[in, String \] und \[ out, Zeichen folgen \] Prototyp

Der folgende Funktionsprototyp verwendet zwei Parameter: einen \[ [**in**](/windows/desktop/Midl/in), einen [**Zeichen**](/windows/desktop/Midl/string) folgen \] Parameter und einen \[ [**out**](/windows/desktop/Midl/out-idl)- **Zeichen** folgen \] Parameter.

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

Der erste Parameter ist \[ nur [**in**](/windows/desktop/Midl/in) \] . Diese Eingabe Zeichenfolge wird nur vom Client an den Server übertragen. Der Server verwendet ihn als Grundlage für die weitere Verarbeitung. Die Zeichenfolge wird nicht geändert und wird vom Client nicht erneut benötigt, sodass Sie nicht an den Client zurückgegeben werden muss.

Der zweite Parameter, der die Antwort des Arztes darstellt, ist \[ [](/windows/desktop/Midl/out-idl) \] nur out. Diese Antwort Zeichenfolge wird nur vom Server an den Client übermittelt. Die Zuordnungs Größe wird bereitgestellt, damit die Server-stubspeicher für Sie Speicher belegen können. Da *pszoutput* ein \[ [**ref**](/windows/desktop/Midl/ref) - \] Zeiger ist, muss dem Client vor dem-Befehl ausreichend Arbeitsspeicher für die Zeichenfolge zugeordnet werden. Die Antwort Zeichenfolge wird in diesen Bereich des Arbeitsspeichers geschrieben, wenn die Remote Prozedur zurückgibt.

 

 