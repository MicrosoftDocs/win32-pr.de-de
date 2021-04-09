---
description: Netzwerkmonitor Ruft die formatproperties-Funktion auf, um die Daten zu formatieren, die im Detailbereich der Netzwerkmonitor Benutzeroberfläche angezeigt werden.
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: Implementieren von formatproperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660b581bf29fd8e5d40af65f5ff90e1e9223ad2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128913"
---
# <a name="implementing-formatproperties"></a>Implementieren von formatproperties

Netzwerkmonitor Ruft die [**formatproperties**](formatproperties.md) -Funktion auf, um die Daten zu formatieren, die im Detailbereich der Netzwerkmonitor Benutzeroberfläche angezeigt werden. Normalerweise wird **formatproperties** aufgerufen, um die Zusammenfassungs Zeile für ein Protokoll zu formatieren, und dann alle Eigenschaften Instanzen des Protokolls innerhalb eines Frames zu formatieren. Netzwerkmonitor gibt jedoch nicht an, wie oft **formatproperties** für einen bestimmten Parser aufgerufen wird.

Beim Aufrufen von [**formatproperties**](formatproperties.md)stellt Netzwerkmonitor eine [**propertyinst**](propertyinst.md) -Struktur für jede angezeigte Eigenschaft bereit. Die **propertyinst** -Struktur stellt Informationen zu den anzuzeigenden Daten bereit, einschließlich eines Zeigers auf die [**PropertyInfo**](propertyinfo.md) -Struktur, die die Funktion angibt, die zum Formatieren der angezeigten Dateneigenschaft verwendet werden soll.

> [!Note]  
> Eine [**PropertyInfo**](propertyinfo.md) -Struktur wird angegeben, wenn der- [*Eigenschaften Datenbank*](p.md) des Parsers eine Eigenschaft hinzugefügt wird.

 

Netzwerkmonitor identifiziert die Formatierungsfunktion, die für jede Eigenschaften Instanz aufgerufen werden soll. Der **InstanceData** -Member der [**PropertyInfo**](propertyinfo.md) -Struktur kann Folgendes angeben:

-   Die [**formatpropertyinstance**](formatpropertyinstance.md) -Funktion, um den von Netzwerkmonitor bereitgestellten [*generischen Formatierer*](g.md) zu verwenden.

    – oder –

-   Der Name einer benutzerdefinierten Format Funktion, die der Parser bereitstellt.

Die [**formatpropertyinstance**](formatpropertyinstance.md) und die benutzerdefinierten Formatfunktionen geben die formatierten Daten zurück, die im Detailbereich der Netzwerkmonitor-Benutzeroberfläche angezeigt werden.

In der folgenden Abbildung wird gezeigt, wie Netzwerkmonitor die Funktion identifiziert, die für jede Eigenschaften Instanz aufgerufen werden soll.

![Identifizieren der aufzurufenden Funktion durch den Netzwerkmonitor](images/formatprop1.png)

Im folgenden Verfahren werden die erforderlichen Schritte zum Implementieren von [**formatproperties**](formatproperties.md)beschrieben.

**So implementieren Sie Format Properties**

-   Rufen Sie mithilfe einer Schleifen Struktur die Format-Funktion für jede [**propertyinst**](propertyinst.md) -Struktur auf, die dem Parser im *lppropinst* -Parameter der [**formatproperties**](formatproperties.md) -Funktion übergeben wird.

Im folgenden finden Sie eine grundlegende Implementierung von [**formatproperties**](formatproperties.md).

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

 

 



