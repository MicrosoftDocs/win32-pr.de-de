---
description: In diesem Thema werden die Unterschiede zwischen den Binärversionen der Tablet PC-Bibliothek beschrieben.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: Welche Bibliotheks Version soll referenziert werden?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f2092cc762a047ac5f0c2408a87f761fc584a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346933"
---
# <a name="which-library-version-to-reference"></a>Welche Bibliotheks Version soll referenziert werden?

In diesem Thema werden die Unterschiede zwischen den Binärversionen der Tablet PC-Bibliothek beschrieben.

## <a name="tablet-pc-library-versions"></a>Tablet PC-Bibliotheksversionen

Die Binärdateien der Tablet PC-Bibliothek (Microsoft.Ink.dll) wurden in Windows Vista aktualisiert. Diese Binärdateien werden als "Version 6,0" bezeichnet, um zusammen mit der Windows-Version, in der Sie veröffentlicht werden, eine Zusammenfassung zu finden.

Die neueste Version der Binärdateien, die mit Windows XP kompatibel sind, wird als "Version 1,7" bezeichnet.

Der Windows SDK kann sowohl auf Vista-als auch auf XP-Computern installiert werden, und die Windows SDK umfasst beide Versionen von Microsoft.Ink.dll.

Diese werden in installiert:

1. % Program Files% \\ Verweisassemblys \\ Microsoft \\ Tablet PC \\ v 1.7 \\Microsoft.Ink.dll

2. % Program Files% \\ Verweisassemblys \\ Microsoft \\ Tablet PC \\ v 6.0 \\Microsoft.Ink.dll

Die Binärdateien der Version 6,0 sind nur mit Windows Vista kompatibel, und Anwendungen, die für diese geschrieben wurden, sollten nur unter Windows Vista ausgeführt werden.

Eine Anwendung, die für die Binärdateien der Version 1,7 geschrieben wurde, sollte unverändert bei der Installation unter Windows Vista ausgeführt werden.

 

 



