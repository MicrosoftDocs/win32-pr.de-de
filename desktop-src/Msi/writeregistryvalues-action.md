---
description: Die Aktion "beschreiteregistryvalues" richtet die Registrierungsinformationen einer Anwendung ein.
ms.assetid: ab121de3-f07d-401a-b52a-246a555c142c
title: Schreibegistryvalues-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13cc5cf5a817e44caa34b9084115b7dda8cee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349482"
---
# <a name="writeregistryvalues-action"></a><span data-ttu-id="30322-103">Schreibegistryvalues-Aktion</span><span class="sxs-lookup"><span data-stu-id="30322-103">WriteRegistryValues Action</span></span>

<span data-ttu-id="30322-104">Die Aktion "beschreiteregistryvalues" richtet die Registrierungsinformationen einer Anwendung ein.</span><span class="sxs-lookup"><span data-stu-id="30322-104">The WriteRegistryValues action sets up an application's registry information.</span></span> <span data-ttu-id="30322-105">Die Registrierungsinformationen werden von der [Komponenten Tabelle](component-table.md)abgegrenzt.</span><span class="sxs-lookup"><span data-stu-id="30322-105">The registry information is gated by the [Component table](component-table.md).</span></span> <span data-ttu-id="30322-106">Ein Registrierungs Wert wird in die Registrierung geschrieben, wenn die entsprechende Komponente so festgelegt wurde, dass Sie entweder lokal oder als von der Quelle ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="30322-106">A registry value is written to the registry if the corresponding component has been set to be installed either locally or as run from source.</span></span> <span data-ttu-id="30322-107">Weitere Informationen finden Sie unter [Registry Table](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="30322-107">For more information, see [Registry table](registry-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="30322-108">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="30322-108">Sequence Restrictions</span></span>

<span data-ttu-id="30322-109">Die [InstallValidate-Aktion](installvalidate-action.md) muss vor der Aktion "beschreiteregistryvalues" erfolgen.</span><span class="sxs-lookup"><span data-stu-id="30322-109">The [InstallValidate action](installvalidate-action.md) must come before the WriteRegistryValues action.</span></span> <span data-ttu-id="30322-110">Wenn eine [removeregistryvalues-Aktion](removeregistryvalues-action.md)vorhanden ist, muss Sie vor der Aktion "schreiteregistryvalues" stehen.</span><span class="sxs-lookup"><span data-stu-id="30322-110">If there is a [RemoveRegistryValues action](removeregistryvalues-action.md), then it must come before the WriteRegistryValues action.</span></span>

<span data-ttu-id="30322-111">Eine benutzerdefinierte Aktion kann verwendet werden, um der [Registrierungs Tabelle](registry-table.md) während einer Installation, einer Neuinstallation oder einer Reparatur Transaktion Zeilen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="30322-111">A custom action can be used to add rows to the [Registry table](registry-table.md) during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="30322-112">Diese Zeilen bleiben in der Registrierungs Tabelle nicht erhalten, und die Informationen sind nur während der aktuellen Transaktion verfügbar.</span><span class="sxs-lookup"><span data-stu-id="30322-112">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="30322-113">Die benutzerdefinierte Aktion muss daher bei jeder Installation, deinstalstallation oder Reparatur Transaktion ausgeführt werden, die die Informationen in diesen zusätzlichen Zeilen benötigt.</span><span class="sxs-lookup"><span data-stu-id="30322-113">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="30322-114">Die benutzerdefinierte Aktion muss vor den Aktionen [removeregistryvalues](removeregistryvalues-action.md) und schreiteregistryvalues in der Aktions Sequenz erfolgen.</span><span class="sxs-lookup"><span data-stu-id="30322-114">The custom action must come before the [RemoveRegistryValues](removeregistryvalues-action.md) and WriteRegistryValues actions in the action sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="30322-115">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="30322-115">ActionData Messages</span></span>



| <span data-ttu-id="30322-116">Feld</span><span class="sxs-lookup"><span data-stu-id="30322-116">Field</span></span> | <span data-ttu-id="30322-117">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="30322-117">Description of action data</span></span>                               |
|-------|----------------------------------------------------------|
| <span data-ttu-id="30322-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="30322-118">\[1\]</span></span> | <span data-ttu-id="30322-119">Der Pfad zum Registrierungsschlüssel des Werts, der in die Registrierung geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="30322-119">Path to registry key of value written to registry.</span></span>       |
| <span data-ttu-id="30322-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="30322-120">\[2\]</span></span> | <span data-ttu-id="30322-121">Formatierter Textzeichen folgen Name des in die Registrierung geschriebenen Werts.</span><span class="sxs-lookup"><span data-stu-id="30322-121">Formatted text string name of value written to registry.</span></span> |
| <span data-ttu-id="30322-122">\[3\]</span><span class="sxs-lookup"><span data-stu-id="30322-122">\[3\]</span></span> | <span data-ttu-id="30322-123">Formatierte Text Zeichenfolge des in die Registrierung geschriebenen Werts.</span><span class="sxs-lookup"><span data-stu-id="30322-123">Formatted text string of value written to registry.</span></span>      |



 

 

 



