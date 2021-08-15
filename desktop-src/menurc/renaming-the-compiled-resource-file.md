---
title: Umbenennen der kompilierten Ressourcendatei
description: Standardmäßig benennt RC beim Kompilieren von Ressourcen die kompilierte Ressourcendatei (RES) mit dem Basisnamen der RC-Datei und platziert sie im gleichen Verzeichnis wie die RC-Datei.
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60f2a920eeed6c1b96b512511b965b0243b89e4f6888120c6183b7a3104963c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733517"
---
# <a name="renaming-the-compiled-resource-file"></a>Umbenennen der kompilierten Ressourcendatei

Standardmäßig benennt RC beim Kompilieren von Ressourcen die kompilierte Ressourcendatei (RES) mit dem Basisnamen der RC-Datei und platziert sie im gleichen Verzeichnis wie die RC-Datei. CVTRES muss dann aufgerufen werden, um die RES-Datei in ein binäres Ressourcenformat (.rbj) zu konvertieren, das vom Linker verstanden werden kann. Im folgenden Beispiel wird MyApp.rc kompiliert und eine kompilierte Ressourcendatei namens MyApp.res im gleichen Verzeichnis wie MyApp.rc erstellt:

**rc myapp.rc**

Die **Option /fo** gibt der resultierenden RES-Datei einen Namen, der sich vom Namen der entsprechenden RC-Datei unterscheidet. Um beispielsweise die resultierende RES-Datei NewFile.res zu benennen, verwenden Sie den folgenden Befehl:

**rc -fo newfile.res myapp.rc**

Mit **der Option /fo** kann die RES-Datei auch in einem anderen Verzeichnis gespeichert werden. Beispielsweise platziert der folgende Befehl die kompilierte Ressourcendatei MyApp.res im Verzeichnis C: \\ \\ Quellressource:

**rc -fo c: \\ \\ \\ Quellressource myapp.res myapp.rc**

 

 




