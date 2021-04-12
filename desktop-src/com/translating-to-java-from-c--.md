---
title: Übersetzen in Java aus C++
description: Mithilfe der Programmiersprache C++ können Entwickler direkt auf den Speicher zugreifen, in dem eine bestimmte Variable gespeichert wird. Speicher Zeiger bieten diesen direkten Zugriff. In Java werden Zeiger für Sie behandelt.
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf63754782cba82819479a7e26535b518835580b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388022"
---
# <a name="translating-to-java-from-c"></a>Übersetzen in Java aus C++

Mithilfe der Programmiersprache C++ können Entwickler direkt auf den Speicher zugreifen, in dem eine bestimmte Variable gespeichert wird. Speicher Zeiger bieten diesen direkten Zugriff. In Java werden Zeiger für Sie behandelt.

In Java werden zusammengesetzte Datentypen " **struct**", " **Union**" und " **typedef** " ausschließlich durch die Verwendung von Klassen behandelt. Der Datentyp C++ **Variant** ist beispielsweise com. **ms. com. Variant** in Java zugeordnet.

In C++ sind Zeichen folgen ein Zeichen Array. In Java sind Zeichen folgen Objekte. Methoden, die auf Zeichen folgen reagieren, behandeln die Zeichenfolge als ein ganzes Objekt.

COM-Methoden geben einen als **HRESULT** bezeichneten Wert zurück, bei dem es sich um einen 32-Bit-Fehlercode handelt. Die Java-Unterstützung für Microsoft Internet Explorer definiert die Klasse **com. ms. com. COMException**, die den **HRESULT** -Fehlercode umschließt.

Java unterstützt keine unsignierten Datentypen mit Ausnahme von **char**, eine 16-Bit-Ganzzahl ohne Vorzeichen. Methoden, die andere nicht signierte Datentypen akzeptieren oder zurückgeben, können nicht in Java verwendet werden.

Java unterstützt keine mehrdimensionalen Arrays. Methoden, die mehrdimensionale Arrays akzeptieren oder zurückgeben, sind von Java aus nicht verfügbar.

Boolesche Werte in Java können nicht in 0 und 1 umgewandelt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in Java](translating-to-java.md)
</dt> </dl>

 

 




