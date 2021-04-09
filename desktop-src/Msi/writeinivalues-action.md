---
description: Mit der Aktion "Write-einivalues" werden die Informationen der INI-Datei, die von der Anwendung benötigt werden, in die INI-Dateien geschrieben.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: Aktion "Write-einivalues"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd96e86c361c7fe83b6ad33959149e82fb9d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866048"
---
# <a name="writeinivalues-action"></a><span data-ttu-id="bdf77-103">Aktion "Write-einivalues"</span><span class="sxs-lookup"><span data-stu-id="bdf77-103">WriteIniValues Action</span></span>

<span data-ttu-id="bdf77-104">Mit der Aktion "Write-einivalues" werden die Informationen der INI-Datei, die von der Anwendung benötigt werden, in die INI-Dateien geschrieben.</span><span class="sxs-lookup"><span data-stu-id="bdf77-104">The WriteIniValues action writes the .ini file information that the application needs written to its .ini files.</span></span> <span data-ttu-id="bdf77-105">Das Schreiben dieser Informationen wird von der [Komponenten Tabelle](component-table.md)abgegrenzt.</span><span class="sxs-lookup"><span data-stu-id="bdf77-105">The writing of this information is gated by the [Component table](component-table.md).</span></span> <span data-ttu-id="bdf77-106">Ein INI-Wert wird geschrieben, wenn die entsprechende Komponente so festgelegt wurde, dass Sie entweder lokal oder über die Quelle ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bdf77-106">An .ini value is written if the corresponding component has been set to be installed either locally or run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="bdf77-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="bdf77-107">Sequence Restrictions</span></span>

<span data-ttu-id="bdf77-108">Die InstallValidate-Aktion muss vor der Aktion "Write-einivalues" erfolgen.</span><span class="sxs-lookup"><span data-stu-id="bdf77-108">The InstallValidate action must come before the WriteIniValues action.</span></span> <span data-ttu-id="bdf77-109">Wenn eine [RemoveIniValues-Aktion](removeinivalues-action.md) in der Sequenz vorhanden ist, muss Sie vor der Aktion "Write" geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bdf77-109">If there is a [RemoveIniValues action](removeinivalues-action.md) in the sequence, then it must come before the WriteIniValues action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="bdf77-110">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="bdf77-110">ActionData Messages</span></span>



| <span data-ttu-id="bdf77-111">Feld</span><span class="sxs-lookup"><span data-stu-id="bdf77-111">Field</span></span> | <span data-ttu-id="bdf77-112">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="bdf77-112">Description of action data</span></span>              |
|-------|-----------------------------------------|
| <span data-ttu-id="bdf77-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="bdf77-113">\[1\]</span></span> | <span data-ttu-id="bdf77-114">Bezeichner der INI-Datei.</span><span class="sxs-lookup"><span data-stu-id="bdf77-114">Identifier of .ini file.</span></span>                |
| <span data-ttu-id="bdf77-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="bdf77-115">\[2\]</span></span> | <span data-ttu-id="bdf77-116">INI-Datei Schlüssel im folgenden Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="bdf77-116">.ini file key in the following section.</span></span> |
| <span data-ttu-id="bdf77-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="bdf77-117">\[3\]</span></span> | <span data-ttu-id="bdf77-118">Das Element wurde aus der INI-Datei entfernt.</span><span class="sxs-lookup"><span data-stu-id="bdf77-118">Item removed from .ini file.</span></span>            |
| <span data-ttu-id="bdf77-119">\[4\]</span><span class="sxs-lookup"><span data-stu-id="bdf77-119">\[4\]</span></span> | <span data-ttu-id="bdf77-120">Der Wert wurde aus der INI-Datei entfernt.</span><span class="sxs-lookup"><span data-stu-id="bdf77-120">Value removed from .ini file.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="bdf77-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bdf77-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdf77-122">INIFILE-Tabelle</span><span class="sxs-lookup"><span data-stu-id="bdf77-122">IniFile table</span></span>](inifile-table.md)
</dt> </dl>

 

 



