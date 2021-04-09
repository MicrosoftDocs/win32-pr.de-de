---
title: Vollständige Zeiger
description: Im Gegensatz zu eindeutigen Zeigern unterstützen vollständige Zeiger Aliasing.
ms.assetid: 38023942-a4c2-4de7-b7d5-10d508cf083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18687b496ddd28dca9e70afca8deafb18774500a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948845"
---
# <a name="full-pointers"></a>Vollständige Zeiger

Im Gegensatz zu [eindeutigen](unique-pointers.md) Zeigern unterstützen vollständige Zeiger Aliasing. Dies bedeutet, dass mehrere Zeiger auf dieselben Daten verweisen können, wie in der folgenden Abbildung dargestellt:

![zwei Zeiger, die auf dieselben Daten verweisen](images/prog-a02.png)

Ein vollständiger Zeiger weist die folgenden Eigenschaften auf:

-   Der Wert kann NULL sein.
-   Sie kann während des-Aufrufes von NULL in ungleich NULL wechseln. Wenn der Wert in einen nicht-NULL-Wert geändert wird, ordnet der Clientstub der Rückgabe einen neuen Arbeitsspeicher zu. Das Client Programm sollte diesen Arbeitsspeicher freigeben, bevor er beendet wird.
-   Sie kann während des Aufrufes von ungleich NULL zu NULL wechseln. Wenn der Wert in NULL geändert wird, ist die Anwendung dafür verantwortlich, den Arbeitsspeicher freizugeben.
-   Der Wert kann von einem nicht-NULL-Wert in einen anderen Wert geändert werden.
-   Auf den Speicher, auf den ein vollständiger Zeiger zeigt, wird möglicherweise ein anderer Zeiger oder Name im Vorgang aufgerufen.
-   Rückgabe Daten werden in den vorhandenen Speicher geschrieben, wenn der Zeiger nicht den Wert NULL hat.

Verwenden Sie das \[ [**ptr**](/windows/desktop/Midl/ptr) - \] Attribut, um einen vollständigen Zeiger anzugeben, wie im folgenden Beispiel gezeigt:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface FullPtrInterface
{
  void RemoteFn([in,ptr,string]) char *ptrName1,
                [in,ptr,string]  char *ptrName2);
}
```

In diesem Beispiel werden die Parameter *ptrName1* und *ptrName2* als vollständige Zeiger auf eine Zeichenfolge definiert. Beide Zeiger können auf dieselbe Speicheradresse zeigen, die eine einzelne Zeichenfolge enthält.

\[**ptr** \] ist beim Bereitstellen von Aliasing-Unterstützung erforderlich. Da es jedoch die meiste Verarbeitung aller in RPC verfügbaren Zeiger erfordert, wird es für die meisten Anwendungen nicht empfohlen.

 

 