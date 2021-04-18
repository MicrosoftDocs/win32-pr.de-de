---
description: Bei Netzwerkmonitor ist das programmgesteuerte Auswählen einer NIC ein zweistufiger Prozess. Erstellen Sie zuerst das filterblob, indem Sie die createBlob-Methode aufrufen. Wählen Sie dann die NIC aus, indem Sie die getnppblobfromui-Methode aufrufen.
ms.assetid: 0556b20a-307e-4bc3-a986-cfee96a8655d
title: Auswählen einer NIC mithilfe von getnppblobfromui
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb429a87d284a5a6a03a20357728c8bbcb5acac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347801"
---
# <a name="selecting-a-nic-using-getnppblobfromui"></a><span data-ttu-id="f23c5-105">Auswählen einer NIC mithilfe von getnppblobfromui</span><span class="sxs-lookup"><span data-stu-id="f23c5-105">Selecting a NIC Using GetNPPBlobFromUI</span></span>

<span data-ttu-id="f23c5-106">Bei Netzwerkmonitor ist das programmgesteuerte Auswählen einer NIC ein zweistufiger Prozess.</span><span class="sxs-lookup"><span data-stu-id="f23c5-106">With Network Monitor, selecting a NIC programmatically is a two-step process.</span></span> <span data-ttu-id="f23c5-107">Erstellen Sie zuerst das filterblob, indem Sie die [**createBlob**](createblob.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f23c5-107">First, create the filter BLOB by calling the [**CreateBlob**](createblob.md) method.</span></span> <span data-ttu-id="f23c5-108">Wählen Sie dann die NIC aus, indem Sie die [**getnppblobfromui**](getnppblobfromui.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f23c5-108">Then, select the NIC by calling the [**GetNPPBlobFromUI**](getnppblobfromui.md) method.</span></span>

<span data-ttu-id="f23c5-109">In diesem Beispiel wird ein filterblob verwendet, um die erforderliche NIC auszuwählen:</span><span class="sxs-lookup"><span data-stu-id="f23c5-109">In this example a filter BLOB is used to select the required NIC:</span></span>


```C++
DWORD rc;

// Call CreateBlob to create a filter blob.
///////////////////////////////////////////
HBLOB hFilterBlob;
rc = CreateBlob(&hFilterBlob);
if (FAILED (rc));
{
  // Failed creating filter BLOB. Add appropriate error handling.
}


// Call GetNPPBlobFromUI to retrieve the NPP Blob.
//////////////////////////////////////////////////
rc = GetNPPBlobFromUI(hwnd,
                      hFilterBlob,
                      &hBlob);
if (FAILED (rc));
{
  // Failed retrieving NPP BLOB. Add appropriate error handling.
}
```



 

 



