---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 35 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: Benutzerdefinierter Aktionstyp 35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8401f26f40ccc7de811ea0d290d556789284680f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357033"
---
# <a name="custom-action-type-35"></a><span data-ttu-id="facee-103">Benutzerdefinierter Aktionstyp 35</span><span class="sxs-lookup"><span data-stu-id="facee-103">Custom Action Type 35</span></span>

<span data-ttu-id="facee-104">Diese benutzerdefinierte Aktion legt das Installationsverzeichnis aus einer formatierten Text Zeichenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="facee-104">This custom action sets the install directory from a formatted text string.</span></span> <span data-ttu-id="facee-105">Weitere Informationen finden Sie unter [Ändern des Zielspeicher Orts für ein Verzeichnis](changing-the-target-location-for-a-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="facee-105">For more information, see [Changing the Target Location for a Directory](changing-the-target-location-for-a-directory.md)</span></span>

## <a name="source"></a><span data-ttu-id="facee-106">`Source`</span><span class="sxs-lookup"><span data-stu-id="facee-106">Source</span></span>

<span data-ttu-id="facee-107">Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Schlüssel für die [Verzeichnis Tabelle](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="facee-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Directory table](directory-table.md).</span></span> <span data-ttu-id="facee-108">Das angegebene Verzeichnis wird von der formatierten Zeichenfolge im Zielfeld mithilfe von " [**msisettargetpath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha)" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="facee-108">The designated directory is set by the formatted string in the Target field using [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha).</span></span> <span data-ttu-id="facee-109">Dadurch wird der Zielpfad und die zugehörige Eigenschaft auf den erweiterten Wert der formatierten Text Zeichenfolge im Zielfeld festgelegt.</span><span class="sxs-lookup"><span data-stu-id="facee-109">This sets the target path and associated property to the expanded value of the formatted text string in the Target field.</span></span> <span data-ttu-id="facee-110">Versuchen Sie nicht, den Speicherort eines Zielverzeichnisses während einer [Wartungs Installation](maintenance-installation.md)zu ändern.</span><span class="sxs-lookup"><span data-stu-id="facee-110">Do not attempt to change the location of a target directory during a [maintenance installation](maintenance-installation.md).</span></span> <span data-ttu-id="facee-111">Versuchen Sie nicht, den Zielverzeichnis Pfad zu ändern, wenn einige Komponenten, die diesen Pfad verwenden, für einen beliebigen Benutzer bereits installiert sind.</span><span class="sxs-lookup"><span data-stu-id="facee-111">Do not attempt to change the target directory path if some components using that path are already installed for any user.</span></span>

## <a name="type-value"></a><span data-ttu-id="facee-112">Typwert</span><span class="sxs-lookup"><span data-stu-id="facee-112">Type Value</span></span>

<span data-ttu-id="facee-113">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.</span><span class="sxs-lookup"><span data-stu-id="facee-113">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="facee-114">Konstanten</span><span class="sxs-lookup"><span data-stu-id="facee-114">Constants</span></span>                                                              | <span data-ttu-id="facee-115">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="facee-115">Hexadecimal</span></span> | <span data-ttu-id="facee-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="facee-116">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="facee-117">**msidbcustomaktiontypetextdata**  +  **msidbcustomaktiontypedirectory**</span><span class="sxs-lookup"><span data-stu-id="facee-117">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="facee-118">0x023</span><span class="sxs-lookup"><span data-stu-id="facee-118">0x023</span></span>       | <span data-ttu-id="facee-119">35</span><span class="sxs-lookup"><span data-stu-id="facee-119">35</span></span>      |



 

## <a name="target"></a><span data-ttu-id="facee-120">Ziel</span><span class="sxs-lookup"><span data-stu-id="facee-120">Target</span></span>

<span data-ttu-id="facee-121">Die Ziel Spalte der [Tabelle CustomAction](customaction-table.md) enthält eine Text Zeichenfolge, die mit der in [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (ohne numerische feldspezifizierer) angegebenen Funktionalität formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="facee-121">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="facee-122">Die zu ersetzenden Parameter werden in eckige Klammern eingeschlossen \[ ... \] , und können Eigenschaften, Umgebungsvariablen (% prefix), Dateipfade ( \# Präfix) oder Komponenten Verzeichnispfade ($ prefix) sein.</span><span class="sxs-lookup"><span data-stu-id="facee-122">Parameters to be replaced are enclosed in square brackets \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span> <span data-ttu-id="facee-123">Beachten Sie, dass Verzeichnispfade immer mit einem Verzeichnis Trennzeichen enden.</span><span class="sxs-lookup"><span data-stu-id="facee-123">Note that directory paths always end with a directory separator.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="facee-124">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="facee-124">Return Processing Options</span></span>

<span data-ttu-id="facee-125">Diese Optionen werden von der benutzerdefinierten Aktion nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="facee-125">The custom action does not use these options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="facee-126">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="facee-126">Execution Scheduling Options</span></span>

<span data-ttu-id="facee-127">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="facee-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="facee-128">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="facee-128">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="facee-129">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="facee-129">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="facee-130">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="facee-130">In-Script Execution Options</span></span>

<span data-ttu-id="facee-131">Diese Optionen werden von der benutzerdefinierten Aktion nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="facee-131">The custom action does not use these options.</span></span>

## <a name="return-values"></a><span data-ttu-id="facee-132">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="facee-132">Return Values</span></span>

<span data-ttu-id="facee-133">Siehe [Rückgabewerte für benutzerdefinierte Aktionen](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="facee-133">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="facee-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="facee-134">Remarks</span></span>

<span data-ttu-id="facee-135">Wenn Sie in der UI-Sequenz eine [private Eigenschaft](private-properties.md) festlegen, indem Sie eine benutzerdefinierte Aktion in einer der Benutzeroberflächen-Sequenz Tabellen erstellen, wird diese Eigenschaft nicht in der Ausführungssequenz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="facee-135">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="facee-136">Wenn Sie die-Eigenschaft in der Ausführungssequenz festlegen möchten, müssen Sie auch eine benutzerdefinierte Aktion in eine Ausführungssequenz Tabelle einfügen.</span><span class="sxs-lookup"><span data-stu-id="facee-136">To set the property in the execution sequence you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="facee-137">Alternativ können Sie die Eigenschaft zu einer [öffentlichen Eigenschaft](public-properties.md) machen und in der [**securecustomproperties-Eigenschaft**](securecustomproperties.md)einschließen.</span><span class="sxs-lookup"><span data-stu-id="facee-137">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties property**](securecustomproperties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="facee-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="facee-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="facee-139">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="facee-139">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="facee-140">Formatierte Text benutzerdefinierte Aktionen</span><span class="sxs-lookup"><span data-stu-id="facee-140">Formatted Text Custom Actions</span></span>](formatted-text-custom-actions.md)
</dt> </dl>

 

 



