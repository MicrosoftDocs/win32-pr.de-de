---
description: Die Registrierung ist eine hierarchische Datenbank, die Daten enthält, die für den Betrieb von Windows und die unter Windows ausgeführten Anwendungen und Dienste von entscheidender Bedeutung sind.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Struktur der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf104806b5e4e10b4be7387018e714a0db8bf37
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386669"
---
# <a name="structure-of-the-registry"></a><span data-ttu-id="0bd1f-103">Struktur der Registrierung</span><span class="sxs-lookup"><span data-stu-id="0bd1f-103">Structure of the Registry</span></span>

<span data-ttu-id="0bd1f-104">Die Registrierung ist eine hierarchische Datenbank, die Daten enthält, die für den Betrieb von Windows und die unter Windows ausgeführten Anwendungen und Dienste von entscheidender Bedeutung sind.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-104">The registry is a hierarchical database that contains data that is critical for the operation of Windows and the applications and services that run on Windows.</span></span> <span data-ttu-id="0bd1f-105">Die Daten sind in einem Strukturformat strukturiert.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-105">The data is structured in a tree format.</span></span> <span data-ttu-id="0bd1f-106">Jeder Knoten in der Struktur wird als Schlüssel *bezeichnet.*</span><span class="sxs-lookup"><span data-stu-id="0bd1f-106">Each node in the tree is called a *key*.</span></span> <span data-ttu-id="0bd1f-107">Jeder Schlüssel kann sowohl Unterschlüssel *als auch* Dateneinträge enthalten, die als Werte *bezeichnet werden.*</span><span class="sxs-lookup"><span data-stu-id="0bd1f-107">Each key can contain both *subkeys* and data entries called *values*.</span></span> <span data-ttu-id="0bd1f-108">Manchmal sind alle Daten, die eine Anwendung benötigt, das Vorhandensein eines Schlüssels. in anderen Zeiten öffnet eine Anwendung einen Schlüssel und verwendet die dem Schlüssel zugeordneten Werte.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-108">Sometimes, the presence of a key is all the data that an application requires; other times, an application opens a key and uses the values associated with the key.</span></span> <span data-ttu-id="0bd1f-109">Ein Schlüssel kann eine beliebige Anzahl von Werten enthalten, und die Werte können in beliebiger Form sein.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-109">A key can have any number of values, and the values can be in any form.</span></span> <span data-ttu-id="0bd1f-110">Weitere Informationen finden Sie unter [Registrierungswerttypen und](registry-value-types.md) [Größenbeschränkungen für Registrierungselemente.](registry-element-size-limits.md)</span><span class="sxs-lookup"><span data-stu-id="0bd1f-110">For more information, see [Registry Value Types](registry-value-types.md) and [Registry Element Size Limits](registry-element-size-limits.md).</span></span>

<span data-ttu-id="0bd1f-111">Jeder Schlüssel hat einen Namen, der aus mindestens einem druckbaren Zeichen besteht.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-111">Each key has a name consisting of one or more printable characters.</span></span> <span data-ttu-id="0bd1f-112">Bei Schlüsselnamen wird die Schreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-112">Key names are not case sensitive.</span></span> <span data-ttu-id="0bd1f-113">Schlüsselnamen dürfen nicht den schrägen Schrägstrich () enthalten, es können jedoch \\ beliebige andere druckbare Zeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-113">Key names cannot include the backslash character (\\), but any other printable character can be used.</span></span> <span data-ttu-id="0bd1f-114">Wertnamen und Daten können den schrägen Schrägstrich enthalten.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-114">Value names and data can include the backslash character.</span></span>

<span data-ttu-id="0bd1f-115">Der Name jedes Unterschlüssels ist in Bezug auf den Schlüssel, der sich direkt darüber in der Hierarchie befindet, eindeutig.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-115">The name of each subkey is unique with respect to the key that is immediately above it in the hierarchy.</span></span> <span data-ttu-id="0bd1f-116">Schlüsselnamen werden nicht in andere Sprachen lokalisiert, obwohl Werte sein können.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-116">Key names are not localized into other languages, although values may be.</span></span>

<span data-ttu-id="0bd1f-117">Die folgende Abbildung zeigt eine Beispielstruktur für Registrierungsschlüssel, die vom Registrierungs-Editor angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-117">The following illustration is an example registry key structure as displayed by the Registry Editor.</span></span>

![Fenster "Registrierungs-Editor"](images/regtree.png)

<span data-ttu-id="0bd1f-119">Jede der Strukturen unter **Arbeitsplatz** ist ein Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-119">Each of the trees under **My Computer** is a key.</span></span> <span data-ttu-id="0bd1f-120">Der **HKEY \_ LOCAL \_ MACHINE-Schlüssel** verfügt über die folgenden Unterschlüssel: **HARDWARE,** **SAM,** **SECURITY,** **SOFTWARE** und **SYSTEM**.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-120">The **HKEY\_LOCAL\_MACHINE** key has the following subkeys: **HARDWARE**, **SAM**, **SECURITY**, **SOFTWARE**, and **SYSTEM**.</span></span> <span data-ttu-id="0bd1f-121">Jeder dieser Schlüssel verfügt wiederum über Unterschlüssel.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-121">Each of these keys in turn has subkeys.</span></span> <span data-ttu-id="0bd1f-122">Beispielsweise verfügt der **HARDWARE-Schlüssel** über die Unterschlüssel **DESCRIPTION,** **DEVICEMAP** und **RESOURCEMAP.** Der **DEVICEMAP-Schlüssel** verfügt über mehrere Unterschlüssel, einschließlich **VIDEO**.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-122">For example, the **HARDWARE** key has the subkeys **DESCRIPTION**, **DEVICEMAP**, and **RESOURCEMAP**; the **DEVICEMAP** key has several subkeys including **VIDEO**.</span></span>

<span data-ttu-id="0bd1f-123">Jeder Wert besteht aus einem Wertnamen und den zugehörigen Daten(sofern möglich).</span><span class="sxs-lookup"><span data-stu-id="0bd1f-123">Each value consists of a value name and its associated data, if any.</span></span> <span data-ttu-id="0bd1f-124">**MaxObjectNumber und** **VgaCompatible sind** Werte, die Daten unter dem **Unterschlüssel VIDEO** enthalten.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-124">**MaxObjectNumber** and **VgaCompatible** are values that contain data under the **VIDEO** subkey.</span></span>

<span data-ttu-id="0bd1f-125">Eine Registrierungsstruktur kann 512 Ebenen tief sein.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-125">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="0bd1f-126">Sie können bis zu 32 Ebenen gleichzeitig über einen einzelnen Registrierungs-API-Aufruf erstellen.</span><span class="sxs-lookup"><span data-stu-id="0bd1f-126">You can create up to 32 levels at a time through a single registry API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bd1f-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0bd1f-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0bd1f-128">[Übersicht über die Windows-Registrierung](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="0bd1f-128">[Overview of the Windows Registry](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span></span>
</dt> </dl>

 

 
