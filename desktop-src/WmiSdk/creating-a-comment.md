---
description: Der Managed Object Format(MOF)-Compiler unterstützt zwei Kommentarstile mit zwei verschiedenen Stilen von Kommentartrennzeichen.
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
ms.openlocfilehash: 870833f1dbb86f53c7114c4e376af2b4882906ffe1b8cc10f5876bd2c80492e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097340"
---
# <a name="creating-a-comment"></a>Erstellen eines Kommentars

Der Managed Object Format(MOF)-Compiler unterstützt zwei Kommentarstile mit zwei verschiedenen Stilen von Kommentartrennzeichen.

In der folgenden Tabelle sind die Trennzeichen aufgeführt, die für Kommentare verwendet werden, und die Auswirkungen, die die Trennzeichen im Code haben.



| Trennzeichen   | Markierungen                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | Beginn eines Kommentars, der am Ende der Zeile endet.                                    |
| /\* Und \*/ | Anfang und Ende eines Kommentars, der mehrere Zeilen oder nur einen Teil einer Zeile umfassen kann. |



 

Wie in den Programmiersprachen C und C++ müssen Sie das /-Trennzeichen nur mit Einzeilenkommentaren verwenden, aber die Trennzeichen /und / mit ein- oder mehrzeilenigen \* \* Kommentaren.

Im folgenden Codebeispiel werden die beiden Trennzeichenstile beschrieben.

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen Managed Object Format -Klassen (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



