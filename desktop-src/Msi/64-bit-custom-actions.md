---
description: Bei 64-Bit-Betriebssystemen können Windows Installer benutzerdefinierte Aktionen aufzurufen, die für 32-Bit-oder 64-Bit-Systeme kompiliert wurden.
ms.assetid: fc370ab4-93f3-4e1e-9468-3454d4fee0be
title: benutzerdefinierte 64-Bit-Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fcd804152abd010f985aab3b92c0de73a2744f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756259"
---
# <a name="64-bit-custom-actions"></a><span data-ttu-id="0adc2-103">benutzerdefinierte 64-Bit-Aktionen</span><span class="sxs-lookup"><span data-stu-id="0adc2-103">64-Bit Custom Actions</span></span>

<span data-ttu-id="0adc2-104">Bei 64-Bit-Betriebssystemen können Windows Installer benutzerdefinierte Aktionen aufzurufen, die für 32-Bit-oder 64-Bit-Systeme kompiliert wurden.</span><span class="sxs-lookup"><span data-stu-id="0adc2-104">On 64-bit operating systems, Windows Installer may call custom actions that have been compiled for 32-bit or 64-bit systems.</span></span>

<span data-ttu-id="0adc2-105">Eine benutzerdefinierte 64-Bit-Aktion, die auf [Skripts](scripts.md) basiert, muss explizit als 64 eine benutzerdefinierte 32-Bit-Aktion gekennzeichnet werden, indem das **msidbCustomActionType64BitScript** -Bit dem numerischen Typ benutzerdefinierte Aktionen in der Type-Spalte der [CustomAction-Tabelle](customaction-table.md)hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="0adc2-105">A 64-bit custom action based on [Scripts](scripts.md) must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom actions numeric type in the Type column of the [CustomAction table](customaction-table.md).</span></span>



| <span data-ttu-id="0adc2-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="0adc2-106">Constant</span></span>                             | <span data-ttu-id="0adc2-107">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="0adc2-107">Hexadecimal</span></span> | <span data-ttu-id="0adc2-108">Decimal</span><span class="sxs-lookup"><span data-stu-id="0adc2-108">Decimal</span></span> | <span data-ttu-id="0adc2-109">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0adc2-109">Meaning</span></span>                                                           |
|--------------------------------------|-------------|---------|-------------------------------------------------------------------|
| <span data-ttu-id="0adc2-110">**msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="0adc2-110">**msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="0adc2-111">0x0001000</span><span class="sxs-lookup"><span data-stu-id="0adc2-111">0x0001000</span></span>   | <span data-ttu-id="0adc2-112">4096</span><span class="sxs-lookup"><span data-stu-id="0adc2-112">4096</span></span>    | <span data-ttu-id="0adc2-113">Dabei handelt es sich um eine in [Skripts](scripts.md)geschriebene benutzerdefinierte 64-Bit-Aktion.</span><span class="sxs-lookup"><span data-stu-id="0adc2-113">This is a 64-bit custom action written in [Scripts](scripts.md).</span></span> |



 

<span data-ttu-id="0adc2-114">Benutzerdefinierte Aktionen, die auf [ausführbaren Dateien](executable-files.md) oder [Dynamic Link-Bibliotheken](dynamic-link-libraries.md) basieren, die für ein 64-Bit-Betriebssystem ausgeführt wurden, müssen dieses zusätzliche Bit nicht in die Spalte Type der Tabelle CustomAction einschließen.</span><span class="sxs-lookup"><span data-stu-id="0adc2-114">Custom actions based on [Executable files](executable-files.md) or [Dynamic-Link Libraries](dynamic-link-libraries.md) that have been complied for a 64-bit operating systems do not require including this additional bit in the Type column of the CustomAction table.</span></span>

 

 



