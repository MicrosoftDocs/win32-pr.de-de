---
description: Der Installer speichert alle Informationen über die Benutzeroberfläche in den Tabellen der-Installations Datenbank.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Anzeigen der Vorschau der Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c58f30dcd797064ef9b01217927fda96a758f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216357"
---
# <a name="previewing-the-user-interface"></a><span data-ttu-id="fab36-103">Anzeigen der Vorschau der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="fab36-103">Previewing the User Interface</span></span>

<span data-ttu-id="fab36-104">Der Installer speichert alle Informationen über die [Benutzeroberfläche](user-interface.md) in den Tabellen der-Installations Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fab36-104">The installer stores all information about the [user interface](user-interface.md) in the tables of the installation database.</span></span> <span data-ttu-id="fab36-105">Um das Design der Benutzeroberfläche zu vereinfachen, bietet das Installationsprogramm außerdem einen Vorschaumodus zum Anzeigen dieser Informationen.</span><span class="sxs-lookup"><span data-stu-id="fab36-105">To facilitate the design of the UI the installer also provides a preview mode for viewing this information.</span></span> <span data-ttu-id="fab36-106">Im folgenden Verfahren wird beschrieben, wie Sie den UI-Vorschaumodus aktivieren und die aktuelle Darstellung von Dialogfeldern und Bildschirm anzeigen.</span><span class="sxs-lookup"><span data-stu-id="fab36-106">The following procedure describes how to enable the UI preview mode and display the current appearance of dialog boxes and billboards.</span></span>

<span data-ttu-id="fab36-107">**So zeigen Sie die Benutzeroberfläche im Vorschaumodus an**</span><span class="sxs-lookup"><span data-stu-id="fab36-107">**To view the user interface in the preview mode**</span></span>

1.  <span data-ttu-id="fab36-108">Aktivieren Sie den Vorschaumodus, indem Sie die [**msienableuipreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fab36-108">Enable the preview mode by calling the [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) function.</span></span>
2.  <span data-ttu-id="fab36-109">Zeigen Sie die einzelnen Dialogfelder an, indem Sie die [**msipreviewdialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fab36-109">Display the particular dialog boxes by calling the [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) function.</span></span>
3.  <span data-ttu-id="fab36-110">Zeigen Sie bestimmte Billboards an, indem Sie die [**msipreviewbillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fab36-110">Display particular billboards by calling the [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) function.</span></span>

 

 



