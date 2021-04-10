---
title: Die STGMEDIUM-Struktur
description: Die STGMEDIUM-Struktur
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86faf52ab93bab39b8413ea2eb6381da24b643b5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "104039824"
---
# <a name="the-stgmedium-structure"></a><span data-ttu-id="700d9-103">Die STGMEDIUM-Struktur</span><span class="sxs-lookup"><span data-stu-id="700d9-103">The STGMEDIUM Structure</span></span>

<span data-ttu-id="700d9-104">Ebenso wie die [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur eine Erweiterung des Windows-Zwischenablage-Format Bezeichners ist, ist die [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur eine Verbesserung des globalen Speicher Handles, das zum Übertragen der Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="700d9-104">Just as the [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) structure is an enhancement of the Windows clipboard format identifier, so the [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure is an improvement of the global memory handle used to transfer the data.</span></span> <span data-ttu-id="700d9-105">Die **STGMEDIUM** -Struktur schließt den Member, **TYMED**, ein, der das zu verwendende Medium angibt, und eine Union, die Zeiger und ein Handle für die Angabe des Mediums angibt, das in **TYMED** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="700d9-105">The **STGMEDIUM** structure includes a member, **tymed**, which indicates the medium to be used, and a union comprising pointers and a handle for getting whichever medium is specified in **tymed**.</span></span>

<span data-ttu-id="700d9-106">Die [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur ermöglicht es Datenquellen und Consumern, das effizienteste Exchange-Medium auf renderbasis auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="700d9-106">The [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure enables both data sources and consumers to choose the most efficient exchange medium on a per-rendering basis.</span></span> <span data-ttu-id="700d9-107">Wenn die Daten so umfangreich sind, dass Sie auf dem Datenträger aufbewahrt werden sollen, kann die Datenquelle ein Datenträger basiertes Medium in seinem bevorzugten Format angeben und nur globalen Speicher als eine Sicherung verwenden, wenn dies das einzige Medium ist, das der Consumer versteht.</span><span class="sxs-lookup"><span data-stu-id="700d9-107">If the data is so large that it should be kept on disk, the data source can indicate a disk-based medium in its preferred format, only using global memory as a backup if that's the only medium the consumer understands.</span></span> <span data-ttu-id="700d9-108">Wenn Sie das beste Medium für Austausch Vorgänge als Standard verwenden können, wird die Gesamtleistung des Datenaustauschs zwischen Anwendungen verbessert.</span><span class="sxs-lookup"><span data-stu-id="700d9-108">Being able to use the best medium for exchanges as the default improves overall performance of data exchange between applications.</span></span> <span data-ttu-id="700d9-109">Wenn z. b. einige der zu übertragenden Daten bereits auf dem Datenträger vorhanden sind, kann die Quell Anwendung Sie verschieben oder in ein neues Ziel kopieren, entweder in der gleichen Anwendung oder in anderen, ohne dass die Daten zuerst in den globalen Speicher geladen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="700d9-109">For example, if some of the data to be transferred is already on disk, the source application can move or copy it to a new destination, either in the same application or in some other, without having first to load the data into global memory.</span></span> <span data-ttu-id="700d9-110">Am empfangenden Ende muss der Consumer der Daten nicht auf den Datenträger zurückgeschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="700d9-110">At the receiving end, the consumer of the data does not have to write it back to disk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="700d9-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="700d9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="700d9-112">Datenformate und Übertragungsmedien</span><span class="sxs-lookup"><span data-stu-id="700d9-112">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




