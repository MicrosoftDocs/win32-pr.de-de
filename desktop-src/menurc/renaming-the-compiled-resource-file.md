---
title: Umbenennen der kompilierten Ressourcen Datei
description: Bei der Ressourcen Kompilierung benennt RC die kompilierte Ressourcen Datei (. res) standardmäßig mit dem Basis Namen der RC-Datei und platziert Sie im gleichen Verzeichnis wie die RC-Datei.
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c54e22cff753dbc59cbce61cd71874c8fe77a85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206314"
---
# <a name="renaming-the-compiled-resource-file"></a>Umbenennen der kompilierten Ressourcen Datei

Bei der Ressourcen Kompilierung benennt RC die kompilierte Ressourcen Datei (. res) standardmäßig mit dem Basis Namen der RC-Datei und platziert Sie im gleichen Verzeichnis wie die RC-Datei. CVTRES muss dann aufgerufen werden, um die res-Datei in ein binäres Ressourcen Format (. RBJ) zu konvertieren, das vom Linker interpretiert werden kann. Im folgenden Beispiel wird "MyApp. RC" kompiliert und eine kompilierte Ressourcen Datei mit dem Namen "MyApp. res" im selben Verzeichnis wie "MyApp. RC" erstellt:

**RC MyApp. RC**

Die **/FO** -Option gibt der resultierenden res-Datei einen Namen, der sich vom Namen der entsprechenden RC-Datei unterscheidet. Verwenden Sie z. b. den folgenden Befehl, um die resultierende res-Datei "newFile. res" zu benennen:

**RC-FO newFile. res MyApp. RC**

Die **/FO** -Option kann die res-Datei auch in einem anderen Verzeichnis platzieren. Beispielsweise wird mit dem folgenden Befehl die kompilierte Ressourcen Datei "MyApp. res" in das Verzeichnis "C: Source" eingefügt \\ \\ :

**RC-FO c: \\ Quell \\ Ressource \\ myapp. res MyApp. RC**

 

 




