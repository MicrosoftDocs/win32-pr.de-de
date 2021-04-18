---
description: Der Installer legt Eigenschaften mit der folgenden Rangfolge fest. Ein Eigenschafts Wert in dieser Liste kann einen Wert, der darauf folgt, außer Kraft setzen und durch einen Wert überschrieben werden, der in der Liste vor ihm liegt.
ms.assetid: ba9240fe-2e5a-43f5-8cdf-59dd6348092b
title: Reihenfolge der Eigenschafts Rangfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c114594b9a825a3847db37f5b98dc990211d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366300"
---
# <a name="order-of-property-precedence"></a><span data-ttu-id="08be0-104">Reihenfolge der Eigenschafts Rangfolge</span><span class="sxs-lookup"><span data-stu-id="08be0-104">Order of Property Precedence</span></span>

<span data-ttu-id="08be0-105">Der Installer legt Eigenschaften mit der folgenden Rangfolge fest.</span><span class="sxs-lookup"><span data-stu-id="08be0-105">The installer sets properties using the following order of precedence.</span></span> <span data-ttu-id="08be0-106">Ein Eigenschafts Wert in dieser Liste kann einen Wert, der darauf folgt, außer Kraft setzen und durch einen Wert überschrieben werden, der in der Liste vor ihm liegt.</span><span class="sxs-lookup"><span data-stu-id="08be0-106">A property value in this list can override a value that comes after it and be overridden by a value coming before it in the list.</span></span>

1.  <span data-ttu-id="08be0-107">Eigenschaften, die von der Betriebsumgebung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="08be0-107">Properties specified by the operating environment.</span></span>
2.  <span data-ttu-id="08be0-108">[Öffentliche Eigenschaften](public-properties.md) , die in der Befehlszeile festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="08be0-108">[Public properties](public-properties.md) set on the command line.</span></span>
3.  <span data-ttu-id="08be0-109">Öffentliche Eigenschaften, die während einer [administrativen Installation](administrative-installation.md) durch das [**Eigenschaftenset adminproperties**](adminproperties.md) aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="08be0-109">Public properties listed by the [**AdminProperties**](adminproperties.md) propertyset during an [administrative installation](administrative-installation.md) .</span></span>
4.  <span data-ttu-id="08be0-110">Öffentliche oder private Eigenschaften, die während der Anwendung einer [*Transformation*](t-gly.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="08be0-110">Public or private properties set during the application of a [*transform*](t-gly.md).</span></span>
5.  <span data-ttu-id="08be0-111">Eine öffentliche oder private Eigenschaft, die durch das Erstellen der [Eigenschaften Tabelle](property-table.md) der MSI-Datei festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="08be0-111">Public or private property that set by authoring the [Property table](property-table.md) of the .msi file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08be0-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08be0-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08be0-113">Informationen zu Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08be0-113">About Properties</span></span>](about-properties.md)
</dt> </dl>

 

 



