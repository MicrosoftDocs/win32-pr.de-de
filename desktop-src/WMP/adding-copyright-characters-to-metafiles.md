---
title: Hinzufügen von Copyright Zeichen zu Metafiles
description: Die Zeichen für Copyright-und Marken Registrierungs Symbole (\ 169; oder \ 174;) werden möglicherweise nicht ordnungsgemäß angezeigt, wenn die Metadatei nicht mit dem UTF-8-Codierungsschema codiert ist.
ms.assetid: 9124c8d4-1fc1-4163-ada9-d96af58f8b98
keywords:
- Hinzufügen von Copyright Zeichen zu Metafiles-Windows-Media Player
topic_type:
- apiref
api_name:
- Adding Copyright Characters to Metafiles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e71b116a3500fdb4217613c81bd4f041af75a66
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312504"
---
# <a name="adding-copyright-characters-to-metafiles"></a><span data-ttu-id="e6205-104">Hinzufügen von Copyright Zeichen zu Metafiles</span><span class="sxs-lookup"><span data-stu-id="e6205-104">Adding Copyright Characters to Metafiles</span></span>

<span data-ttu-id="e6205-105">Die Zeichen für Copyright-und Marken Registrierungs Symbole (© oder®) werden möglicherweise nicht ordnungsgemäß angezeigt, wenn die Metadatei nicht mit dem UTF-8-Codierungsschema codiert ist.</span><span class="sxs-lookup"><span data-stu-id="e6205-105">The characters for copyright and trademark registration symbols ( © or ® ) may not display correctly if the metafile is not encoded using the UTF-8 encoding scheme.</span></span> <span data-ttu-id="e6205-106">In diesem Fall können Sie die ASCII-Entsprechungen (c) und (r) im **Copyright** -Element verwenden, wie im folgenden Code gezeigt, um eines dieser Symbole für alle Benutzer ordnungsgemäß anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e6205-106">In this case, to display either of these symbols properly for all users, you can use the ASCII equivalents (c) and (r) inside the **COPYRIGHT** element, as shown in the following code.</span></span>


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



<span data-ttu-id="e6205-107">Wenn die Metadatendatei mit UTF-8 codiert wird, werden Copyright-und Marken Symbole ordnungsgemäß angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6205-107">If the metafile is encoded using UTF-8, copyright and trademark symbols will display correctly.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6205-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6205-108">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6205-109">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="e6205-109">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




