---
description: Sie müssen die setupopeninffile-Funktion verwenden, um die INF-Datei zu öffnen, bevor Sie Informationen aus ihr abrufen oder andere INF-Dateien an Sie anfügen können.
ms.assetid: ba4d511a-ad19-4619-a10a-cafef789821b
title: Öffnen der INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8493fda983f2942705b97ea243f6cb95e91c15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865719"
---
# <a name="opening-the-inf-file"></a>Öffnen der INF-Datei

Sie müssen die [**setupopeninffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) -Funktion verwenden, um die INF-Datei zu öffnen, bevor Sie Informationen aus ihr abrufen oder andere INF-Dateien an Sie anfügen können.

Im folgenden wird eine INF-Datei mithilfe von [**setupopeninffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) geöffnet, und es wird ein Handle, myinf, an die geöffnete INF-Datei zurückgegeben. Der *infclass* -Parameter von **setupopeininffile** ist als **null** angegeben, um anzugeben, dass die Klasse der INF-Datei ignoriert werden soll.


```C++
HINF MyInf;                //variable to hold the INF handle
UINT ErrorLine;            //variable to hold errors returned
BOOL test=0;                 //variable to receive function success
 
MyInf = SetupOpenInfFile (
      szInfFileName,       //the filename of the inf file to open
      NULL,                //optional class information
      INF_STYLE_WIN4,      //the inf style
      &ErrorLine           //line number of the syntax error
);
```



Nachdem eine INF-Datei geöffnet wurde, können Sie die Funktion [**setupopenappendinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) aufrufen, um der geöffneten INF-Datei eine Datei anzufügen. Wiederholen Sie diesen Vorgang, um mehrere Dateien anzufügen. Wenn Sie die Funktion **setupopenappendinffile** aufrufen und der an Sie weiter gegebene Dateiname **null** ist, durchsucht die Funktion den Abschnitt Version der geöffneten INF-Datei (und alle angefügten INF-Dateien) nach einem Layoutfile-Schlüssel. Wenn die Funktion einen Schlüssel findet, wird die durch diesen Schlüssel angegebene Datei (normalerweise Layout) angefügt. Inf). Wenn mehrere INF-Dateien kombiniert wurden, wird **setupopeinappendinffile** bei der Suche nach einem Versions Abschnitt mit der letzten angefügten INF-Datei gestartet.

 

 



