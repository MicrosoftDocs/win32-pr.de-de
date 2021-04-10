---
title: Format Bezeichner/Offset-paar
description: Der zweite Teil des Eigenschaften Satz-Streams enthält ein Format Bezeichner/Offset-Paar.
ms.assetid: cc3a748d-e81c-45da-b04f-ea986158a4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f80a85175278b92fedbfd7b2d50d94007b7e4a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309811"
---
# <a name="format-identifieroffset-pair"></a>Format Bezeichner/Offset-paar

Der zweite Teil des Eigenschaften Satz-Streams enthält ein Format Bezeichner/Offset-Paar. Die fmtid ist der Name der Eigenschaften Gruppe. Es identifiziert eindeutig, wie der Inhalt des folgenden Abschnitts interpretiert werden kann. Der Offset ist die Entfernung in Bytes vom Beginn des gesamten Streams bis zum Beginn des Abschnitts.

Die folgende Struktur ist hilfreich bei der Verarbeitung von Format Bezeichnern/Offset-Paaren.

``` syntax
typedef struct tagFORMATIDOFFSET 
{ 
    FMTID  fmtid ;     // Name of the section. 
    DWORD  dwOffset ;  // Offset for the section. 
} FORMATIDOFFSET;
```

 

 




