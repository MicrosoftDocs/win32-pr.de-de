---
description: Die Registrierung ist eine hierarchische Datenbank, die Daten enthält, die für den Betrieb von Windows und die Anwendungen und Dienste, die unter Windows ausgeführt werden, wichtig sind.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Struktur der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b76b7f827ae3ea96d75d089c7d874c3d31d030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555543"
---
# <a name="structure-of-the-registry"></a><span data-ttu-id="39732-103">Struktur der Registrierung</span><span class="sxs-lookup"><span data-stu-id="39732-103">Structure of the Registry</span></span>

<span data-ttu-id="39732-104">Die Registrierung ist eine hierarchische Datenbank, die Daten enthält, die für den Betrieb von Windows und die Anwendungen und Dienste, die unter Windows ausgeführt werden, wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="39732-104">The registry is a hierarchical database that contains data that is critical for the operation of Windows and the applications and services that run on Windows.</span></span> <span data-ttu-id="39732-105">Die Daten sind in einem Struktur Format strukturiert.</span><span class="sxs-lookup"><span data-stu-id="39732-105">The data is structured in a tree format.</span></span> <span data-ttu-id="39732-106">Jeder Knoten in der Struktur wird als *Schlüssel* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="39732-106">Each node in the tree is called a *key*.</span></span> <span data-ttu-id="39732-107">Jeder Schlüssel kann sowohl *Unterschlüssel* als auch Dateneinträge mit dem Namen *Values* enthalten.</span><span class="sxs-lookup"><span data-stu-id="39732-107">Each key can contain both *subkeys* and data entries called *values*.</span></span> <span data-ttu-id="39732-108">Manchmal handelt es sich bei dem vorhanden sein eines Schlüssels um alle Daten, die für eine Anwendung erforderlich sind. in anderen Zeiten öffnet eine Anwendung einen Schlüssel und verwendet die Werte, die dem Schlüssel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="39732-108">Sometimes, the presence of a key is all the data that an application requires; other times, an application opens a key and uses the values associated with the key.</span></span> <span data-ttu-id="39732-109">Ein Schlüssel kann eine beliebige Anzahl von Werten aufweisen, und die Werte können in beliebiger Form vorliegen.</span><span class="sxs-lookup"><span data-stu-id="39732-109">A key can have any number of values, and the values can be in any form.</span></span> <span data-ttu-id="39732-110">Weitere Informationen finden Sie unter [Registrierungs Werttypen](registry-value-types.md) und [Größenbeschränkungen für Registrierungs Elemente](registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="39732-110">For more information, see [Registry Value Types](registry-value-types.md) and [Registry Element Size Limits](registry-element-size-limits.md).</span></span>

<span data-ttu-id="39732-111">Jeder Schlüssel weist einen Namen auf, der aus einem oder mehreren druckbaren Zeichen besteht.</span><span class="sxs-lookup"><span data-stu-id="39732-111">Each key has a name consisting of one or more printable characters.</span></span> <span data-ttu-id="39732-112">Bei Schlüsselnamen wird Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="39732-112">Key names are not case sensitive.</span></span> <span data-ttu-id="39732-113">Schlüsselnamen dürfen keinen umgekehrten Schrägstrich enthalten ( \) , es kann jedoch ein beliebiges anderes druckbares Zeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39732-113">Key names cannot include the backslash character (\), but any other printable character can be used.</span></span> <span data-ttu-id="39732-114">Wertnamen und-Daten können den umgekehrten Schrägstrich enthalten.</span><span class="sxs-lookup"><span data-stu-id="39732-114">Value names and data can include the backslash character.</span></span>

<span data-ttu-id="39732-115">Der Name jedes unter Schlüssels ist in Bezug auf den Schlüssel, der sich direkt oberhalb des Schlüssels in der Hierarchie befindet, eindeutig.</span><span class="sxs-lookup"><span data-stu-id="39732-115">The name of each subkey is unique with respect to the key that is immediately above it in the hierarchy.</span></span> <span data-ttu-id="39732-116">Schlüsselnamen sind nicht in anderen Sprachen lokalisiert, auch wenn die Werte lauten.</span><span class="sxs-lookup"><span data-stu-id="39732-116">Key names are not localized into other languages, although values may be.</span></span>

<span data-ttu-id="39732-117">Die folgende Abbildung ist ein Beispiel für eine Registrierungsschlüssel Struktur, die im Registrierungs-Editor angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="39732-117">The following illustration is an example registry key structure as displayed by the Registry Editor.</span></span>

![Fenster des Registrierungs-Editors](images/regtree.png)

<span data-ttu-id="39732-119">Jede Struktur unter **Arbeitsplatz** ist ein Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="39732-119">Each of the trees under **My Computer** is a key.</span></span> <span data-ttu-id="39732-120">Der Schlüssel **des \_ lokalen \_ HKEY** -Computers verfügt über die folgenden Unterschlüssel: **Hardware**, **Sam**, **Security**, **Software** und **System**.</span><span class="sxs-lookup"><span data-stu-id="39732-120">The **HKEY\_LOCAL\_MACHINE** key has the following subkeys: **HARDWARE**, **SAM**, **SECURITY**, **SOFTWARE**, and **SYSTEM**.</span></span> <span data-ttu-id="39732-121">Alle diese Schlüssel haben wiederum Unterschlüssel.</span><span class="sxs-lookup"><span data-stu-id="39732-121">Each of these keys in turn has subkeys.</span></span> <span data-ttu-id="39732-122">Der **Hardware** Schlüssel weist beispielsweise die Unterschlüssel **Beschreibung**, **DeviceMap** und **ResourceMap** auf. der **DeviceMap** -Schlüssel verfügt über mehrere Unterschlüssel, einschließlich **Video**.</span><span class="sxs-lookup"><span data-stu-id="39732-122">For example, the **HARDWARE** key has the subkeys **DESCRIPTION**, **DEVICEMAP**, and **RESOURCEMAP**; the **DEVICEMAP** key has several subkeys including **VIDEO**.</span></span>

<span data-ttu-id="39732-123">Jeder Wert besteht aus einem Wertnamen und den zugehörigen Daten, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="39732-123">Each value consists of a value name and its associated data, if any.</span></span> <span data-ttu-id="39732-124">" **Maxobjectnumber** " und " **vgacompatible** " sind Werte, die Daten unter dem **Video** Unterschlüssel enthalten.</span><span class="sxs-lookup"><span data-stu-id="39732-124">**MaxObjectNumber** and **VgaCompatible** are values that contain data under the **VIDEO** subkey.</span></span>

<span data-ttu-id="39732-125">Eine Registrierungs Struktur kann 512 Ebenen tief sein.</span><span class="sxs-lookup"><span data-stu-id="39732-125">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="39732-126">Sie können bis zu 32 Ebenen gleichzeitig über einen einzigen Registrierungs-API-Aufruf erstellen.</span><span class="sxs-lookup"><span data-stu-id="39732-126">You can create up to 32 levels at a time through a single registry API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39732-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39732-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="39732-128">[Übersicht über die Windows-Registrierung](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="39732-128">[Overview of the Windows Registry](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span></span>
</dt> </dl>

 

 
