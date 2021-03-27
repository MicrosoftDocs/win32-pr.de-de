---
description: Gekrümmte Pfade
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Gekrümmte Pfade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe27e20d7c5c3f59ea4bd38b46049088ae9d409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863675"
---
# <a name="curved-paths"></a>Gekrümmte Pfade

Eine Anwendung kann die Kurven in einem Pfad vereinfachen, indem Sie die Funktion "vereinfachender [**Pfad**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) " aufrufen. Diese Funktion ist besonders nützlich für Anwendungen, die Text in die Kontur eines Pfades einfügen, der Kurven enthält. Die Anwendung muss die folgenden Schritte ausführen, damit Sie in den Text passt:

1.  Erstellen Sie den Pfad, in dem der Text angezeigt wird.
2.  Greifen Sie auf die Funktion "vereinfachte [**path**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) " zu, um die Kurven in einem Pfad in Liniensegmente zu konvertieren.
3.  Rufen Sie die [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) -Funktion auf, um diese Liniensegmente abzurufen.
4.  Berechnen Sie die Länge der einzelnen Zeilen und die Breite jedes Zeichens in der Zeichenfolge.
5.  Verwenden Sie Daten der Zeilenbreite und der Zeichenbreite, um die einzelnen Zeichen entlang der Kurve zu positionieren.

 

 



