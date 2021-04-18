---
description: Die ModuleSignature-Tabelle enthält alle Informationen, die zum Identifizieren des Mergemoduls erforderlich sind.
ms.assetid: 5f0b4590-dac3-4528-b714-ff760ae8d123
title: Erstellen von ModuleSignature-Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796775b0237c17db4fa21075a792c372bed3e97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351638"
---
# <a name="authoring-modulesignature-tables"></a><span data-ttu-id="22806-103">Erstellen von ModuleSignature-Tabellen</span><span class="sxs-lookup"><span data-stu-id="22806-103">Authoring ModuleSignature Tables</span></span>

<span data-ttu-id="22806-104">Die [ModuleSignature-Tabelle](modulesignature-table.md) enthält alle Informationen, die zum Identifizieren des Mergemoduls erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="22806-104">The [ModuleSignature table](modulesignature-table.md) contains all the information needed to identify the merge module.</span></span>

<span data-ttu-id="22806-105">Das ModuleID-Feld ist der Primärschlüssel für diese Tabelle und muss der in Benennen von [primär Schlüsseln in mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md)beschriebenen Konvention folgen.</span><span class="sxs-lookup"><span data-stu-id="22806-105">The ModuleID field is the primary key for this table and must follow the convention described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span> <span data-ttu-id="22806-106">Wenn beispielsweise der lesbare Name des Mergemoduls MyLibrary und die GUID für das Mergemodul {880de2f0-cdd8-11d1-a849-006097abde17} ist, wird der Eintrag in der ModuleID-Spalte der ModuleSignature-Tabelle zu MyLibrary. 880de2f0 \_ CDD8 \_ 11d1 \_ A849 \_ 006097abde17.</span><span class="sxs-lookup"><span data-stu-id="22806-106">For example, if the readable name of the merge module is MyLibrary and the GUID for the merge module is {880DE2F0-CDD8-11D1-A849-006097ABDE17}, the entry in the ModuleID column of the ModuleSignature table becomes MyLibrary.880DE2F0\_CDD8\_11D1\_A849\_006097ABDE17.</span></span>

<span data-ttu-id="22806-107">Geben Sie den Dezimal Bezeichner für die Standardsprache des Mergemoduls in das Sprachfeld der ModuleSignature-Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="22806-107">Enter the decimal identifier for the default language of the merge module into the Language field of the ModuleSignature table.</span></span>

<span data-ttu-id="22806-108">Geben Sie die Version des Mergemoduls in das Feld Version ein.</span><span class="sxs-lookup"><span data-stu-id="22806-108">Enter the version of the merge module into the Version field.</span></span>

 

 



