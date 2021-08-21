---
title: Übersetzen in Java aus C++
description: Mithilfe der Programmiersprache C++ können Entwickler direkt auf den Arbeitsspeicher zugreifen, der eine bestimmte Variable speichert. Arbeitsspeicherzeker bieten diesen direkten Zugriff. In Java werden Zeiger für Sie verarbeitet.
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73efe022fa09ce13a2d5e4e04978033fc3ab8f33abb6afb3b5abf493dab12178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047748"
---
# <a name="translating-to-java-from-c"></a>Übersetzen in Java aus C++

Mithilfe der Programmiersprache C++ können Entwickler direkt auf den Arbeitsspeicher zugreifen, der eine bestimmte Variable speichert. Arbeitsspeicherzeker bieten diesen direkten Zugriff. In Java werden Zeiger für Sie verarbeitet.

In Java werden zusammengesetzte **Datentypen** **struct,** union und **typedef** ausschließlich mithilfe von Klassen behandelt. Der C++-Datentyp **VARIANT** wird z. B. **com.ms.com.Variant** in Java angezeigt.

In C++ sind Zeichenfolgen ein Array von Zeichen. In Java sind Zeichenfolgen Objekte. Methoden, die auf Zeichenfolgen wirken, behandeln die Zeichenfolge als vollständiges -Objekt.

COM-Methoden geben einen Wert zurück, der als **HRESULT** bezeichnet wird. Dabei handelt es sich um einen 32-Bit-Fehlercode. Die Java-Unterstützung für Microsoft Internet Explorer definiert die Klasse **com.ms.com.ComException,** die den **HRESULT-Fehlercode** umgibt.

Java unterstützt keine Datentypen ohne Vorzeichen, mit Ausnahme **von char**, bei dem es sich um eine 16-Bit-Ganzzahl ohne Vorzeichen handelt. Methoden, die andere Datentypen ohne Vorzeichen akzeptieren oder zurückgeben, können nicht von Java verwendet werden.

Java unterstützt keine mehrdimensionalen Arrays. Methoden, die mehrdimensionale Arrays akzeptieren oder zurückgeben, sind in Java nicht verfügbar.

Boolesche Werte in Java können nicht in 0 und 1 castt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in Java](translating-to-java.md)
</dt> </dl>

 

 




