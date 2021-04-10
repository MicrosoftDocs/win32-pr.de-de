---
description: Die BindImage-Tabelle enthält Informationen zu jeder ausführbaren Datei oder dll, die an die von ihr importierten DLLs gebunden werden muss.
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: BindImage-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47b97efc8886d7748d0426a49ed76567810939c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959502"
---
# <a name="bindimage-table"></a><span data-ttu-id="c201a-103">BindImage-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c201a-103">BindImage Table</span></span>

<span data-ttu-id="c201a-104">Die BindImage-Tabelle enthält Informationen zu jeder ausführbaren Datei oder dll, die an die von ihr importierten DLLs gebunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="c201a-104">The BindImage table contains information about each executable or DLL that needs to be bound to the DLLs imported by it.</span></span>

<span data-ttu-id="c201a-105">Die BindImage-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="c201a-105">The BindImage table has the following columns.</span></span>



| <span data-ttu-id="c201a-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="c201a-106">Column</span></span> | <span data-ttu-id="c201a-107">Typ</span><span class="sxs-lookup"><span data-stu-id="c201a-107">Type</span></span>                         | <span data-ttu-id="c201a-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c201a-108">Key</span></span> | <span data-ttu-id="c201a-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="c201a-109">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="c201a-110">Datei\_</span><span class="sxs-lookup"><span data-stu-id="c201a-110">File\_</span></span> | [<span data-ttu-id="c201a-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="c201a-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="c201a-112">J</span><span class="sxs-lookup"><span data-stu-id="c201a-112">Y</span></span>   | <span data-ttu-id="c201a-113">N</span><span class="sxs-lookup"><span data-stu-id="c201a-113">N</span></span>        |
| <span data-ttu-id="c201a-114">Pfad</span><span class="sxs-lookup"><span data-stu-id="c201a-114">Path</span></span>   | [<span data-ttu-id="c201a-115">Paths</span><span class="sxs-lookup"><span data-stu-id="c201a-115">Paths</span></span>](paths.md)           | <span data-ttu-id="c201a-116">N</span><span class="sxs-lookup"><span data-stu-id="c201a-116">N</span></span>   | <span data-ttu-id="c201a-117">J</span><span class="sxs-lookup"><span data-stu-id="c201a-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c201a-118">Spalten</span><span class="sxs-lookup"><span data-stu-id="c201a-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c201a-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_</span><span class="sxs-lookup"><span data-stu-id="c201a-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="c201a-120">Ein externer Schlüssel für die Spalte einer der [Datei Tabellen](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="c201a-120">An external key to column one of the [File table](file-table.md).</span></span> <span data-ttu-id="c201a-121">Dabei muss es sich um eine ausführbare Datei oder eine DLL-Datei handeln.</span><span class="sxs-lookup"><span data-stu-id="c201a-121">This must be an executable file or a DLL file.</span></span>

</dd> <dt>

<span data-ttu-id="c201a-122"><span id="Path"></span><span id="path"></span><span id="PATH"></span>ADS</span><span class="sxs-lookup"><span data-stu-id="c201a-122"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Path</span></span>
</dt> <dd>

<span data-ttu-id="c201a-123">Eine durch Semikolons getrennte Liste von Pfaden, die die Pfade darstellen, die durchsucht werden sollen, um die importierten DLLs zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c201a-123">A list of paths, separated by semicolons, that represent the paths to be searched to find the imported DLLs.</span></span> <span data-ttu-id="c201a-124">Die Liste ist normalerweise eine Liste von Eigenschaften, wobei jede Eigenschaft in eckige Klammern () eingeschlossen ist \[ \] .</span><span class="sxs-lookup"><span data-stu-id="c201a-124">The list is usually a list of properties, with each property enclosed inside square brackets (\[ \]) .</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c201a-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c201a-125">Remarks</span></span>

<span data-ttu-id="c201a-126">Das Installationsprogramm berechnet die virtuelle Adresse der einzelnen Funktionen, die aus allen DLLs importiert werden, und die berechnete virtuelle Adresse wird dann in der Import Adress Tabelle (IAT) des importierten Images gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c201a-126">The installer computes the virtual address of each function that is imported from all DLLs, and the computed virtual address is then saved in the importing image's Import Address Table (IAT).</span></span>

<span data-ttu-id="c201a-127">Diese Tabelle wird beim Ausführen der [BindImage-Aktion](bindimage-action.md) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c201a-127">This table is referred to when the [BindImage action](bindimage-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="c201a-128">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="c201a-128">Validation</span></span>

<dl>

[<span data-ttu-id="c201a-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="c201a-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c201a-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="c201a-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c201a-131">ICE32</span><span class="sxs-lookup"><span data-stu-id="c201a-131">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="c201a-132">ICE46</span><span class="sxs-lookup"><span data-stu-id="c201a-132">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="c201a-133">ICE76</span><span class="sxs-lookup"><span data-stu-id="c201a-133">ICE76</span></span>](ice76.md)  
</dl>

 

 



