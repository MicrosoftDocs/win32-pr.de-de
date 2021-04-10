---
description: Die RemoveIniValues-Aktion entfernt die zum Entfernen angegebenen ini-Dateiinformationen in der removeinifile-Tabelle, wenn die Komponente für die lokale Installation oder die Ausführung aus der Quelle festgelegt ist.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: RemoveIniValues-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dfb847d911e847de00ede6eab30ac3a86615eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960757"
---
# <a name="removeinivalues-action"></a><span data-ttu-id="5a031-103">RemoveIniValues-Aktion</span><span class="sxs-lookup"><span data-stu-id="5a031-103">RemoveIniValues Action</span></span>

<span data-ttu-id="5a031-104">Die RemoveIniValues-Aktion entfernt die zum Entfernen angegebenen ini-Dateiinformationen in der [removeinifile-Tabelle](removeinifile-table.md) , wenn die Komponente für die lokale Installation oder die Ausführung aus der Quelle festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5a031-104">The RemoveIniValues action removes .ini file information specified for removal in the [RemoveIniFile table](removeinifile-table.md) if the component is set to be installed locally or run-from-source.</span></span> <span data-ttu-id="5a031-105">Die RemoveIniValues-Aktion entfernt ini-Dateiinformationen, die einer Komponente in der Tabelle " [IniFile](inifile-table.md)" zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="5a031-105">The RemoveIniValues action removes .ini file information that has been associated with a component in the [IniFile table](inifile-table.md).</span></span> <span data-ttu-id="5a031-106">Mit dieser Aktion werden auch ini-Dateiinformationen entfernt, wenn die Informationen von der [Aktion "Write-einivalues](writeinivalues-action.md) " geschrieben und die Komponente deinstalliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a031-106">This action also removes .ini file information if the information was written by the [WriteIniValues action](writeinivalues-action.md) and the component is scheduled to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="5a031-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="5a031-107">Sequence Restrictions</span></span>

<span data-ttu-id="5a031-108">Die [InstallValidate](installvalidate-action.md) -Aktion muss vor der RemoveIniValues-Aktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5a031-108">The [InstallValidate](installvalidate-action.md) action must be called before the RemoveIniValues action.</span></span> <span data-ttu-id="5a031-109">Wenn eine " [Write](writeinivalues-action.md) "-Aktion in der Sequenz verwendet wird, muss Sie nach "RemoveIniValues" angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5a031-109">If a [WriteIniValues](writeinivalues-action.md) action is used in the sequence, it must appear after RemoveIniValues.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="5a031-110">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="5a031-110">ActionData Messages</span></span>



| <span data-ttu-id="5a031-111">Feld</span><span class="sxs-lookup"><span data-stu-id="5a031-111">Field</span></span> | <span data-ttu-id="5a031-112">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="5a031-112">Description of action data</span></span>    |
|-------|-------------------------------|
| <span data-ttu-id="5a031-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="5a031-113">\[1\]</span></span> | <span data-ttu-id="5a031-114">Bezeichner der INI-Datei.</span><span class="sxs-lookup"><span data-stu-id="5a031-114">Identifier of .ini file.</span></span>      |
| <span data-ttu-id="5a031-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="5a031-115">\[2\]</span></span> | <span data-ttu-id="5a031-116">Der Schlüssel Abschnitt der INI-Datei.</span><span class="sxs-lookup"><span data-stu-id="5a031-116">An .ini file key section.</span></span>     |
| <span data-ttu-id="5a031-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="5a031-117">\[3\]</span></span> | <span data-ttu-id="5a031-118">Das Element wurde aus der INI-Datei entfernt.</span><span class="sxs-lookup"><span data-stu-id="5a031-118">Item removed from .ini file.</span></span>  |
| <span data-ttu-id="5a031-119">\[4\]</span><span class="sxs-lookup"><span data-stu-id="5a031-119">\[4\]</span></span> | <span data-ttu-id="5a031-120">Der Wert wurde aus der INI-Datei entfernt.</span><span class="sxs-lookup"><span data-stu-id="5a031-120">Value removed from .ini file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5a031-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5a031-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a031-122">Removeinifile-Tabelle</span><span class="sxs-lookup"><span data-stu-id="5a031-122">RemoveIniFile table</span></span>](removeinifile-table.md)
</dt> <dt>

[<span data-ttu-id="5a031-123">INIFILE-Tabelle</span><span class="sxs-lookup"><span data-stu-id="5a031-123">IniFile table</span></span>](inifile-table.md)
</dt> <dt>

[<span data-ttu-id="5a031-124">Aktion "Write-einivalues"</span><span class="sxs-lookup"><span data-stu-id="5a031-124">WriteIniValues action</span></span>](writeinivalues-action.md)
</dt> <dt>

[<span data-ttu-id="5a031-125">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="5a031-125">InstallValidate</span></span>](installvalidate-action.md)
</dt> </dl>

 

 



