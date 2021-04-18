---
title: IBackgroundCopyCallback3-Methoden
description: Die IBackgroundCopyCallback3-Schnittstelle stellt die folgenden Methoden zur Verfügung.
ms.assetid: FF0BA13F-63DA-46A4-ACC6-DE72AC20EAA2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f13aa1c97006084007e747f2766868c25e5b998
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337966"
---
# <a name="ibackgroundcopycallback3-methods"></a><span data-ttu-id="44de6-103">IBackgroundCopyCallback3-Methoden</span><span class="sxs-lookup"><span data-stu-id="44de6-103">IBackgroundCopyCallback3 Methods</span></span>

<span data-ttu-id="44de6-104">Die [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) -Schnittstelle stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="44de6-104">The [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="44de6-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="44de6-105">In this section</span></span>



| <span data-ttu-id="44de6-106">Thema</span><span class="sxs-lookup"><span data-stu-id="44de6-106">Topic</span></span>                                                                                             | <span data-ttu-id="44de6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44de6-107">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44de6-108">**Filerangestransferred-Methode**</span><span class="sxs-lookup"><span data-stu-id="44de6-108">**FileRangesTransferred method**</span></span>](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopycallback3-filerangestransferred)<br/> | <span data-ttu-id="44de6-109">Bits ruft Ihre Implementierung der [**filerangestransferred**](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopycallback3-filerangestransferred) -Methode auf, wenn ein oder mehrere Datei Bereiche heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="44de6-109">BITS calls your implementation of the [**FileRangesTransferred**](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopycallback3-filerangestransferred) method when one or more file ranges have been downloaded.</span></span> <span data-ttu-id="44de6-110">Datei Bereiche werden mithilfe der [**IBackgroundCopyFile6:: requestfileranges**](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopyfile6-requestfileranges) -Methode dem Auftrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="44de6-110">File ranges are added to the job using the [**IBackgroundCopyFile6::RequestFileRanges**](/windows/desktop/api/Bits10_1/nf-bits10_1-ibackgroundcopyfile6-requestfileranges) method.</span></span><br/> |



 

 

 





