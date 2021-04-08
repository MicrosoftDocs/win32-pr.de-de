---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 51 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: Benutzerdefinierter Aktionstyp 51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3224add3a425131ee3308bc4f610b086cd99a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960351"
---
# <a name="custom-action-type-51"></a><span data-ttu-id="f9966-103">Benutzerdefinierter Aktionstyp 51</span><span class="sxs-lookup"><span data-stu-id="f9966-103">Custom Action Type 51</span></span>

<span data-ttu-id="f9966-104">Diese benutzerdefinierte Aktion legt eine Eigenschaft aus einer formatierten Text Zeichenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="f9966-104">This custom action sets a property from a formatted text string.</span></span>

<span data-ttu-id="f9966-105">Um eine Eigenschaft zu beeinflussen, die in einer Bedingung für eine Komponente oder eine Funktion verwendet wird, muss die benutzerdefinierte Aktion vor der [Aktion "costfinalize](costfinalize-action.md) " in der Aktions Sequenz erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f9966-105">To affect a property used in a condition on a component or feature, the custom action must come before the [CostFinalize action](costfinalize-action.md) in the action sequence.</span></span>

## <a name="source"></a><span data-ttu-id="f9966-106">`Source`</span><span class="sxs-lookup"><span data-stu-id="f9966-106">Source</span></span>

<span data-ttu-id="f9966-107">Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " kann entweder den Namen einer Eigenschaft oder einen Schlüssel für die [Eigenschaften Tabelle](property-table.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="f9966-107">The Source field of the [CustomAction table](customaction-table.md) can contain either the name of a property or a key to the [Property table](property-table.md).</span></span> <span data-ttu-id="f9966-108">Diese Eigenschaft wird von der formatierten Zeichenfolge im Zielfeld mithilfe von " [**msisetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9966-108">This property is set by the formatted string in the Target field using [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).</span></span>

## <a name="type-value"></a><span data-ttu-id="f9966-109">Typwert</span><span class="sxs-lookup"><span data-stu-id="f9966-109">Type Value</span></span>

<span data-ttu-id="f9966-110">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f9966-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="f9966-111">Konstanten</span><span class="sxs-lookup"><span data-stu-id="f9966-111">Constants</span></span>                                                             | <span data-ttu-id="f9966-112">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="f9966-112">Hexadecimal</span></span> | <span data-ttu-id="f9966-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="f9966-113">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="f9966-114">**msidbcustomaktiontypetextdata**  +  **msidbcustomaktiontypeproperty**</span><span class="sxs-lookup"><span data-stu-id="f9966-114">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="f9966-115">0x033</span><span class="sxs-lookup"><span data-stu-id="f9966-115">0x033</span></span>       | <span data-ttu-id="f9966-116">51</span><span class="sxs-lookup"><span data-stu-id="f9966-116">51</span></span>      |



 

## <a name="target"></a><span data-ttu-id="f9966-117">Ziel</span><span class="sxs-lookup"><span data-stu-id="f9966-117">Target</span></span>

<span data-ttu-id="f9966-118">Die Ziel Spalte der [Tabelle CustomAction](customaction-table.md) enthält eine Text Zeichenfolge, die mit der in [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (ohne numerische feldspezifizierer) angegebenen Funktionalität formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="f9966-118">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="f9966-119">Die zu ersetzenden Parameter sind in eckige Klammern ( \[ ...) eingeschlossen \] und können Eigenschaften, Umgebungsvariablen (% prefix), Dateipfade ( \# Präfix) oder Komponenten Verzeichnispfade ($ prefix) sein.</span><span class="sxs-lookup"><span data-stu-id="f9966-119">Parameters to be replaced are enclosed in square brackets, \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="f9966-120">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="f9966-120">Return Processing Options</span></span>

<span data-ttu-id="f9966-121">Diese Optionen werden von der benutzerdefinierten Aktion nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9966-121">The custom action does not use these options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="f9966-122">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="f9966-122">Execution Scheduling Options</span></span>

<span data-ttu-id="f9966-123">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f9966-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="f9966-124">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="f9966-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="f9966-125">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="f9966-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="f9966-126">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="f9966-126">In-Script Execution Options</span></span>

<span data-ttu-id="f9966-127">Diese Optionen werden von der benutzerdefinierten Aktion nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9966-127">The custom action does not use these options.</span></span>

## <a name="return-values"></a><span data-ttu-id="f9966-128">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f9966-128">Return Values</span></span>

<span data-ttu-id="f9966-129">Siehe [Rückgabewerte für benutzerdefinierte Aktionen](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f9966-129">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f9966-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9966-130">Remarks</span></span>

<span data-ttu-id="f9966-131">Wenn Sie in der UI-Sequenz eine [private Eigenschaft](private-properties.md) festlegen, indem Sie eine benutzerdefinierte Aktion in einer der Benutzeroberflächen-Sequenz Tabellen erstellen, wird diese Eigenschaft nicht in der Ausführungssequenz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f9966-131">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="f9966-132">Wenn Sie die-Eigenschaft in der Ausführungssequenz festlegen möchten, müssen Sie auch eine benutzerdefinierte Aktion in eine Ausführungssequenz Tabelle einfügen.</span><span class="sxs-lookup"><span data-stu-id="f9966-132">To set the property in the execution sequence, you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="f9966-133">Alternativ können Sie die Eigenschaft zu einer [öffentlichen Eigenschaft](public-properties.md) machen und in der [**securecustomproperties-Eigenschaft**](securecustomproperties.md)einschließen.</span><span class="sxs-lookup"><span data-stu-id="f9966-133">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties property**](securecustomproperties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9966-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9966-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9966-135">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="f9966-135">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="f9966-136">Formatierte Text benutzerdefinierte Aktionen</span><span class="sxs-lookup"><span data-stu-id="f9966-136">Formatted Text Custom Actions</span></span>](formatted-text-custom-actions.md)
</dt> </dl>

 

 



