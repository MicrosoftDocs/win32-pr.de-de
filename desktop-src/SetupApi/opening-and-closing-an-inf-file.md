---
description: Bevor die Setup Funktionen auf Informationen in der INF zugreifen können, müssen Sie Sie mit einem Aufrufen der setupopeninffile-Funktion öffnen. Diese Funktion gibt ein Handle für die INF-Datei zurück.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Öffnen und Schließen einer INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893b72d000f433fb4da7ecfee0db4d856f878814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529324"
---
# <a name="opening-and-closing-an-inf-file"></a><span data-ttu-id="1bdd7-104">Öffnen und Schließen einer INF-Datei</span><span class="sxs-lookup"><span data-stu-id="1bdd7-104">Opening and Closing an INF file</span></span>

<span data-ttu-id="1bdd7-105">Bevor die Setup Funktionen auf Informationen in der INF zugreifen können, müssen Sie Sie mit einem Aufrufen der [**setupopeninffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) -Funktion öffnen.</span><span class="sxs-lookup"><span data-stu-id="1bdd7-105">Before the setup functions can access information in the INF, you must open it with a call to the [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) function.</span></span> <span data-ttu-id="1bdd7-106">Diese Funktion gibt ein Handle für die INF-Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="1bdd7-106">This function returns a handle to the INF file.</span></span>

<span data-ttu-id="1bdd7-107">Wenn Sie den Namen der INF-Datei, die Sie öffnen müssen, nicht kennen, können Sie die [**setupgetinffilelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) -Funktion verwenden, um eine Liste der INF-Dateien in einem Verzeichnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1bdd7-107">If you do not know the name of the INF file that you need to open, you can use the [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) function to obtain a list of INF files in a directory.</span></span>

<span data-ttu-id="1bdd7-108">Nachdem Sie eine INF-Datei geöffnet haben, können Sie zusätzliche INF-Dateien an die geöffnete INF-Datei anfügen, indem Sie die [**setupopenappendinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="1bdd7-108">After you open an INF file, you can append additional INF files to the opened INF file by using the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function.</span></span> <span data-ttu-id="1bdd7-109">Dies ist funktionell vergleichbar mit einer include-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="1bdd7-109">This is functionally similar to an include statement.</span></span> <span data-ttu-id="1bdd7-110">Wenn nachfolgende Setup Funktionen auf eine geöffnete INF-Datei verweisen, können Sie auch auf alle in den angefügten Dateien gespeicherten Informationen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="1bdd7-110">When subsequent setup functions reference an open INF file, they will also be able to access any information stored in the appended files.</span></span>

<span data-ttu-id="1bdd7-111">Wenn Sie beim Aufrufen der [**setupopenappendinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) -Funktion keine INF-Datei angeben, fügt **setupopenappendinffile** die Dateien, die vom **Layoutfile** -Schlüssel angegeben werden, im Abschnitt **Version** der geöffneten INF-Datei an.</span><span class="sxs-lookup"><span data-stu-id="1bdd7-111">If you do not specify an INF file during the call to the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function, **SetupOpenAppendInfFile** appends the file(s) specified by the **LayoutFile** key in the **Version** section of the open INF file.</span></span>

<span data-ttu-id="1bdd7-112">Wenn Sie die Informationen in der INF-Datei nicht mehr benötigen, rufen Sie die [**setupcloseinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) -Funktion auf, um die während des Aufrufes [**setupopenappendinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)zugeordneten Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="1bdd7-112">When you no longer need the information in the INF file, call the [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) function to release resources allocated during the call to [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).</span></span>

 

 



