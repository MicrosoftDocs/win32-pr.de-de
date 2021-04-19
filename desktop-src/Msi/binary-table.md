---
description: Die binäre Tabelle enthält die Binärdaten für Elemente wie z. b. Bitmaps, Animationen und Symbole. Die binäre Tabelle wird auch zum Speichern von Daten für benutzerdefinierte Aktionen verwendet. Siehe OLE-Einschränkungen für Datenströme.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Binäre Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4069c7e684e7d90c94b4b04f3d5839058f3570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349166"
---
# <a name="binary-table"></a><span data-ttu-id="dbed9-105">Binäre Tabelle</span><span class="sxs-lookup"><span data-stu-id="dbed9-105">Binary Table</span></span>

<span data-ttu-id="dbed9-106">Die binäre Tabelle enthält die Binärdaten für Elemente wie z. b. Bitmaps, Animationen und Symbole.</span><span class="sxs-lookup"><span data-stu-id="dbed9-106">The Binary table holds the binary data for items such as bitmaps, animations, and icons.</span></span> <span data-ttu-id="dbed9-107">Die binäre Tabelle wird auch zum Speichern von Daten für benutzerdefinierte Aktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="dbed9-107">The binary table is also used to store data for custom actions.</span></span> <span data-ttu-id="dbed9-108">Siehe [OLE-Einschränkungen für Datenströme](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="dbed9-108">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

<span data-ttu-id="dbed9-109">Die binäre Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="dbed9-109">The Binary table has the following columns.</span></span>



| <span data-ttu-id="dbed9-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="dbed9-110">Column</span></span> | <span data-ttu-id="dbed9-111">Typ</span><span class="sxs-lookup"><span data-stu-id="dbed9-111">Type</span></span>                         | <span data-ttu-id="dbed9-112">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="dbed9-112">Key</span></span> | <span data-ttu-id="dbed9-113">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="dbed9-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="dbed9-114">Name</span><span class="sxs-lookup"><span data-stu-id="dbed9-114">Name</span></span>   | [<span data-ttu-id="dbed9-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="dbed9-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="dbed9-116">J</span><span class="sxs-lookup"><span data-stu-id="dbed9-116">Y</span></span>   | <span data-ttu-id="dbed9-117">N</span><span class="sxs-lookup"><span data-stu-id="dbed9-117">N</span></span>        |
| <span data-ttu-id="dbed9-118">Daten</span><span class="sxs-lookup"><span data-stu-id="dbed9-118">Data</span></span>   | [<span data-ttu-id="dbed9-119">Binär (Binary)</span><span class="sxs-lookup"><span data-stu-id="dbed9-119">Binary</span></span>](binary.md)         | <span data-ttu-id="dbed9-120">N</span><span class="sxs-lookup"><span data-stu-id="dbed9-120">N</span></span>   | <span data-ttu-id="dbed9-121">N</span><span class="sxs-lookup"><span data-stu-id="dbed9-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="dbed9-122">Spalten</span><span class="sxs-lookup"><span data-stu-id="dbed9-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="dbed9-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="dbed9-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="dbed9-124">Ein eindeutiger Schlüssel, der die jeweiligen Binärdaten identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dbed9-124">A unique key that identifies the particular binary data.</span></span> <span data-ttu-id="dbed9-125">Wenn die Binärdaten für ein Steuerelement vorgesehen sind, wird der Schlüssel in der Text-Spalte des zugeordneten Steuer Elements in der [Steuerelement Tabelle](control-table.md)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dbed9-125">If the binary data is for a control, the key appears in the Text column of the associated control in the [Control table](control-table.md).</span></span> <span data-ttu-id="dbed9-126">Dieser Schlüssel muss für alle Steuerelemente, die Binärdaten erfordern, eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="dbed9-126">This key must be unique among all controls requiring binary data.</span></span>

</dd> <dt>

<span data-ttu-id="dbed9-127"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Vorrats</span><span class="sxs-lookup"><span data-stu-id="dbed9-127"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="dbed9-128">Die unformatierten Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="dbed9-128">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="dbed9-129">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="dbed9-129">Validation</span></span>

<dl>

[<span data-ttu-id="dbed9-130">ICE03</span><span class="sxs-lookup"><span data-stu-id="dbed9-130">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="dbed9-131">ICE06</span><span class="sxs-lookup"><span data-stu-id="dbed9-131">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="dbed9-132">ICE17</span><span class="sxs-lookup"><span data-stu-id="dbed9-132">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="dbed9-133">ICE29</span><span class="sxs-lookup"><span data-stu-id="dbed9-133">ICE29</span></span>](ice29.md)  
</dl>

 

 



