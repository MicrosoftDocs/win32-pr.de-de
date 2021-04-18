---
description: Ein Alias in WMI ist ein symbolischer Verweis in einer Klasse oder einer Klasseninstanz an einer anderen Stelle in einer Managed Object Format Datei (MOF).
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: Erstellen eines WMI-Alias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdd538e113f227eac4980855ea0035e839b92fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343819"
---
# <a name="creating-a-wmi-alias"></a>Erstellen eines WMI-Alias

Ein [*Alias*](gloss-a.md) in WMI ist ein symbolischer Verweis in einer Klasse oder einer Klasseninstanz an einer anderen Stelle in einer Managed Object Format Datei (MOF). Der MOF-Compiler verwendet Aliase, um Verweise zwischen Klassen und Instanzen herzustellen. Der Compiler löst Aliase zu den Klassen auf, auf die Sie verweisen, sodass Aliasnamen im kompilierten Code nicht verfügbar sind. Daher können Client Anwendungen nicht auf Klassen verweisen, die Aliase verwenden.

> [!Note]  
> WMI unterstützt Forward-Verweise, aber keine zirkulären Aliase.

 

Ein Alias weist nur den Gültigkeitsbereich innerhalb der MOF-Datei auf, in der Sie den Alias deklarieren. Daher verwenden Sie in der Regel einen Alias als Verknüpfung zu einem langen Objekt Pfad.

**So definieren Sie einen Alias**

1.  Fügen Sie der-Instanz oder-Klassen Deklaration den Ausdruck "as $*Aliasname*" hinzu.
2.  Aliasnamen folgen denselben Regeln wie Instanznamen und Klassennamen, mit dem Unterschied, dass Aliasnamen mit einem Dollarzeichen ($) beginnen müssen. Unterstriche können in einem Aliasnamen nach dem ersten Zeichen angezeigt werden.

Im folgenden Codebeispiel wird beschrieben, wie ein Alias in einer Klassendefinition verwendet wird.

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

In den folgenden Codebeispielen wird beschrieben, wie ein Alias als symbolischer Verweis auf einen Objekt Pfad verwendet wird. In diesen Beispielen werden zwei Klassen deklariert, um einen Datenträger zu beschreiben: die Disk-Klasse zum Angeben des Laufwerk Buchstabens und die DiskRef-Klasse, um den Datenträger Pfad anzugeben. Ein Alias ist für die Datenträger Klasseninstanz definiert. Dieser Alias wird als Wert für die Eigenschaft pathto Disk in der DiskRef-Instanz verwendet.

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

 

 



