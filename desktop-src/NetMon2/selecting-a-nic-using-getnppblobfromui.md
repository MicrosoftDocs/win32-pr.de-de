---
description: Bei Netzwerkmonitor ist die programmgesteuerte Auswahl einer NIC ein zweistufiger Prozess. Erstellen Sie zunächst das Filterblob, indem Sie die CreateBlob-Methode aufrufen. Wählen Sie dann die NIC aus, indem Sie die GetNPPBlobFromUI-Methode aufrufen.
ms.assetid: 0556b20a-307e-4bc3-a986-cfee96a8655d
title: Auswählen einer NIC mit GetNPPBlobFromUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3bd02ef5085bba511fb0d05844840eb92d85ef83c67f244ab321570fae4ad8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128900"
---
# <a name="selecting-a-nic-using-getnppblobfromui"></a>Auswählen einer NIC mit GetNPPBlobFromUI

Bei Netzwerkmonitor ist die programmgesteuerte Auswahl einer NIC ein zweistufiger Prozess. Erstellen Sie zunächst das Filterblob, indem Sie die [**CreateBlob-Methode**](createblob.md) aufrufen. Wählen Sie dann die NIC aus, indem Sie die [**GetNPPBlobFromUI-Methode**](getnppblobfromui.md) aufrufen.

In diesem Beispiel wird ein Filterblob verwendet, um die erforderliche NIC auszuwählen:


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



 

 



