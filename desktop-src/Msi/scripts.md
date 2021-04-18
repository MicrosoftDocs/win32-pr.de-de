---
description: Eine benutzerdefinierte Aktion kann Funktionen aufzurufen, die in VBScript oder JScript geschrieben sind.
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114a11c12e94dd2f3285757bd01167f14b412ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358462"
---
# <a name="scripts"></a><span data-ttu-id="81100-103">Skripts</span><span class="sxs-lookup"><span data-stu-id="81100-103">Scripts</span></span>

<span data-ttu-id="81100-104">Eine benutzerdefinierte Aktion kann Funktionen aufzurufen, die in VBScript oder JScript geschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="81100-104">A custom action can call functions that are written in VBScript or JScript.</span></span> <span data-ttu-id="81100-105">Windows Installer stellt die Skript-Engine nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="81100-105">Windows Installer does not provide the script engine.</span></span> <span data-ttu-id="81100-106">Autoren, die während der Installation eine Skriptsprache verwenden möchten, müssen daher sicherstellen, dass die entsprechende Skript-Engine verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="81100-106">Authors wishing to make use of a scripting language during installation must therefore ensure that the appropriate scripting engine is available.</span></span>

<span data-ttu-id="81100-107">Die JScript-Version 1,0 wird vom Installationsprogramm nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81100-107">The installer does not support JScript version 1.0.</span></span>

