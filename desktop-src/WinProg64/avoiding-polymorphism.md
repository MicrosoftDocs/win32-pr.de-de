---
title: Vermeiden von Polymorphie
description: Die neuen Datentypen umfassen die beiden polymorphen Typen int \_ ptr und Long \_ ptr.
ms.assetid: 3d18016d-772c-45bc-8057-7281e71a8707
keywords:
- Polymorphie 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec0fd26944d58a9ba0d253da8b8dbcd68156436
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311105"
---
# <a name="avoiding-polymorphism"></a>Vermeiden von Polymorphie

Die neuen Datentypen umfassen die beiden polymorphen Typen **int \_ ptr** und **Long \_ ptr**. Bei 32-Bit-Fenstern wird das **int- \_ ptr** **int** und der **lange \_ ptr** -Wert **Long** zugeordnet. Bei 64-Bit-Fenstern werden beide Typen dem systeminternen **\_ \_ Int64** -Typ zugeordnet. Der mittlerer l-Compiler unterstützt diese Typen für Remote Prozedur Aufrufe, aber es gibt eine inhärente Einschränkung, die Sie berücksichtigen müssen, wenn Sie in einer verteilten Umgebung verwendet werden. Stellen Sie sicher, dass Sie Ihren Code entsprechend kommentieren.

Unabhängig von der Platt Form Größe ist die Wire-Größe dieser polymorphen Typen immer 32 Bits. Wenn das Marshalling bei 64-Bit-Fenstern durchgeführt wird, erweitert das Lauf Zeit Bibliotheks Zeichen signierte Werte und weist der höherwertigen Bytes für einen Wert ohne Vorzeichen NULL zu. Wenn Sie einen 64-Bit-Wert für die Übertragung platzieren, verkürzt die Laufzeit die höherwertigen Bytes. Daher können nur die 32-Bit-Werte in niedriger Reihenfolge verwendet werden.

Verwenden Sie die polymorphen Typen nur, wenn dies für das Portieren erforderlich ist. Verwenden Sie für neue Schnittstellen die systeminternen ganzzahligen Typen **\_ \_ Int32** und **\_ \_ Int64**, oder verwenden Sie einen Zeigertyp oder ein Kontext Handle, je nachdem, welcher Typ für die übertragene Art von Daten am besten geeignet ist.

Der 64-Bit-Compiler unterstützt eine neue polymorphe intrinsische **\_ \_ int3264**. Dieser Typ wurde ebenfalls entwickelt, um das Portieren zu unterstützen, in diesem Fall, um die **uint- \_ ptr** -Typen transparent zu unterstützen. (Eine andere intrinsische, **\_ \_ long3264**-Unterstützung unterstützt den **ulong \_ ptr** -Typ.) Verwenden Sie **\_ \_ int3264** nicht direkt. verwenden Sie den **int- \_ ptr** -Typ, wenn Sie für Portierungs Gründe einen polymorphen Typ benötigen.

 

 




