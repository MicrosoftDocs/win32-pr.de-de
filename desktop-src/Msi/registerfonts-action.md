---
description: Mit der RegisterFonts-Aktion werden installierte Schriftarten beim System registriert. Durch diese Aktion wird der Schriftart Name in der FontTitle-Spalte der Schriftart Tabelle dem Pfad der installierten Schriftart Datei zugeordnet.
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: RegisterFonts-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98532be2744e89fff79f6e3d8becd2e6cc9259a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362206"
---
# <a name="registerfonts-action"></a><span data-ttu-id="04e31-104">RegisterFonts-Aktion</span><span class="sxs-lookup"><span data-stu-id="04e31-104">RegisterFonts Action</span></span>

<span data-ttu-id="04e31-105">Mit der RegisterFonts-Aktion werden installierte Schriftarten beim System registriert.</span><span class="sxs-lookup"><span data-stu-id="04e31-105">The RegisterFonts action registers installed fonts with the system.</span></span> <span data-ttu-id="04e31-106">Durch diese Aktion wird der Schriftart Name in der FontTitle-Spalte der [Schriftart Tabelle](font-table.md) dem Pfad der installierten Schriftart Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="04e31-106">This action maps the font name in the FontTitle column of the [Font table](font-table.md) to the path of the font file installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="04e31-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="04e31-107">Sequence Restrictions</span></span>

<span data-ttu-id="04e31-108">Vor dem Aufrufen der RegisterFonts-Aktion muss die [InstallFiles](installfiles-action.md) -Aktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="04e31-108">The [InstallFiles](installfiles-action.md) action must be called before calling the RegisterFonts action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="04e31-109">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="04e31-109">ActionData Messages</span></span>



| <span data-ttu-id="04e31-110">Feld</span><span class="sxs-lookup"><span data-stu-id="04e31-110">Field</span></span> | <span data-ttu-id="04e31-111">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="04e31-111">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="04e31-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="04e31-112">\[1\]</span></span> | <span data-ttu-id="04e31-113">Schriftart Datei.</span><span class="sxs-lookup"><span data-stu-id="04e31-113">Font file.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="04e31-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04e31-114">Remarks</span></span>

<span data-ttu-id="04e31-115">Die Aktion RegisterFonts wird ausgeführt, wenn die Datei, die in der \_ Spalte Datei der [Schriftart Tabelle](font-table.md) angegeben ist, zu einer Komponente gehört, die installiert wird.</span><span class="sxs-lookup"><span data-stu-id="04e31-115">The RegisterFonts action is executed if the file specified in the File\_ column of the [Font table](font-table.md) belongs to a component being installed.</span></span>

 

 



