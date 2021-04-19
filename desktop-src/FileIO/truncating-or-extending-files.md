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
# <a name="truncating-or-extending-files"></a><span data-ttu-id="9dff0-103">Abschneiden oder Erweitern von Dateien</span><span class="sxs-lookup"><span data-stu-id="9dff0-103">Truncating or Extending Files</span></span>

<span data-ttu-id="9dff0-104">Eine Anwendung kann eine Datei durch Aufrufen von [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)abschneiden oder erweitern.</span><span class="sxs-lookup"><span data-stu-id="9dff0-104">An application can truncate or extend a file by calling [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span></span> <span data-ttu-id="9dff0-105">Diese Funktion legt die Markierung für das Ende der Datei auf die aktuelle Position des Dateizeigers fest.</span><span class="sxs-lookup"><span data-stu-id="9dff0-105">This function sets the end-of-file marker to the current position of the file pointer.</span></span>

<span data-ttu-id="9dff0-106">Beachten Sie Folgendes: Wenn eine Datei erweitert wird, werden die Inhalte zwischen dem alten und dem neuen Speicherort der Datei Ende nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="9dff0-106">Note that when a file is extended, the contents between the old and new end-of-file locations are not defined.</span></span>

 

 



