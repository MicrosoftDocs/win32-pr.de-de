---
title: Vorbereiten der Anwendung für 64-Bit-Windows
description: Es gibt mehrere Features, die ihnen die Entwicklung von Anwendungen erleichtern, die sowohl auf 32- als auch auf 64-Bit-Windows. Die meisten dieser Datentypen, z. B. die neuen Datentypen, werden unter Getting Ready for 64-bit Windows.
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- 64-Bit-Toolkit 64-Bit-Windows Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6c8d31b685e6f545aca4bdaac341fe25a3c96f458048808536899a8416120a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071620"
---
# <a name="preparing-your-application-for-64-bit-windows"></a>Vorbereiten der Anwendung für 64-Bit-Windows

Es gibt mehrere Features, die ihnen die Entwicklung von Anwendungen erleichtern, die sowohl auf 32- als auch auf 64-Bit-Windows. Die meisten dieser Datentypen, z. B. die neuen Datentypen, werden unter [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).

Das im Windows SDK enthaltene 64-Bit-Toolkit enthält einen 64-Bit-MIDL-Compiler Midl.exe zum Generieren nativer 64-Bit-Stubs sowie 32-Bit-Stubs. Verwenden Sie **den Schalter /env win64,** um nur 64-Bit-Stubs zu generieren. Standardmäßig werden duale Stubs generiert, die auf beiden Plattformen ausgeführt werden.

Beachten Sie, dass die 64-Bit-MIDL nur die [**Optimierungsmodi /Oicf**](/windows/desktop/Midl/-oi) und [**/Os**](/windows/desktop/Midl/-os) unterstützt.

 

 