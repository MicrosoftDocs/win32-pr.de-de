---
description: Zeitstempel werden normalerweise eingeschlossen, wenn eine Datei mithilfe von SignTool mit der Option-t signiert wird.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Hinzufügen von Zeitstempeln zu zuvor signierten Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e750dcb178b2a089bfbde0b2aea882b097c86
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106367338"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a><span data-ttu-id="71bbd-103">Hinzufügen von Zeitstempeln zu zuvor signierten Dateien</span><span class="sxs-lookup"><span data-stu-id="71bbd-103">Adding Time Stamps to Previously Signed Files</span></span>

<span data-ttu-id="71bbd-104">Zeitstempel werden normalerweise eingeschlossen, wenn eine Datei mithilfe von SignTool mit der Option **-t** signiert wird.</span><span class="sxs-lookup"><span data-stu-id="71bbd-104">Time stamps are normally included when a file is signed using SignTool with the **-t** option.</span></span> <span data-ttu-id="71bbd-105">Außerdem können Zeitstempel zu Dateien hinzugefügt werden, die ohne einen Zeitstempel signiert wurden.</span><span class="sxs-lookup"><span data-stu-id="71bbd-105">In addition, time stamps can be added to files that were signed without a time stamp.</span></span> <span data-ttu-id="71bbd-106">Mit dem folgenden Befehl wird einer zuvor signierten Datei ein Zeitstempel hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="71bbd-106">The following command adds a time stamp to a previously signed file:</span></span>

<span data-ttu-id="71bbd-107">**SignTool Zeitstempel-t https: \/ /timestamp.Digicert.com *MyControl.exe***</span><span class="sxs-lookup"><span data-stu-id="71bbd-107">**signtool timestamp -t https:\//timestamp.digicert.com *MyControl.exe***</span></span>

> [!Note]  
> <span data-ttu-id="71bbd-108">Die Datei, die mit einem Zeitstempel versehen werden soll, muss bereits signiert sein.</span><span class="sxs-lookup"><span data-stu-id="71bbd-108">The file to be time stamped must have previously been signed.</span></span>

 

<span data-ttu-id="71bbd-109">Weitere Informationen zu SignTool finden Sie unter [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="71bbd-109">For more information about SignTool, see [SignTool](signtool.md).</span></span>

 

 



