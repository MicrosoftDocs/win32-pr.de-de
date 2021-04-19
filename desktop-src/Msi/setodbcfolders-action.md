---
description: Die Aktion setodbcfolders überprüft vorhandene ODBC-Treiber auf dem System und legt das Zielverzeichnis jedes neuen Treibers auf den Speicherort eines vorhandenen Treibers fest.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: "\"Stodbcfolders\"-Aktion"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b229d127e976ddb37096c5f3a21605ba8d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343233"
---
# <a name="setodbcfolders-action"></a><span data-ttu-id="b8dcc-103">"Stodbcfolders"-Aktion</span><span class="sxs-lookup"><span data-stu-id="b8dcc-103">SetODBCFolders Action</span></span>

<span data-ttu-id="b8dcc-104">Die Aktion setodbcfolders überprüft vorhandene ODBC-Treiber auf dem System und legt das Zielverzeichnis jedes neuen Treibers auf den Speicherort eines vorhandenen Treibers fest.</span><span class="sxs-lookup"><span data-stu-id="b8dcc-104">The SetODBCFolders action checks for existing ODBC drivers on the system and sets the target directory of each new driver to the location of an existing driver.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b8dcc-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="b8dcc-105">Sequence Restrictions</span></span>

<span data-ttu-id="b8dcc-106">Die "stodbcfolders"-Aktion muss nach der " [costfinalize](costfinalize-action.md) "-Aktion und vor der [InstallValidate-Aktion](installvalidate-action.md)erfolgen.</span><span class="sxs-lookup"><span data-stu-id="b8dcc-106">The SetODBCFolders action must come after the [CostFinalize action](costfinalize-action.md) and before the [InstallValidate action](installvalidate-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b8dcc-107">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="b8dcc-107">ActionData Messages</span></span>



| <span data-ttu-id="b8dcc-108">Feld</span><span class="sxs-lookup"><span data-stu-id="b8dcc-108">Field</span></span> | <span data-ttu-id="b8dcc-109">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="b8dcc-109">Description of action data</span></span>                                                          |
|-------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b8dcc-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b8dcc-110">\[1\]</span></span> | <span data-ttu-id="b8dcc-111">Treiber Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="b8dcc-111">Driver description.</span></span> <span data-ttu-id="b8dcc-112">Der Schlüssel des ODBC-Treibers.</span><span class="sxs-lookup"><span data-stu-id="b8dcc-112">The ODBC driver key.</span></span>                                            |
| <span data-ttu-id="b8dcc-113">\[2\]</span><span class="sxs-lookup"><span data-stu-id="b8dcc-113">\[2\]</span></span> | <span data-ttu-id="b8dcc-114">Ursprünglicher Ordner Speicherort des neuen Treibers.</span><span class="sxs-lookup"><span data-stu-id="b8dcc-114">Original folder location of the new driver.</span></span>                                         |
| <span data-ttu-id="b8dcc-115">\[3\]</span><span class="sxs-lookup"><span data-stu-id="b8dcc-115">\[3\]</span></span> | <span data-ttu-id="b8dcc-116">Neuer Speicherort des Ordners für den neuen Treiber.</span><span class="sxs-lookup"><span data-stu-id="b8dcc-116">New folder location for the new driver.</span></span> <span data-ttu-id="b8dcc-117">Dies ist der Speicherort eines vorhandenen Treibers.</span><span class="sxs-lookup"><span data-stu-id="b8dcc-117">This is the location of an existing driver.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b8dcc-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8dcc-118">Remarks</span></span>

<span data-ttu-id="b8dcc-119">Durch diese Aktion wird ein neuer Treiber in demselben Verzeichnis wie der vorhandene Treiber platziert, der ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b8dcc-119">This action places a new driver into the same directory as the existing driver being replaced.</span></span> <span data-ttu-id="b8dcc-120">Die setodbcfolders-Aktion verwendet die [Verzeichnis Tabelle](directory-table.md) , um die Speicherorte vorhandener Treiber festzulegen, die ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b8dcc-120">The SetODBCFolders action uses the [Directory table](directory-table.md) to set the locations of existing drivers that are to be replaced.</span></span>

 

 