<span data-ttu-id="81100-108">Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss explizit als 64 eine benutzerdefinierte 32-Bit-Aktion gekennzeichnet werden, indem das **msidbCustomActionType64BitScript** -Bit dem numerischen Typ benutzerdefinierte Aktionen in der Type-Spalte der [CustomAction](customaction-table.md) -Tabelle hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="81100-108">A 64-bit custom action based on scripts must be explicitly marked as a 64-bit custom action by adding the **msidbCustomActionType64BitScript** bit to the custom actions numeric type in the Type column of the [CustomAction](customaction-table.md) table.</span></span> <span data-ttu-id="81100-109">Weitere Informationen finden Sie unter [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="81100-109">For information see [64-Bit Custom Actions](64-bit-custom-actions.md).</span></span>

<span data-ttu-id="81100-110">Die folgenden grundlegenden benutzerdefinierten Aktions Typen werden in Skripts geschriebene Funktionen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="81100-110">The following basic custom action types call functions written in script.</span></span>



| <span data-ttu-id="81100-111">Benutzerdefinierter Aktionstyp</span><span class="sxs-lookup"><span data-stu-id="81100-111">Custom action type</span></span>                                 | <span data-ttu-id="81100-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81100-112">Description</span></span>                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81100-113">Benutzerdefinierter Aktionstyp 5</span><span class="sxs-lookup"><span data-stu-id="81100-113">Custom Action Type 5</span></span>](custom-action-type-5.md)   | <span data-ttu-id="81100-114">JScript-Datei, die in einem binären Tabellenstream gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="81100-114">JScript file stored in a Binary table stream.</span></span>                                                  |
| [<span data-ttu-id="81100-115">Benutzerdefinierter Aktionstyp 21</span><span class="sxs-lookup"><span data-stu-id="81100-115">Custom Action Type 21</span></span>](custom-action-type-21.md) | <span data-ttu-id="81100-116">JScript-Datei, die mit einem Produkt installiert wird.</span><span class="sxs-lookup"><span data-stu-id="81100-116">JScript file that is installed with a product.</span></span>                                                 |
| [<span data-ttu-id="81100-117">Benutzerdefinierter Aktionstyp 53</span><span class="sxs-lookup"><span data-stu-id="81100-117">Custom Action Type 53</span></span>](custom-action-type-53.md) | <span data-ttu-id="81100-118">Der von einem Eigenschafts Wert angegebene JScript-Text.</span><span class="sxs-lookup"><span data-stu-id="81100-118">JScript text specified by a property value.</span></span>                                                    |
| [<span data-ttu-id="81100-119">Benutzerdefinierter Aktionstyp 37</span><span class="sxs-lookup"><span data-stu-id="81100-119">Custom Action Type 37</span></span>](custom-action-type-37.md) | <span data-ttu-id="81100-120">JScript-Text, der in der Ziel Spalte der [CustomAction](customaction-table.md) -Tabelle gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="81100-120">JScript text stored in the Target column of the [CustomAction](customaction-table.md) table.</span></span>  |
| [<span data-ttu-id="81100-121">Benutzerdefinierter Aktionstyp 6</span><span class="sxs-lookup"><span data-stu-id="81100-121">Custom Action Type 6</span></span>](custom-action-type-6.md)   | <span data-ttu-id="81100-122">VBScript-Datei, die in einem [binären](binary-table.md) Tabellenstream gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="81100-122">VBScript file stored in a [Binary](binary-table.md) table stream.</span></span>                             |
| [<span data-ttu-id="81100-123">Benutzerdefinierter Aktionstyp 22</span><span class="sxs-lookup"><span data-stu-id="81100-123">Custom Action Type 22</span></span>](custom-action-type-22.md) | <span data-ttu-id="81100-124">VBScript-Datei, die mit einem Produkt installiert wird.</span><span class="sxs-lookup"><span data-stu-id="81100-124">VBScript file that is installed with a product.</span></span>                                                |
| [<span data-ttu-id="81100-125">Benutzerdefinierter Aktionstyp 54</span><span class="sxs-lookup"><span data-stu-id="81100-125">Custom Action Type 54</span></span>](custom-action-type-54.md) | <span data-ttu-id="81100-126">VBScript-Text, der von einem Eigenschafts Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="81100-126">VBScript text specified by a property value.</span></span>                                                   |
| [<span data-ttu-id="81100-127">Benutzerdefinierter Aktionstyp 38</span><span class="sxs-lookup"><span data-stu-id="81100-127">Custom Action Type 38</span></span>](custom-action-type-38.md) | <span data-ttu-id="81100-128">VBScript-Text, der in der Ziel Spalte der [CustomAction](customaction-table.md) -Tabelle gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="81100-128">VBScript text stored in the Target column of the [CustomAction](customaction-table.md) table.</span></span> |



 

> [!Note]  
> <span data-ttu-id="81100-129">Das Installationsprogramm führt benutzerdefinierte Skript Aktionen direkt aus und verwendet nicht den Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="81100-129">The installer runs script custom actions directly and does not use the Windows Script Host.</span></span> <span data-ttu-id="81100-130">Das **WScript** -Objekt kann nicht in einer benutzerdefinierten Skript Aktion verwendet werden, da dieses Objekt vom Windows Script Host bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="81100-130">The **WScript** object cannot be used inside a script custom action because this object is provided by the Windows Script Host.</span></span> <span data-ttu-id="81100-131">Objekte im Windows Script Host-Objektmodell können nur in benutzerdefinierten Aktionen verwendet werden, wenn Windows Script Host auf dem Computer installiert ist, indem neue Instanzen des-Objekts mit einem Aufrufen von "anateobject" erstellt werden und die ProgID des Objekts (z. b. "Wscript. Shell") bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="81100-131">Objects in the Windows Script Host object model can only be used in custom actions if Windows Script Host is installed on the computer by creating new instances of the object, with a call to CreateObject, and providing the ProgId of the object (for example "WScript.Shell").</span></span> <span data-ttu-id="81100-132">Abhängig vom Typ der benutzerdefinierten Skript Aktion kann der Zugriff auf einige Objekte und Methoden des Windows Script Host-Objektmodells aus Sicherheitsgründen verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="81100-132">Depending on the type of script custom action, access to some objects and methods of the Windows Script Host object model may be denied for security reasons.</span></span>

 

<span data-ttu-id="81100-133">Weitere Informationen finden Sie unter [Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen](summary-list-of-all-custom-action-types.md) für eine Zusammenfassung aller Typen von benutzerdefinierten Aktionen und deren Codierung in die [CustomAction](customaction-table.md) -Tabelle.</span><span class="sxs-lookup"><span data-stu-id="81100-133">For more information, see [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a summary of all types of custom actions and how they are encoded into the [CustomAction](customaction-table.md) table.</span></span>

 

 



