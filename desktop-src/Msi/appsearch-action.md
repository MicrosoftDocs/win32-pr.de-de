---
description: Die AppSearch-Aktion verwendet Datei Signaturen, um nach vorhandenen Versionen von Produkten zu suchen.
ms.assetid: 56665876-2c74-476b-aa1a-158c6e86418d
title: AppSearch-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04187fb146af80839e135c99986dea1902ccb6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215718"
---
# <a name="appsearch-action"></a><span data-ttu-id="43788-103">AppSearch-Aktion</span><span class="sxs-lookup"><span data-stu-id="43788-103">AppSearch Action</span></span>

<span data-ttu-id="43788-104">Die AppSearch-Aktion verwendet Datei Signaturen, um nach vorhandenen Versionen von Produkten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="43788-104">The AppSearch action uses file signatures to search for existing versions of products.</span></span> <span data-ttu-id="43788-105">Mithilfe der AppSearch-Aktion können Sie ermitteln, wo Upgrades installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="43788-105">The AppSearch action may use this information to determine where upgrades are to be installed.</span></span> <span data-ttu-id="43788-106">Die AppSearch-Aktion kann auch verwendet werden, um eine Eigenschaft auf den vorhandenen Wert eines Registrierungs-oder INI-Datei Eintrags festzulegen.</span><span class="sxs-lookup"><span data-stu-id="43788-106">The AppSearch action can also be used to set a property to the existing value of an registry or .ini file entry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="43788-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="43788-107">Sequence Restrictions</span></span>

<span data-ttu-id="43788-108">AppSearch sollte in der Tabelle [InstallUISequence](installuisequence-table.md) und der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="43788-108">AppSearch should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="43788-109">Das Installationsprogramm verhindert, dass die AppSearch-Aktion in der InstallExecuteSequence-Sequenz ausgeführt wird, wenn die Aktion bereits in der InstallUISequence-Sequenz ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="43788-109">The installer prevents the AppSearch action from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="43788-110">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="43788-110">ActionData Messages</span></span>



| <span data-ttu-id="43788-111">Feld</span><span class="sxs-lookup"><span data-stu-id="43788-111">Field</span></span> | <span data-ttu-id="43788-112">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="43788-112">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="43788-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="43788-113">\[1\]</span></span> | <span data-ttu-id="43788-114">Eigenschaft, die den Datei Speicherort enthält</span><span class="sxs-lookup"><span data-stu-id="43788-114">Property holding file location.</span></span> |
| <span data-ttu-id="43788-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="43788-115">\[2\]</span></span> | <span data-ttu-id="43788-116">Datei Signatur.</span><span class="sxs-lookup"><span data-stu-id="43788-116">File signature.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="43788-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43788-117">Remarks</span></span>

<span data-ttu-id="43788-118">Die Aktion AppSearch erfordert, dass die [Signatur](signature-table.md) Tabelle im Installationspaket vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="43788-118">The AppSearch action requires that the [Signature](signature-table.md) table be present in the installation package.</span></span> <span data-ttu-id="43788-119">Datei Signaturen werden in der Signatur Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="43788-119">File signatures are listed in the Signature table.</span></span> <span data-ttu-id="43788-120">Eine Signatur, die nicht in der Signatur Tabelle ist, gibt ein Verzeichnis an, und die-Eigenschaft legt die-Eigenschaft auf den Verzeichnispfad für diese Signatur fest.</span><span class="sxs-lookup"><span data-stu-id="43788-120">A signature that is not in the Signature table denotes a directory and the action sets the property to the directory path for that signature.</span></span>

<span data-ttu-id="43788-121">Die AppSearch-Aktion sucht zunächst mithilfe der Tabelle " [complocator](complocator-table.md) ", der Tabelle " [reglocator](reglocator-table.md) ", der Tabelle " [inilocator](inilocator-table.md) " und schließlich der Tabelle " [drlocator](drlocator-table.md) " nach Datei Signaturen.</span><span class="sxs-lookup"><span data-stu-id="43788-121">The AppSearch action searches for file signatures using the [CompLocator](complocator-table.md) table first, the [RegLocator](reglocator-table.md) table next, then the [IniLocator](inilocator-table.md) table, and finally the [DrLocator](drlocator-table.md) table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43788-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43788-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43788-123">AppSearch</span><span class="sxs-lookup"><span data-stu-id="43788-123">AppSearch</span></span>](appsearch-table.md)
</dt> <dt>

[<span data-ttu-id="43788-124">Complocator</span><span class="sxs-lookup"><span data-stu-id="43788-124">CompLocator</span></span>](complocator-table.md)
</dt> <dt>

[<span data-ttu-id="43788-125">Inilocator</span><span class="sxs-lookup"><span data-stu-id="43788-125">IniLocator</span></span>](inilocator-table.md)
</dt> <dt>

[<span data-ttu-id="43788-126">Reglocator</span><span class="sxs-lookup"><span data-stu-id="43788-126">RegLocator</span></span>](reglocator-table.md)
</dt> <dt>

[<span data-ttu-id="43788-127">Drlocator</span><span class="sxs-lookup"><span data-stu-id="43788-127">DrLocator</span></span>](drlocator-table.md)
</dt> </dl>

 

 



