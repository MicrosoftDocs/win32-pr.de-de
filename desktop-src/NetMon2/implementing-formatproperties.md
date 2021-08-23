---
description: Netzwerkmonitor ruft die FormatProperties-Funktion auf, um die Daten zu formatieren, die im Detailbereich der Netzwerkmonitor werden.
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: Implementieren von FormatProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50e7b927f15ccb2c216e345b37bc87593e33339671f906e28d33759ca9db0abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778974"
---
# <a name="implementing-formatproperties"></a>Implementieren von FormatProperties

Netzwerkmonitor ruft die [**FormatProperties-Funktion**](formatproperties.md) auf, um die Daten zu formatieren, die im Detailbereich der Netzwerkmonitor werden. In der Regel wird **FormatProperties** aufgerufen, um die Zusammenfassungszeile für ein Protokoll zu formatieren und dann alle Eigenschafteninstanzen des Protokolls innerhalb eines Frames zu formatieren. Allerdings Netzwerkmonitor nicht, wie oft **FormatProperties** für einen bestimmten Parser aufgerufen wird.

Beim Aufrufen [**von FormatProperties**](formatproperties.md)stellt Netzwerkmonitor [**eine PROPERTYINST-Struktur**](propertyinst.md) für jede angezeigte Eigenschaft zur Verfügung. Die **PROPERTYINST-Struktur** stellt Informationen zu den anzuzeigenden Daten zur Verfügung, einschließlich eines Zeigers auf die [**PROPERTYINFO-Struktur,**](propertyinfo.md) der die Funktion angibt, die zum Formatieren der angezeigten Dateneigenschaft verwendet werden soll.

> [!Note]  
> Eine [**PROPERTYINFO-Struktur**](propertyinfo.md) wird angegeben, wenn der Eigenschaftendatenbank [*des*](p.md) Parsers eine Eigenschaft hinzugefügt wird.

 

Netzwerkmonitor identifiziert die Formatfunktion, die für jede Eigenschafteninstanz aufruft werden soll. Der **InstanceData-Member** der [**PROPERTYINFO-Struktur**](propertyinfo.md) kann Folgendes angeben:

-   Die [**FormatPropertyInstance-Funktion**](formatpropertyinstance.md) zur Verwendung des [*generischen Formatierungsers,*](g.md) den Netzwerkmonitor bietet.

    – oder –

-   Der Name einer benutzerdefinierten Formatfunktion, die der Parser zur Verfügung stellt.

Die [**FormatPropertyInstance-**](formatpropertyinstance.md) und die benutzerdefinierten Formatfunktionen geben die formatierten Daten zurück, die im Detailbereich der benutzeroberfläche Netzwerkmonitor werden.

Die folgende Abbildung zeigt, Netzwerkmonitor die Funktion identifiziert, die für jede Eigenschafteninstanz aufruft.

![Wie der Netzwerkmonitor die aufrufende Funktion identifiziert](images/formatprop1.png)

Im folgenden Verfahren werden die erforderlichen Schritte zum Implementieren von [**FormatProperties beschrieben.**](formatproperties.md)

**So implementieren Sie FormatProperties**

-   Rufen Sie mithilfe einer Schleifenstruktur die Formatfunktion für jede [**PROPERTYINST-Struktur**](propertyinst.md) auf, die im *lpPropInst-Parameter* der [**FormatProperties-Funktion**](formatproperties.md) an den Parser übergeben wird.

Im Folgenden finden Sie eine grundlegende Implementierung von [**FormatProperties**](formatproperties.md).

``` syntax
#include <windows.h>

DWORD BHAPI MyProtocolFormatProperties( HFRAME hFrame,
                                        LPBYTE         pMacFrame,
                                        LPBYTE         pBLRPLATEFrame,
                                        DWORD          nPropertyInsts
                                        LPPROPERTYINST  p)
  {
    while( nPropertyInsts-- > 0)
      {
         ( (FORMAT) p->lpPropertyInfo->InstanceData) ) (p);
         p++;
      }
  return BHERR_SUCCESS;
  }
```

 

 



