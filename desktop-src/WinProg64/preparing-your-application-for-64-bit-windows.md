---
title: Vorbereiten der Anwendung für 64-Bit-Windows
description: Es gibt mehrere Features, die es Ihnen erleichtern, Anwendungen zu entwickeln, die auf 32-und 64-Bit-Fenstern ausgeführt werden können. Die meisten dieser Informationen, wie z. b. die neuen Datentypen, werden unter Vorbereiten für 64-Bit-Windows beschrieben.
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- 64-Bit-Toolkit 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f3b40d2fb22b84abdd4322f476981dc54c7ad3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209333"
---
# <a name="preparing-your-application-for-64-bit-windows"></a>Vorbereiten der Anwendung für 64-Bit-Windows

Es gibt mehrere Features, die es Ihnen erleichtern, Anwendungen zu entwickeln, die auf 32-und 64-Bit-Fenstern ausgeführt werden können. Die meisten dieser Informationen, wie z. b. die neuen Datentypen, werden unter [vorbereiten für 64-Bit-Windows](getting-ready-for-64-bit-windows.md)beschrieben.

Das 64-Bit-Toolkit, das im Lieferumfang des Windows SDK enthalten ist, enthält einen 64-Bit-Mittelwert Compiler, Midl.exe, zum Erstellen von nativen 64-Bit-stubwerten sowie 32-Bit-stubwerte. Verwenden Sie den Schalter **/env Win64** , um nur 64-Bit-stubwerte zu generieren. Standardmäßig werden duale stubwerte generiert, die auf beiden Plattformen ausgeführt werden.

Beachten Sie, dass die 64-Bit-Mittell nur die Optimierungs Modi [**/Oicf**](/windows/desktop/Midl/-oi) und [**/OS**](/windows/desktop/Midl/-os) unterstützt.

 

 