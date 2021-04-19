---
description: Windows verwendet einen Dateizeiger, um die gelesenen oder geschriebenen Bytes nachzuverfolgen.
ms.assetid: 21c75d96-0357-422d-b12b-74c56f64ecf1
title: Positionieren eines Dateizeigers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6588a3d65e71c2180c4e9753e65cd94ed070d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353472"
---
# <a name="positioning-a-file-pointer"></a>Positionieren eines Dateizeigers

Wenn eine Anwendung "up [**File**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " aufruft, um eine Datei zum ersten Mal zu öffnen, platziert Windows den [Dateizeiger](file-pointers.md) am Anfang der Datei. Wenn Bytes aus der Datei gelesen oder in diese geschrieben werden, verschiebt Windows den Dateizeiger um die Anzahl der gelesenen oder geschriebenen Bytes.

Eine Anwendung kann den Dateizeiger auf einen angegebenen Offset positionieren, indem [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer)aufgerufen wird.

Die [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) -Funktion kann auch verwendet werden, um die aktuelle Dateizeiger Position abzufragen, indem Sie eine Verschiebungs Methode der **\_ aktuellen Datei** und einen Abstand von 0 (null) angibt.

 

 



