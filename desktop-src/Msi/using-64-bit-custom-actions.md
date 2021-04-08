---
description: Auf 64-Bit-Betriebssystemen können Windows Installer benutzerdefinierte Aktionen aufzurufen, die für 32-Bit-oder 64-Bit-Systeme kompiliert werden.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Verwenden von benutzerdefinierten 64-Bit-Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1465f1b82d18c8e07d95e6d3ab08e9da6827bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960147"
---
# <a name="using-64-bit-custom-actions"></a><span data-ttu-id="e78e9-103">Verwenden von benutzerdefinierten 64-Bit-Aktionen</span><span class="sxs-lookup"><span data-stu-id="e78e9-103">Using 64-bit Custom Actions</span></span>

<span data-ttu-id="e78e9-104">Auf 64-Bit-Betriebssystemen können Windows Installer benutzerdefinierte Aktionen aufzurufen, die für 32-Bit-oder 64-Bit-Systeme kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="e78e9-104">On 64-bit operating systems, Windows Installer can call custom actions that are compiled for 32-bit or 64-bit systems.</span></span> <span data-ttu-id="e78e9-105">Eine benutzerdefinierte 64-Bit-Aktion, die auf [Skripts](scripts.md) basiert, muss explizit als 64 eine benutzerdefinierte 32-Bit-Aktion gekennzeichnet werden, indem das **msidbCustomActionType64BitScript** -Bit dem numerischen Typ benutzerdefinierte Aktion in der Type-Spalte der [CustomAction-Tabelle](customaction-table.md)hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e78e9-105">A 64-bit custom action based on [Scripts](scripts.md) must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom action numeric type in the Type column of the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="e78e9-106">Benutzerdefinierte Aktionen, die auf [ausführbaren Dateien](executable-files.md) oder [Dynamic Link-Bibliotheken](dynamic-link-libraries.md) basieren, die für 64-Bit-Betriebssysteme erfüllt werden, müssen dieses zusätzliche Bit nicht in die Spalte Type der Tabelle CustomAction einschließen.</span><span class="sxs-lookup"><span data-stu-id="e78e9-106">Custom actions based on [Executable files](executable-files.md) or [Dynamic-Link Libraries](dynamic-link-libraries.md) that are complied for 64-bit operating systems do not require including this additional bit in the Type column of the CustomAction Table.</span></span>

<span data-ttu-id="e78e9-107">Weitere Informationen finden Sie unter [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="e78e9-107">For more information, see [64-Bit Custom Actions](64-bit-custom-actions.md).</span></span>

 

 



