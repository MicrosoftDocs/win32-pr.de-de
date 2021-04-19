---
description: Schließt den Inhalt einer MOF-Datei in eine andere MOF-Datei ein.
ms.assetid: 06765956-e4ee-467b-9b3b-d5da17b9cd82
ms.tgt_platform: multiple
title: '#include'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5eb3d203cff5bca7e5096082cca7ba531580ae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362679"
---
# <a name="include"></a>"#include"
/* Title: mymof. MOF                           *//*   Title: MyMof2. MOF */

Der \# Befehl include Präprozessor enthält den Inhalt einer MOF-Datei in eine andere MOF-Datei. Im folgenden Codebeispiel wird die Syntax für den \# include-Befehl beschrieben.

``` syntax
#include ("Moffile.mof")
```

Im vorherigen Beispiel ist "muffile. mof" der Name der MOF-Datei, die eingeschlossen werden soll.

Das folgende Beispiel zeigt zwei MOF-Dateien. Wenn Sie die erste MOF-Datei kompilieren, kompiliert der Compiler automatisch die zweite MOF-Datei (Mymof2. MOF) an dem Speicherort, an dem Sie die \# include-Anweisung platzieren.

``` syntax
/*   Title: MyMof.Mof                           */
/*                                              */ 
/*   This MOF file shows how to include  */
/*   an MOF file in another MOF file             */

#pragma namespace("\\\\.\\root")            

#include ("mymof2.mof")

class myclass1 
{
    [key] string Description;
};


instance of myclass1
{
    Description = "Description of myclass1";
};
/*   End of MyMof.Mof                           */
```

Das vorherige Beispiel enthält die folgende MOF-Datei:

``` syntax
/*   Title: MyMof2.Mof                               */
/*                                                   */
/*   This MOF is included when MyMof.MOF is compiled */

class myclass2 
{
    [key] string Description;
};


instance of myclass2
{
    Description = "Description of myclass2";
    
};
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 



