---
title: Application-Allocated Puffer
description: Das ACF-Attribut \ Byte \_ Anzahl \ weist die Stub an, einen vorab zugeordneten Puffer zu verwenden, der nicht von den Client-Unterstützungs Routinen zugeordnet oder freigegeben wird.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db533495f16d37aca0bdae96035783650573a60f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473916"
---
# <a name="application-allocated-buffer"></a>Application-Allocated Puffer

Die Byte Anzahl der ACF-Attribute weist \[ [**\_**](/windows/desktop/Midl/byte-count) \] die Stub an, einen vorab zugeordneten Puffer zu verwenden, der nicht von den Client-Unterstützungs Routinen zugeordnet oder freigegeben wird. Das \[ **Byte \_ count** - \] Attribut wird auf einen Zeiger-oder Array Parameter angewendet, der auf den Puffer zeigt. Hierfür ist ein Parameter erforderlich, der die Puffergröße in Bytes angibt.

Der vom Client zugewiesene Speicherbereich kann komplexe Datenstrukturen mit mehreren Zeigern enthalten. Da der Speicherbereich zusammenhängend ist, muss die Anwendung nicht mehrere Aufrufe durchführen, um jeden Zeiger und jede Struktur einzeln freizugeben. Wie bei Verwendung des Attributs "Allocation" \[ [**(alle \_ Knoten)**](/windows/desktop/Midl/allocate) \] kann der Speicherbereich mit einem Rückruf der Speicher Belegungs Routine oder der kostenlosen Routine zugeordnet oder freigegeben werden. Anders als bei Verwendung des \[ Attributs " **zuordnen" (alle \_ Knoten)** \] wird der Puffer Parameter jedoch nicht vom Client-Stub, sondern von der Client Anwendung verwaltet.

Der Puffer muss ein \[ [](/windows/desktop/Midl/out-idl) \] nur-Out-Parameter sein, und die Pufferlänge in Byte muss ein \[ [](/windows/desktop/Midl/in) \] nur-der-Parameter sein. Das \[ [**Byte \_ count**](/windows/desktop/Midl/byte-count) - \] Attribut kann nur auf Zeiger Typen angewendet werden. Das \[ ACF-Attribut für die **Byte \_ Anzahl** \] ist eine Microsoft-Erweiterung für DCE-IDL und ist daher nicht verfügbar, wenn Sie mit dem [**/OSF**](/windows/desktop/Midl/-osf) -Schalter für mittlere Kompilierung kompilieren.

Im folgenden Beispiel verwendet der Parameter *Proot* Byte Anzahl:

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

Das \[ [**Byte \_ count**](/windows/desktop/Midl/byte-count) - \] Attribut wird in der ACF wie folgt angezeigt:

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

Der von diesen IDL-und ACF-Dateien generierte Clientstub weist den Speicher für diesen Puffer nicht zu oder gibt diesen frei. Der Serverstub ordnet den Puffer zu und gibt ihn in einem einzelnen-Befehl mit dem angegebenen Size-Parameter frei. Wenn die Daten für die angegebene Puffergröße zu groß sind, wird eine Ausnahme ausgelöst.

 

 