---
description: Die ccpsearch-Tabelle enthält die Liste der Datei Signaturen, die für das Kompatibilitäts Überprüfungs Programm (CCP) verwendet werden. Mindestens eine dieser Dateien muss auf dem Computer eines Benutzers vorhanden sein, damit der Benutzer mit dem Programm konform ist.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Ccpsearch-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c0452fea011aca1080ca17020467ba6e0dc4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356678"
---
# <a name="ccpsearch-table"></a><span data-ttu-id="b64b8-104">Ccpsearch-Tabelle</span><span class="sxs-lookup"><span data-stu-id="b64b8-104">CCPSearch Table</span></span>

<span data-ttu-id="b64b8-105">Die ccpsearch-Tabelle enthält die Liste der Datei Signaturen, die für das Kompatibilitäts Überprüfungs Programm (CCP) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b64b8-105">The CCPSearch table contains the list of file signatures used for the Compliance Checking Program (CCP).</span></span> <span data-ttu-id="b64b8-106">Mindestens eine dieser Dateien muss auf dem Computer eines Benutzers vorhanden sein, damit der Benutzer mit dem Programm konform ist.</span><span class="sxs-lookup"><span data-stu-id="b64b8-106">At least one of these files needs to be present on a user's computer for the user to be in compliance with the program.</span></span>

<span data-ttu-id="b64b8-107">Die ccpsearch-Tabelle weist die folgende Spalte auf.</span><span class="sxs-lookup"><span data-stu-id="b64b8-107">The CCPSearch table has the following column.</span></span>



| <span data-ttu-id="b64b8-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="b64b8-108">Column</span></span>      | <span data-ttu-id="b64b8-109">Typ</span><span class="sxs-lookup"><span data-stu-id="b64b8-109">Type</span></span>                         | <span data-ttu-id="b64b8-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b64b8-110">Key</span></span> | <span data-ttu-id="b64b8-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="b64b8-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="b64b8-112">Signatur\_</span><span class="sxs-lookup"><span data-stu-id="b64b8-112">Signature\_</span></span> | [<span data-ttu-id="b64b8-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b64b8-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="b64b8-114">J</span><span class="sxs-lookup"><span data-stu-id="b64b8-114">Y</span></span>   | <span data-ttu-id="b64b8-115">N</span><span class="sxs-lookup"><span data-stu-id="b64b8-115">N</span></span>        |



 

## <a name="column"></a><span data-ttu-id="b64b8-116">Column</span><span class="sxs-lookup"><span data-stu-id="b64b8-116">Column</span></span>

<dl> <dt>

<span data-ttu-id="b64b8-117"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Unter\_</span><span class="sxs-lookup"><span data-stu-id="b64b8-117"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="b64b8-118">Die Signatur \_ stellt eine eindeutige Datei Signatur dar und ist auch der externe Schlüssel in den Tabellen " [Signature](signature-table.md)", " [reglocator](reglocator-table.md)", " [inilocator](inilocator-table.md)", " [complocator](complocator-table.md)" und " [drlocator](drlocator-table.md) ".</span><span class="sxs-lookup"><span data-stu-id="b64b8-118">The Signature\_ represents a unique file signature and is also the external key into the [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md), and [DrLocator](drlocator-table.md) tables.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b64b8-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b64b8-119">Remarks</span></span>

<span data-ttu-id="b64b8-120">Auf diese Tabelle wird verwiesen, wenn die [ccpsearch-Aktion](ccpsearch-action.md) oder die [RMCCPSEARCH-Aktion](rmccpsearch-action.md) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b64b8-120">This table is referred to when the [CCPSearch action](ccpsearch-action.md) or the [RMCCPSearch action](rmccpsearch-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="b64b8-121">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="b64b8-121">Validation</span></span>

<dl>

[<span data-ttu-id="b64b8-122">ICE03</span><span class="sxs-lookup"><span data-stu-id="b64b8-122">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b64b8-123">ICE06</span><span class="sxs-lookup"><span data-stu-id="b64b8-123">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b64b8-124">ICE32</span><span class="sxs-lookup"><span data-stu-id="b64b8-124">ICE32</span></span>](ice32.md)  
</dl>

 

 



