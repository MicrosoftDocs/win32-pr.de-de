---
description: Ein Alias in WMI ist ein symbolischer Verweis in einer Klasse oder einer Klasseninstanz, die sich an anderer Stelle in einer MOF-Datei (Managed Object Format) befindet.
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: Erstellen eines WMI-Alias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a4709cba6ba1fa1790c80ac8d8f52f5fa2105207f0094ec3168f62ba0fcc43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925621"
---
# <a name="creating-a-wmi-alias"></a>Erstellen eines WMI-Alias

Ein [*Alias*](gloss-a.md) in WMI ist ein symbolischer Verweis in einer Klasse oder einer Klasseninstanz, die sich an anderer Stelle in einer MOF-Datei (Managed Object Format) befindet. Der MOF-Compiler verwendet Aliase, um Verweise zwischen Klassen und Instanzen herzustellen. Der Compiler löst Aliase in die Klassen auf, auf die sie verweisen, sodass Aliasnamen im kompilierten Code nicht verfügbar sind. Daher können Clientanwendungen nicht auf Klassen verweisen, die Aliase verwenden.

> [!Note]  
> WMI unterstützt Vorwärtsverweisen, aber keine zirkulären Aliase.

 

Ein Alias hat nur einen Bereich innerhalb der MOF-Datei, in der Sie den Alias deklarieren. Daher verwenden Sie in der Regel einen Alias als Verknüpfung mit einem langen Objektpfad.

**So definieren Sie einen Alias**

1.  Fügen Sie der Instanz- oder Klassendeklaration den Ausdruck "as $*aliasname"* hinzu.
2.  Aliasnamen folgen den gleichen Regeln wie Instanz- und Klassennamen, außer dass Aliasnamen mit einem Dollarzeichen ($) beginnen müssen. Unterstriche können in einem Aliasnamen nach dem Anfangszeichen angezeigt werden.

Im folgenden Codebeispiel wird beschrieben, wie ein Alias in einer Klassendefinition verwendet wird.

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

In den folgenden Codebeispielen wird beschrieben, wie ein Alias als symbolischer Verweis auf einen Objektpfad verwendet wird. In diesen Beispielen werden zwei Klassen deklariert, um einen Datenträger zu beschreiben: die Disk-Klasse zum Angeben des Laufwerkbuchstabens und die DiskRef-Klasse zum Angeben des Datenträgerpfads. Ein Alias wird für die Disk-Klasseninstanz definiert. Dieser Alias wird als Wert für die PathToDisk-Eigenschaft in der DiskRef-Instanz verwendet.

``` syntax
class Disk {
    [key]  string    DriveLetter;
};

class DiskRef 
{
    [key]  string    MyKey;
    Disk   ref       PathToDisk;
};

instance of Disk as $DiskAlias 
{
    DriveLetter = "c";
};

instance of DiskRef
{
    MyKey      =  "hello";
    PathToDisk = $DiskAlias;
};
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Klasse](creating-a-class.md)
</dt> </dl>

 

 



