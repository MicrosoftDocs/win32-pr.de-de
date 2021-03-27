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
# <a name="curved-paths"></a><span data-ttu-id="b75a2-103">Gekrümmte Pfade</span><span class="sxs-lookup"><span data-stu-id="b75a2-103">Curved Paths</span></span>

<span data-ttu-id="b75a2-104">Eine Anwendung kann die Kurven in einem Pfad vereinfachen, indem Sie die Funktion "vereinfachender [**Pfad**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b75a2-104">An application can flatten the curves in a path by calling the [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) function.</span></span> <span data-ttu-id="b75a2-105">Diese Funktion ist besonders nützlich für Anwendungen, die Text in die Kontur eines Pfades einfügen, der Kurven enthält.</span><span class="sxs-lookup"><span data-stu-id="b75a2-105">This function is especially useful for applications that fit text onto the contour of a path which contains curves.</span></span> <span data-ttu-id="b75a2-106">Die Anwendung muss die folgenden Schritte ausführen, damit Sie in den Text passt:</span><span class="sxs-lookup"><span data-stu-id="b75a2-106">To fit the text, the application must perform the following steps:</span></span>

1.  <span data-ttu-id="b75a2-107">Erstellen Sie den Pfad, in dem der Text angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b75a2-107">Create the path where the text appears.</span></span>
2.  <span data-ttu-id="b75a2-108">Greifen Sie auf die Funktion "vereinfachte [**path**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) " zu, um die Kurven in einem Pfad in Liniensegmente zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="b75a2-108">Call the [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) function to convert the curves in a path into line segments.</span></span>
3.  <span data-ttu-id="b75a2-109">Rufen Sie die [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) -Funktion auf, um diese Liniensegmente abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b75a2-109">Call the [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) function to retrieve those line segments.</span></span>
4.  <span data-ttu-id="b75a2-110">Berechnen Sie die Länge der einzelnen Zeilen und die Breite jedes Zeichens in der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b75a2-110">Calculate the length of each line and the width of each character in the string.</span></span>
5.  <span data-ttu-id="b75a2-111">Verwenden Sie Daten der Zeilenbreite und der Zeichenbreite, um die einzelnen Zeichen entlang der Kurve zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="b75a2-111">Use line-width and character-width data to position each character along the curve.</span></span>

 

 



