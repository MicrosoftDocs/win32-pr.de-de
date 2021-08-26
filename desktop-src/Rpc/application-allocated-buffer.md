---
title: Application-Allocated Buffer
description: Das ACF-Attribut \byte count\ leitet die Stubs an, einen vorab zugeordneten Puffer zu verwenden, der nicht von den Clientunterstützungsroutinen zugeordnet oder \_ frei wird.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb87390637cba57cbdf4021a43f4ec98ea64c3828c67dfdb615ffcd62dc8c16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024180"
---
# <a name="application-allocated-buffer"></a>Application-Allocated Buffer

Die \[ [**Byteanzahl \_**](/windows/desktop/Midl/byte-count) des ACF-Attributs leitet die Stubs an, einen vorab zugeordneten Puffer zu verwenden, der von den Clientunterstützungsroutinen nicht zugeordnet oder \] frei wird. Das \[ **\_ Byteanzahlattribut** \] wird auf einen Zeiger oder Arrayparameter angewendet, der auf den Puffer zeigt. Sie erfordert einen Parameter, der die Puffergröße in Bytes angibt.

Der vom Client zugewiesene Speicherbereich kann komplexe Datenstrukturen mit mehreren Zeigern enthalten. Da der Speicherbereich zusammenhängend ist, muss die Anwendung nicht mehrere Aufrufe tätigen, um jeden Zeiger und jede Struktur einzeln frei zu geben. Wie bei Verwendung des \[ [**Attributs allocate(all \_ nodes)**](/windows/desktop/Midl/allocate) kann der Arbeitsspeicherbereich mit einem Aufruf der Speicherzuordnungsroutine oder der freien Routine zugeordnet oder \] freigerufen werden. Im Gegensatz zur Verwendung des \[ **Attributs allocate(all \_ nodes)** wird der Pufferparameter jedoch nicht vom Clientstub, \] sondern von der Clientanwendung verwaltet.

Der Puffer muss ein \[ [](/windows/desktop/Midl/out-idl) \] out-only-Parameter sein, und die Pufferlänge in Bytes muss ein \[ [**in**](/windows/desktop/Midl/in) \] -only-Parameter sein. Das \[ [**\_ Byteanzahlattribut**](/windows/desktop/Midl/byte-count) \] kann nur auf Zeigertypen angewendet werden. Das Byteanzahl-ACF-Attribut ist eine Microsoft-Erweiterung für DCE-IDL und daher nicht verfügbar, wenn Sie mit dem \[ **\_** \] [**MIDL/osf-Switch kompilieren.**](/windows/desktop/Midl/-osf)

Im folgenden Beispiel verwendet der *Parameter pRoot* die Byteanzahl:

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

Das \[ [**\_ Byteanzahlattribut**](/windows/desktop/Midl/byte-count) \] wird im ACF wie im folgenden Beispiel angezeigt:

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

Der aus diesen IDL- und ACF-Dateien generierte Clientstub weist den Arbeitsspeicher für diesen Puffer nicht zu oder gibt diesen frei. Der Serverstub ordnet den Puffer in einem einzigen Aufruf zu und gibt ihn mithilfe des angegebenen Größenparameters frei. Wenn die Daten für die angegebene Puffergröße zu groß sind, wird eine Ausnahme ausgelöst.

 

 