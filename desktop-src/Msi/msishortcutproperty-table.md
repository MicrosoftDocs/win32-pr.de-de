---
description: Die msishortcutproperty-Tabelle ermöglicht dem Fenster Installer das Festlegen von Eigenschaften für Tastenkombinationen, die auch als Windows-Shellobjekte dienen.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Msishortcutproperty-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529798"
---
# <a name="msishortcutproperty-table"></a><span data-ttu-id="9361d-103">Msishortcutproperty-Tabelle</span><span class="sxs-lookup"><span data-stu-id="9361d-103">MsiShortcutProperty Table</span></span>

<span data-ttu-id="9361d-104">Die msishortcutproperty-Tabelle ermöglicht dem Fenster Installer das Festlegen von Eigenschaften für Tastenkombinationen, die auch als [Windows-Shellobjekte](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) dienen.</span><span class="sxs-lookup"><span data-stu-id="9361d-104">The MsiShortcutProperty table enables Window Installer to set properties for shortcuts that are also [Windows Shell](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) objects.</span></span> <span data-ttu-id="9361d-105">Ab Windows Vista und Windows Server 2008 bietet die Windows-Shell eine IPropertyStore-Schnittstelle für Shellobjekte wie z. b. Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="9361d-105">Beginning with Windows Vista and Windows Server 2008 the Windows Shell provides an IPropertyStore Interface for shell objects such as shortcuts.</span></span> <span data-ttu-id="9361d-106">Mit einem Windows Installer 5,0-Paket, das unter Windows Server 2008 R2 oder Windows 7 ausgeführt wird, können diese Eigenschaften festgelegt werden, wenn die Verknüpfung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="9361d-106">A Windows Installer 5.0 package running on Windows Server 2008 R2 or Windows 7 can set these properties when the shortcut is installed.</span></span>

<span data-ttu-id="9361d-107">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9361d-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="9361d-108">Diese Tabelle ist ab Windows Installer 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9361d-108">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="9361d-109">Die msishortcutproperty-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="9361d-109">The MsiShortcutProperty table has the following columns.</span></span>



