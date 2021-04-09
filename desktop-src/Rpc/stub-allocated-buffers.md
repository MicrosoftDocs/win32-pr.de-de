---
title: Stub-Allocated Puffer
description: Anstatt einen separaten Aufruf für jeden Knoten der Struktur oder des Diagramms zu erzwingen, können Sie die Stub anweisen, die Größe der Daten zu berechnen und Arbeitsspeicher zuzuordnen und freizugeben, indem Sie einen einzelnen Aufruf an die mittlere Benutzer Zuordnungs- \_ \_ oder mittellose Benutzer Freigabe richten \_ \_ .
ms.assetid: 9911649d-00e8-47d8-b512-7d9b185d1e09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956acf6452c1a4e7d04afcd1da263439436e3bad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039334"
---
# <a name="stub-allocated-buffers"></a>Stub-Allocated Puffer

Anstatt einen separaten Aufruf für jeden Knoten der Struktur oder des Diagramms zu erzwingen, können Sie die Stub anweisen, die Größe der Daten zu berechnen und Arbeitsspeicher zuzuordnen und freizugeben, indem Sie einen einzelnen Aufruf an die [mittlere \_ Benutzer \_ ](/windows/desktop/Midl/midl-user-allocate-1) Zuordnungs-oder [mittellose \_ Benutzer \_ ](/windows/desktop/Midl/midl-user-free-1)Freigabe richten. Das ACF-Attribut " **\[ zuordnen" (alle \_ Knoten) \]** weist die Stub an, alle Knoten in einem einzelnen Rückruf der vom Benutzer bereitgestellten –-Speicherverwaltungsfunktionen zuzuordnen oder freizugeben.

Eine RPC-Anwendung könnte z. b. die folgende binäre Strukturdaten Struktur verwenden:

``` syntax
/* IDL file fragment */
typedef struct _TREE_TYPE 
{
    short sNumber;
    struct _TREE_TYPE * pLeft;
    struct _TREE_TYPE * pRight;
} TREE_TYPE;

typedef TREE_TYPE * P_TREE_TYPE;
```

Das auf diesen Datentyp angewendete ACF-Attribut **\[ (alle \_ Knoten \] )** wird in der **typedef** -Deklaration in der ACF wie folgt angezeigt:

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes)] P_TREE_TYPE;
```

Das Attribut " **\[ zuordnen \]** " kann nur auf Zeiger Typen angewendet werden. Das Attribut "Zuordnungs-ACF" ist eine Microsoft-Erweiterung für DCE IDL und ist daher nicht verfügbar, wenn Sie mit dem **/OSF** -Schalter für mittlere Kompilierung kompilieren. **\[ \]** Wenn "Allocation **\[ (alle \_ Knoten \] )** " auf einen Zeigertyp angewendet wird, durchlaufen die vom Mittelwert Compiler generierten Stuben die angegebene Datenstruktur, um die Zuordnungs Größe zu bestimmen. Die Stub erstellen dann einen einzelnen Aufruf, um die gesamte Menge an Arbeitsspeicher zuzuordnen, die für das Diagramm oder die Struktur benötigt wird. Eine Client Anwendung kann viel effizienter Arbeitsspeicher freigeben, indem Sie einen einzelnen aufzurufenden **\_ Benutzer \_ kostenlos** aufruft. Die Server-Stub-Leistung wird jedoch im Allgemeinen bei der Verwendung der Knoten Speicher Belegung (Knoten Weise) gesteigert, da die Serverstubs häufig privaten Speicher verwenden können, der keine Zuweisungen erfordert.

Weitere Informationen finden Sie unter [Zuordnung und Aufhebung der Zuordnung von Knoten](node-by-node-allocation-and-deallocation.md)zu Knoten.

 

 