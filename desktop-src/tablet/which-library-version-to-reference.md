---
description: In diesem Thema werden die Unterschiede zwischen den Binärversionen der Tablet PC-Bibliothek beschrieben.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: Auf welche Bibliotheksversion verwiesen werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 899866dd11bbe72f9476ee3b645ed4e5612fe7043dae38675bd206e81562ca68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589280"
---
# <a name="which-library-version-to-reference"></a>Auf welche Bibliotheksversion verwiesen werden soll

In diesem Thema werden die Unterschiede zwischen den Binärversionen der Tablet PC-Bibliothek beschrieben.

## <a name="tablet-pc-library-versions"></a>Versionen der Tablet PC-Bibliothek

Die Binärdateien der Tablet PC-Bibliothek (Microsoft.Ink.dll) wurden in Windows Vista aktualisiert. Diese Binärdateien werden als "Version 6.0" bezeichnet, um mit der Version von Windows zusammenzufassen, in der sie veröffentlicht werden.

Das neueste Release der Binärdateien, die mit Windows XP kompatibel sind, wird als "Version 1.7" bezeichnet.

Das Windows SDK kann auf Vista- und XP-Computern installiert werden, und das Windows SDK enthält beide Versionen von Microsoft.Ink.dll.

Diese werden in installiert:

1. %programfiles% \\ Reference Assemblies Microsoft Tablet PC \\ \\ \\ v1.7 \\Microsoft.Ink.dll

2. %programfiles% \\ Verweisassemblys \\ Microsoft Tablet PC \\ \\ v6.0 \\Microsoft.Ink.dll

Die Binärdateien der Version 6.0 sind nur mit Windows Vista kompatibel, und anwendungen, die für sie geschrieben wurden, sollten immer nur auf Windows Vista ausgeführt werden.

Eine Anwendung, die für die Binärdateien der Version 1.7 geschrieben wurde, sollte ohne Änderungen ausgeführt werden, wenn sie auf Windows Vista installiert ist.

 

 