| <span data-ttu-id="9361d-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="9361d-110">Column</span></span>              | <span data-ttu-id="9361d-111">Typ</span><span class="sxs-lookup"><span data-stu-id="9361d-111">Type</span></span>                         | <span data-ttu-id="9361d-112">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="9361d-112">Key</span></span> | <span data-ttu-id="9361d-113">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="9361d-113">Nullable</span></span> |
|---------------------|------------------------------|-----|----------|
| <span data-ttu-id="9361d-114">Msishortcutproperty</span><span class="sxs-lookup"><span data-stu-id="9361d-114">MsiShortcutProperty</span></span> | [<span data-ttu-id="9361d-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="9361d-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="9361d-116">J</span><span class="sxs-lookup"><span data-stu-id="9361d-116">Y</span></span>   | <span data-ttu-id="9361d-117">N</span><span class="sxs-lookup"><span data-stu-id="9361d-117">N</span></span>        |
| <span data-ttu-id="9361d-118">Abkürzung\_</span><span class="sxs-lookup"><span data-stu-id="9361d-118">Shortcut\_</span></span>          | [<span data-ttu-id="9361d-119">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="9361d-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="9361d-120">N</span><span class="sxs-lookup"><span data-stu-id="9361d-120">N</span></span>   | <span data-ttu-id="9361d-121">N</span><span class="sxs-lookup"><span data-stu-id="9361d-121">N</span></span>        |
| <span data-ttu-id="9361d-122">PropertyKey</span><span class="sxs-lookup"><span data-stu-id="9361d-122">PropertyKey</span></span>         | [<span data-ttu-id="9361d-123">Großformatige</span><span class="sxs-lookup"><span data-stu-id="9361d-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="9361d-124">N</span><span class="sxs-lookup"><span data-stu-id="9361d-124">N</span></span>   | <span data-ttu-id="9361d-125">N</span><span class="sxs-lookup"><span data-stu-id="9361d-125">N</span></span>        |
| <span data-ttu-id="9361d-126">Propvariantvalue</span><span class="sxs-lookup"><span data-stu-id="9361d-126">PropVariantValue</span></span>    | [<span data-ttu-id="9361d-127">Großformatige</span><span class="sxs-lookup"><span data-stu-id="9361d-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="9361d-128">N</span><span class="sxs-lookup"><span data-stu-id="9361d-128">N</span></span>   | <span data-ttu-id="9361d-129">N</span><span class="sxs-lookup"><span data-stu-id="9361d-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9361d-130">Spalten</span><span class="sxs-lookup"><span data-stu-id="9361d-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9361d-131"><span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>Msishortcutproperty</span><span class="sxs-lookup"><span data-stu-id="9361d-131"><span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty</span></span>
</dt> <dd>

<span data-ttu-id="9361d-132">Eindeutiger Bezeichner für diese Zeile der msishortcutproperty-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9361d-132">Unique identifier for this row of the MsiShortcutProperty table.</span></span>

</dd> <dt>

<span data-ttu-id="9361d-133"><span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Kontext\_</span><span class="sxs-lookup"><span data-stu-id="9361d-133"><span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Shortcut\_</span></span>
</dt> <dd>

<span data-ttu-id="9361d-134">Ein Schlüssel in die [Verknüpfungs Tabelle, der die](shortcut-table.md) Verknüpfung mit einem Eigenschaften Satz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9361d-134">A key into the [Shortcut](shortcut-table.md) table that identifies the shortcut having a property set.</span></span>

</dd> <dt>

<span data-ttu-id="9361d-135"><span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey</span><span class="sxs-lookup"><span data-stu-id="9361d-135"><span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey</span></span>
</dt> <dd>

<span data-ttu-id="9361d-136">Ein Zeichen folgen Wert, der Informationen für die [**PropertyKey**](/windows/win32/api/wtypes/ns-wtypes-propertykey) -Struktur bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9361d-136">A string value that provides information for the [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure.</span></span> <span data-ttu-id="9361d-137">Die Informationen in diesem Feld müssen auf den kanonischen Namen einer Eigenschaft verweisen, die beim Windows-Eigenschaften System registriert ist.</span><span class="sxs-lookup"><span data-stu-id="9361d-137">The information in this field must refer to the canonical name of a property registered with the Windows property system.</span></span> <span data-ttu-id="9361d-138">Weitere Informationen zum Windows-Eigenschaften System finden Sie in der [Übersicht über das Eigenschaften System](/previous-versions//bb776909(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9361d-138">For more information about the Windows property system, see the [Property System Overview](/previous-versions//bb776909(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9361d-139"><span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>Propvariantvalue</span><span class="sxs-lookup"><span data-stu-id="9361d-139"><span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue</span></span>
</dt> <dd>

<span data-ttu-id="9361d-140">Ein Zeichen folgen Wert, der Informationen für die [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9361d-140">A string value that provides information for the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

</dd> </dl>

<span data-ttu-id="9361d-141">Für eine Verknüpfung können mehrere Eigenschaften festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9361d-141">Multiple properties can be set on a shortcut.</span></span> <span data-ttu-id="9361d-142">Wenn dieselbe Eigenschaft mehrmals bei derselben Verknüpfung festgelegt wird, wird der Wert in einer nicht angegebenen Reihenfolge festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9361d-142">If the same property is set multiple times on the same shortcut the value is set in an unspecified order.</span></span>

<span data-ttu-id="9361d-143">Windows Installer können die Verknüpfungs Eigenschaften nur festlegen, wenn die Verknüpfung installiert oder neu installiert wird.</span><span class="sxs-lookup"><span data-stu-id="9361d-143">Windows Installer can set shortcut properties only when the shortcut is installed or reinstalled.</span></span> <span data-ttu-id="9361d-144">Bei einem Patch, bei dem eine bereits installierte Verknüpfung nicht neu installiert wird, werden die Eigenschaften der Verknüpfung nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9361d-144">A patch that does not reinstall a shortcut that has already been installed does not update the shortcut's properties.</span></span> <span data-ttu-id="9361d-145">Ein Patch kann die Eigenschaften aktualisieren, indem er [eine](shortcut-table.md) Verknüpfungs Tabelle in das Patchpaket einschließt und die Verknüpfung erneut installiert.</span><span class="sxs-lookup"><span data-stu-id="9361d-145">A patch can update the properties by including a [Shortcut](shortcut-table.md) table in the patch package and reinstalling the shortcut.</span></span>

## <a name="remarks"></a><span data-ttu-id="9361d-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9361d-146">Remarks</span></span>

<span data-ttu-id="9361d-147">[Windows Installer Fehlermeldung](windows-installer-error-messages.md) 1946 wird als Warnung zurückgegeben, und die Installation wird fortgesetzt, wenn Windows Installer keine in der Tabelle msishortcutproperty angegebene Verknüpfungs Eigenschaft festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="9361d-147">[Windows Installer Error Message](windows-installer-error-messages.md) 1946 is returned as a warning, and the installation continues, if Windows Installer is unable to set a shortcut property specified in the MsiShortcutProperty table.</span></span>

## <a name="validation"></a><span data-ttu-id="9361d-148">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="9361d-148">Validation</span></span>

<dl>

[<span data-ttu-id="9361d-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="9361d-149">ICE03</span></span>](ice03.md)  
</dl>

 

 
