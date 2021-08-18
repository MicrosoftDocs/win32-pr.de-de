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
ms.openlocfilehash: 3b7577639bd215fc051c2f1303e74fe946341a31c4b6708f881c3c9fabae2372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557777"
---
# <a name="include"></a>"#include"
/* Title: MyMof.Mof                           */ /*   Title: MyMof2.Mof */

Der \# Befehl include preprocessor schließt den Inhalt einer MOF-Datei in eine andere MOF-Datei ein. Im folgenden Codebeispiel wird die Syntax für den \# Includebefehl beschrieben.

``` syntax
#include ("Moffile.mof")
```

Im vorherigen Beispiel ist Moffile.mof der Name der mof-Datei, die enthalten sein soll.

Das folgende Beispiel zeigt zwei MOF-Dateien. Wenn Sie die erste MOF-Datei kompilieren, kompiliert der Compiler automatisch die zweite MOF-Datei (Mymof2.mof) an dem Speicherort, an dem Sie die \# include-Anweisung platzieren.

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

Die folgende MOF-Datei ist im vorherigen Beispiel enthalten:

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

 

 



