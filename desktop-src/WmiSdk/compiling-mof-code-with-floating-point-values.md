---
description: Der MOF-Compiler akzeptiert einen Gleit Komma Wert, der für eine nicht-Gleit Komma Eigenschaft angegeben ist. Der Wert wird aufgerundet und als nicht Gleit Komma Zahl gespeichert. Diese Situation kann zu unerwarteten Ergebnissen führen.
ms.assetid: 5cf7d8e1-c29d-4b9f-8557-e656c5e83370
ms.tgt_platform: multiple
title: Kompilieren von MOF-Code mit Floating-Point Werten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734639e1038b8e9739fead694740dbf5ab5f9cc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217129"
---
# <a name="compiling-mof-code-with-floating-point-values"></a>Kompilieren von MOF-Code mit Floating-Point Werten

Der MOF-Compiler akzeptiert einen Gleit Komma Wert, der für eine nicht-Gleit Komma Eigenschaft angegeben ist. Der Wert wird aufgerundet und als nicht Gleit Komma Zahl gespeichert. Diese Situation kann zu unerwarteten Ergebnissen führen.

Im folgenden MOF-Codebeispiel wird eine Klasse namens **ABC** in einem Namespace mit dem Namen "Test" definiert. Dieser MOF-Code wird ohne Fehler kompiliert, Sie können jedoch keine Abfrage für den Gleit Komma Wert durchführt, der für die Eigenschaft **exampleUint16** in der von diesem Code erstellten-Instanz definiert ist.

``` syntax
#pragma namespace ("\\\\.\\Root")

instance of __Namespace
{
    Name = "Test";
};

#pragma namespace ("\\\\.\\Root\\test")

Class abc
{
        [KEY] String testID ;
        Uint16 exampleUint16;
        Real64 exampleReal64;
};

Instance of abc
{ 
        TestID ="exampleID";
        exampleUint16 = 1000.4;
};
```

Wenn Sie die folgende Abfrage ausgeben, erhalten Sie einen Fehlercode, der auf eine ungültige Abfrage hinweist.


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000.4
```



Die folgende Abfrage findet jedoch die festgestellte Instanz.


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompilieren von MOF-Dateien](compiling-mof-files.md)
</dt> <dt>

[**Mofcomp**](mofcomp.md)
</dt> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 



