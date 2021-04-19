---
description: Eine Anwendung kann eine Datei durch Aufrufen von SetEndOfFile abschneiden oder erweitern.
ms.assetid: 23a0242d-50e9-4324-bb09-505afe383a80
title: Abschneiden oder Erweitern von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf8a2d4e7e346bfea41285be97d6d756e2a6b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363675"
---
# <a name="truncating-or-extending-files"></a>Abschneiden oder Erweitern von Dateien

Eine Anwendung kann eine Datei durch Aufrufen von [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)abschneiden oder erweitern. Diese Funktion legt die Markierung für das Ende der Datei auf die aktuelle Position des Dateizeigers fest.

Beachten Sie Folgendes: Wenn eine Datei erweitert wird, werden die Inhalte zwischen dem alten und dem neuen Speicherort der Datei Ende nicht definiert.

 

 



