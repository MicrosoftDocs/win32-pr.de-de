---
description: Der MOF-Compiler (Managed Object Format) unterstützt zwei Arten von Kommentaren unter Verwendung zweier verschiedener Arten von Kommentar Trennzeichen.
ms.assetid: 5ab71b45-7ed1-44c4-8710-6b833b0afb80
ms.tgt_platform: multiple
title: Erstellen eines Kommentars
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d0e7cf2484fef018c62c8c47d9c55d245191681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368241"
---
# <a name="creating-a-comment"></a>Erstellen eines Kommentars

Der MOF-Compiler (Managed Object Format) unterstützt zwei Arten von Kommentaren unter Verwendung zweier verschiedener Arten von Kommentar Trennzeichen.

In der folgenden Tabelle werden die Trennzeichen aufgelistet, die für Kommentare verwendet werden, und die Auswirkungen, die die Trennzeichen im Code aufweisen.



| Trennzeichen   | Markierungen                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | Beginn eines Kommentars, der am Ende der Zeile endet.                                    |
| /\* immer \*/ | Anfang und Ende eines Kommentars, der sich möglicherweise über mehrere Zeilen erstreckt oder nur einen Teil einer Zeile umfasst. |



 

Wie in den Programmiersprachen C und C++ muss das//-Trennzeichen nur mit einzeiligen Kommentaren verwendet werden. dabei werden die/ \* und \* /-Trennzeichen entweder mit einzeiligen oder mehrzeiligen Kommentaren verwendet.

Im folgenden Codebeispiel werden die beiden Trennzeichen Stile beschrieben.

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



