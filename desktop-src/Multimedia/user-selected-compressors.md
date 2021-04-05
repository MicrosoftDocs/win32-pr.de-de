---
title: User-Selected-Kompressoren
description: User-Selected-Kompressoren
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- Videokomprimierungs-Manager (VCM), vom Benutzer ausgewählte Kompressoren
- VCM (Videokomprimierungs-Manager), vom Benutzer ausgewählte Kompressoren
- Iccompressorchoose-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbba48b919265ea6e0bab2c3d891f628c4e660a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947879"
---
# <a name="user-selected-compressors"></a><span data-ttu-id="0f7bb-106">User-Selected-Kompressoren</span><span class="sxs-lookup"><span data-stu-id="0f7bb-106">User-Selected Compressors</span></span>

<span data-ttu-id="0f7bb-107">Wenn Sie Daten komprimieren, kann die Anwendung die [**iccompressorchoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) -Funktion verwenden, um ein Dialogfeld zu erstellen, in dem der Benutzer den Kompressor auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-107">When compressing data, your application can use the [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) function to create a dialog box in which the user can select the compressor.</span></span> <span data-ttu-id="0f7bb-108">Sie können Flags für diese Funktion angeben, um dem Benutzer die Angabe der Keyframe-Frequenz und der Movie-Data-Rate oder das Anzeigen eines Vorschau Fensters zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-108">You can specify flags for this function to allow the user to specify the key-frame frequency and the movie-data rate, or to display a preview window.</span></span>

<span data-ttu-id="0f7bb-109">Der vom Benutzer ausgewählte Kompressor wird automatisch geöffnet, und das zugehörige Handle wird im hussiemember der in **iccompressorchoose** angegebenen [**compvars**](/windows/desktop/api/Vfw/ns-vfw-compvars) -Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-109">The compressor selected by the user is automatically opened and its handle is returned in the hic member of the [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) structure specified in **ICCompressorChoose**.</span></span>

<span data-ttu-id="0f7bb-110">Wenn Sie **iccompressorchoose** verwenden, verwenden Sie die [**iccompressorfree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) -Funktion, um den-Kompressor zu schließen und alle Ressourcen freizugeben, die der **compvars** -Struktur zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0f7bb-110">If you use **ICCompressorChoose**, use the [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) function to close the compressor and free any resources associated with the **COMPVARS** structure.</span></span>

 

 




