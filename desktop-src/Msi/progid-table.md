---
description: Die ProgID-Tabelle enthält Informationen zu Programm-IDs und Versions unabhängigen Programm-IDs, die als Teil der Produktankündigung generiert werden müssen.
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: ProgID-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293ce3748f691b664d55b0a1158a574472388202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960758"
---
# <a name="progid-table"></a><span data-ttu-id="72b1c-103">ProgID-Tabelle</span><span class="sxs-lookup"><span data-stu-id="72b1c-103">ProgId Table</span></span>

<span data-ttu-id="72b1c-104">Die ProgID-Tabelle enthält Informationen zu Programm-IDs und Versions unabhängigen Programm-IDs, die als Teil der Produktankündigung generiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="72b1c-104">The ProgId table contains information for program IDs and version independent program IDs that must be generated as a part of the product advertisement.</span></span>

<span data-ttu-id="72b1c-105">Die ProgID-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="72b1c-105">The ProgId table has the following columns.</span></span>



| <span data-ttu-id="72b1c-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="72b1c-106">Column</span></span>         | <span data-ttu-id="72b1c-107">Typ</span><span class="sxs-lookup"><span data-stu-id="72b1c-107">Type</span></span>                         | <span data-ttu-id="72b1c-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="72b1c-108">Key</span></span> | <span data-ttu-id="72b1c-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="72b1c-109">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="72b1c-110">ProgId</span><span class="sxs-lookup"><span data-stu-id="72b1c-110">ProgId</span></span>         | [<span data-ttu-id="72b1c-111">Text</span><span class="sxs-lookup"><span data-stu-id="72b1c-111">Text</span></span>](text.md)             | <span data-ttu-id="72b1c-112">J</span><span class="sxs-lookup"><span data-stu-id="72b1c-112">Y</span></span>   | <span data-ttu-id="72b1c-113">N</span><span class="sxs-lookup"><span data-stu-id="72b1c-113">N</span></span>        |
| <span data-ttu-id="72b1c-114">ProgID \_ übergeordnet</span><span class="sxs-lookup"><span data-stu-id="72b1c-114">ProgId\_Parent</span></span> | [<span data-ttu-id="72b1c-115">Text</span><span class="sxs-lookup"><span data-stu-id="72b1c-115">Text</span></span>](text.md)             | <span data-ttu-id="72b1c-116">N</span><span class="sxs-lookup"><span data-stu-id="72b1c-116">N</span></span>   | <span data-ttu-id="72b1c-117">J</span><span class="sxs-lookup"><span data-stu-id="72b1c-117">Y</span></span>        |
| <span data-ttu-id="72b1c-118">Klasse\_</span><span class="sxs-lookup"><span data-stu-id="72b1c-118">Class\_</span></span>        | [<span data-ttu-id="72b1c-119">GUID</span><span class="sxs-lookup"><span data-stu-id="72b1c-119">GUID</span></span>](guid.md)             | <span data-ttu-id="72b1c-120">N</span><span class="sxs-lookup"><span data-stu-id="72b1c-120">N</span></span>   | <span data-ttu-id="72b1c-121">J</span><span class="sxs-lookup"><span data-stu-id="72b1c-121">Y</span></span>        |
| <span data-ttu-id="72b1c-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72b1c-122">Description</span></span>    | [<span data-ttu-id="72b1c-123">Text</span><span class="sxs-lookup"><span data-stu-id="72b1c-123">Text</span></span>](text.md)             | <span data-ttu-id="72b1c-124">N</span><span class="sxs-lookup"><span data-stu-id="72b1c-124">N</span></span>   | <span data-ttu-id="72b1c-125">J</span><span class="sxs-lookup"><span data-stu-id="72b1c-125">Y</span></span>        |
| <span data-ttu-id="72b1c-126">Symbol\_</span><span class="sxs-lookup"><span data-stu-id="72b1c-126">Icon\_</span></span>         | [<span data-ttu-id="72b1c-127">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="72b1c-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="72b1c-128">N</span><span class="sxs-lookup"><span data-stu-id="72b1c-128">N</span></span>   | <span data-ttu-id="72b1c-129">J</span><span class="sxs-lookup"><span data-stu-id="72b1c-129">Y</span></span>        |
| <span data-ttu-id="72b1c-130">IconIndex</span><span class="sxs-lookup"><span data-stu-id="72b1c-130">IconIndex</span></span>      | [<span data-ttu-id="72b1c-131">Integer</span><span class="sxs-lookup"><span data-stu-id="72b1c-131">Integer</span></span>](integer.md)       | <span data-ttu-id="72b1c-132">N</span><span class="sxs-lookup"><span data-stu-id="72b1c-132">N</span></span>   | <span data-ttu-id="72b1c-133">J</span><span class="sxs-lookup"><span data-stu-id="72b1c-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="72b1c-134">Spalten</span><span class="sxs-lookup"><span data-stu-id="72b1c-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="72b1c-135"><span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgID</span><span class="sxs-lookup"><span data-stu-id="72b1c-135"><span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgId</span></span>
</dt> <dd>

<span data-ttu-id="72b1c-136">Die Programm-ID oder Versions unabhängige Programm-ID.</span><span class="sxs-lookup"><span data-stu-id="72b1c-136">The program ID or version independent program ID.</span></span> <span data-ttu-id="72b1c-137">Die in der ProgID-Tabelle aufgeführten ProgIDs werden registriert, wenn die in der Class-Spalte der Tabelle aufgeführte CLSID \_ angekündigt oder installiert wird.</span><span class="sxs-lookup"><span data-stu-id="72b1c-137">ProgIds listed in the ProgId table are registered if the CLSID listed in the Class\_column of this table is scheduled to be advertised or installed.</span></span> <span data-ttu-id="72b1c-138">Wenn die ProgID für die Registrierung ausgewählt ist, werden alle ProgIDs, die auf diese Zeile über die übergeordnete ProgID-Spalte verweisen, \_ ebenfalls für die Registrierung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="72b1c-138">When the ProgId is selected for registration, all ProgIds that refer to this row through the ProgId\_Parent column are also selected for registration.</span></span>

</dd> <dt>

<span data-ttu-id="72b1c-139"><span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgID \_ übergeordnet</span><span class="sxs-lookup"><span data-stu-id="72b1c-139"><span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId\_Parent</span></span>
</dt> <dd>

<span data-ttu-id="72b1c-140">Nur für Versions unabhängige Programm-IDs definiert.</span><span class="sxs-lookup"><span data-stu-id="72b1c-140">Defined only for version independent program IDs.</span></span> <span data-ttu-id="72b1c-141">Dieses Feld ist ein Fremdschlüssel in die ProgID-Spalte.</span><span class="sxs-lookup"><span data-stu-id="72b1c-141">This field is a foreign key into the ProgId column.</span></span> <span data-ttu-id="72b1c-142">Um eine Versions unabhängige Programm-ID zu definieren, geben Sie die entsprechende ProgID in die übergeordnete ProgID- \_ Spalte ein.</span><span class="sxs-lookup"><span data-stu-id="72b1c-142">To define a version independent program ID, enter the corresponding ProgId into the ProgId\_Parent column.</span></span> <span data-ttu-id="72b1c-143">Wenn die ProgID für die Installation ausgewählt ist, werden die entsprechenden Versions unabhängigen ProgIDs, die über die übergeordnete Spalte ProgID verknüpft \_ sind, ebenfalls für die Registrierung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="72b1c-143">When the ProgId is selected for installation, the corresponding version-independent ProgIds associated through the ProgId\_Parent column are also selected for registration.</span></span>

</dd> <dt>

<span data-ttu-id="72b1c-144"><span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Klassi\_</span><span class="sxs-lookup"><span data-stu-id="72b1c-144"><span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Class\_</span></span>
</dt> <dd>

<span data-ttu-id="72b1c-145">Ein optionaler Fremdschlüssel in die [Klassen Tabelle](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="72b1c-145">An optional foreign key into the [Class table](class-table.md).</span></span> <span data-ttu-id="72b1c-146">Diese Spalte muss für eine Versions unabhängige ProgID NULL sein.</span><span class="sxs-lookup"><span data-stu-id="72b1c-146">This column must be Null for a version independent ProgId.</span></span> <span data-ttu-id="72b1c-147">Wenn der Klassen \_ Wert für eine ProgID NULL ist, wird die ProgID registriert, wenn Sie in der ProgID-Spalte einer Zeile in der [Erweiterungs Tabelle](extension-table.md) angezeigt wird und der Erweiterung mindestens ein Verb in der [Verb Tabelle](verb-table.md)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="72b1c-147">If the Class\_value for a ProgId is null, the ProgId is registered when it appears in the ProgId column of a row in the [Extension table](extension-table.md) and the extension has at least one Verb associated with it in the [Verb table](verb-table.md).</span></span> <span data-ttu-id="72b1c-148">Bei der auf diese Weise für die Registrierung ausgewählten ProgIDs werden andere Programm-IDs, die auf die aktuelle ProgID verweisen, nicht mithilfe des ProgID- \_ Standardwerts installiert.</span><span class="sxs-lookup"><span data-stu-id="72b1c-148">ProgIds selected for registration in this manner do not install other ProgIds that reference the current ProgId through the ProgId\_Default value.</span></span>

</dd> <dt>

<span data-ttu-id="72b1c-149"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72b1c-149"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="72b1c-150">Eine optionale lokalisierte Beschreibung der zugeordneten Programm-ID.</span><span class="sxs-lookup"><span data-stu-id="72b1c-150">An optional localized description of the associated program ID.</span></span>

</dd> <dt>

<span data-ttu-id="72b1c-151"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Angezeigt\_</span><span class="sxs-lookup"><span data-stu-id="72b1c-151"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="72b1c-152">Ein optionaler Fremdschlüssel in der [Symboltabelle](icon-table.md) , der die Symbol Datei angibt, die dieser ProgID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="72b1c-152">An optional foreign key into the [Icon table](icon-table.md) that specifies the icon file associated with this ProgId.</span></span> <span data-ttu-id="72b1c-153">Diese wird unter dem DefaultIcon-Schlüssel geschrieben, der dieser ProgID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="72b1c-153">This is written under the DefaultIcon key associated with this ProgId.</span></span> <span data-ttu-id="72b1c-154">Diese Spalte muss für eine Versions unabhängige ProgID NULL sein.</span><span class="sxs-lookup"><span data-stu-id="72b1c-154">This column must be Null for a version independent ProgId.</span></span>

</dd> <dt>

<span data-ttu-id="72b1c-155"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span><span class="sxs-lookup"><span data-stu-id="72b1c-155"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="72b1c-156">Der Symbol Index in die Symbol Datei.</span><span class="sxs-lookup"><span data-stu-id="72b1c-156">The Icon index into the icon file.</span></span> <span data-ttu-id="72b1c-157">Diese Spalte muss für eine Versions unabhängige ProgID NULL sein.</span><span class="sxs-lookup"><span data-stu-id="72b1c-157">This column must be Null for a version independent ProgId.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72b1c-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72b1c-158">Remarks</span></span>

<span data-ttu-id="72b1c-159">Die Aktionen [registerprogidinfo](registerprogidinfo-action.md) und [unregisterprogidinfo](unregisterprogidinfo-action.md) in [*Sequenz Tabellen*](s-gly.md) verarbeiten die Informationen in dieser Tabelle.</span><span class="sxs-lookup"><span data-stu-id="72b1c-159">The [RegisterProgIdInfo](registerprogidinfo-action.md) and [UnregisterProgIdInfo](unregisterprogidinfo-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="72b1c-160">Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="72b1c-160">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="72b1c-161">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="72b1c-161">Validation</span></span>

<dl>

[<span data-ttu-id="72b1c-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="72b1c-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="72b1c-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="72b1c-163">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="72b1c-164">ICE32</span><span class="sxs-lookup"><span data-stu-id="72b1c-164">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="72b1c-165">ICE36</span><span class="sxs-lookup"><span data-stu-id="72b1c-165">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="72b1c-166">ICE89</span><span class="sxs-lookup"><span data-stu-id="72b1c-166">ICE89</span></span>](ice89.md)  
</dl>

 

 



