---
description: Kurvenpfade
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Kurvenpfade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b58018b7ef95b30c5ae2751ed963caefee7b9313ca86a8c6a2a4fee246908f8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849180"
---
# <a name="curved-paths"></a>Kurvenpfade

Eine Anwendung kann die Kurven in einem Pfad durch Aufrufen der [**FlattenPath-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) abflachen. Diese Funktion ist besonders nützlich für Anwendungen, die Text in die Kontur eines Pfads einfügen, der Kurven enthält. Um den Text anzupassen, muss die Anwendung die folgenden Schritte ausführen:

1.  Erstellen Sie den Pfad, in dem der Text angezeigt wird.
2.  Rufen Sie die [**FlattenPath-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) auf, um die Kurven in einem Pfad in Liniensegmente zu konvertieren.
3.  Rufen Sie die [**GetPath-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) auf, um diese Zeilensegmente abzurufen.
4.  Berechnen Sie die Länge jeder Zeile und die Breite jedes Zeichens in der Zeichenfolge.
5.  Verwenden Sie Daten zur Linienbreite und zur Zeichenbreite, um jedes Zeichen entlang der Kurve zu positionieren.

 

 



