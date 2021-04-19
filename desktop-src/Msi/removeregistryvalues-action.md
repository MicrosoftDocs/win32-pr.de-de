---
description: Mit der removeregistryvalues-Aktion können nur Werte aus der Systemregistrierung entfernt werden, die in der Registrierungs Tabelle oder der Tabelle "removeregistry" erstellt wurden.
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: Removeregistryvalues-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e6e7473be344faa08ed456e72e3b9c80c4aa8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360627"
---
# <a name="removeregistryvalues-action"></a><span data-ttu-id="f9a74-103">Removeregistryvalues-Aktion</span><span class="sxs-lookup"><span data-stu-id="f9a74-103">RemoveRegistryValues Action</span></span>

<span data-ttu-id="f9a74-104">Mit der removeregistryvalues-Aktion können nur Werte aus der Systemregistrierung entfernt werden, die in der [Registrierungs Tabelle](registry-table.md) oder der [Tabelle "removeregistry](removeregistry-table.md)" erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="f9a74-104">The RemoveRegistryValues action can only remove values from the system registry that have been authored into the [Registry table](registry-table.md) or the [RemoveRegistry table](removeregistry-table.md).</span></span> <span data-ttu-id="f9a74-105">Diese Aktion entfernt einen Registrierungs Wert, der in der Registrierungs Tabelle erstellt wurde, wenn die zugeordnete Komponente lokal installiert wurde oder von der Quelle ausgeführt wurde und jetzt deinstalliert wurde.</span><span class="sxs-lookup"><span data-stu-id="f9a74-105">This action removes a registry value that has been authored into the Registry table if the associated component was installed locally or as run from source and is now set to be uninstalled.</span></span> <span data-ttu-id="f9a74-106">Diese Aktion entfernt einen Registrierungs Wert, der in der Tabelle "removeregistry" erstellt wurde, wenn die zugeordnete Komponente so festgelegt ist, dass Sie lokal installiert oder von der Quelle ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9a74-106">This action removes a registry value that has been authored into the RemoveRegistry table if the associated component is set to be installed locally or as run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f9a74-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="f9a74-107">Sequence Restrictions</span></span>

<span data-ttu-id="f9a74-108">Die [InstallValidate](installvalidate-action.md) -Aktion muss vor dem Aufruf von removeregistryvalues aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f9a74-108">The [InstallValidate](installvalidate-action.md) action must be called before calling RemoveRegistryValues.</span></span> <span data-ttu-id="f9a74-109">Wenn eine " [schreiteregistryvalues](writeregistryvalues-action.md) "-Aktion verwendet wird, muss Sie nach "removeregistryvalues" erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f9a74-109">If a [WriteRegistryValues](writeregistryvalues-action.md) action is used, it must come after RemoveRegistryValues.</span></span> <span data-ttu-id="f9a74-110">' Removeregistryvalues ' muss vor ' [unregistermimeinfo](unregistermimeinfo-action.md) ' oder ' [unregisterprogidinfo](unregisterprogidinfo-action.md)' stehen.</span><span class="sxs-lookup"><span data-stu-id="f9a74-110">RemoveRegistryValues must come before [UnregisterMIMEInfo](unregistermimeinfo-action.md) or [UnregisterProgIDInfo](unregisterprogidinfo-action.md).</span></span>

<span data-ttu-id="f9a74-111">Eine benutzerdefinierte Aktion kann verwendet werden, um der [Registrierungs Tabelle](registry-table.md) während einer Installation, einer Neuinstallation oder einer Reparatur Transaktion Zeilen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f9a74-111">A custom action can be used to add rows to the [Registry table](registry-table.md) during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="f9a74-112">Diese Zeilen bleiben in der Registrierungs Tabelle nicht erhalten, und die Informationen sind nur während der aktuellen Transaktion verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f9a74-112">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="f9a74-113">Die benutzerdefinierte Aktion muss daher bei jeder Installation, deinstalstallation oder Reparatur Transaktion ausgeführt werden, die die Informationen in diesen zusätzlichen Zeilen benötigt.</span><span class="sxs-lookup"><span data-stu-id="f9a74-113">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="f9a74-114">Die benutzerdefinierte Aktion muss vor den Aktionen removeregistryvalues und [schreiteregistryvalues](writeregistryvalues-action.md) in der Aktions Sequenz erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f9a74-114">The custom action must come before the RemoveRegistryValues and [WriteRegistryValues](writeregistryvalues-action.md) actions in the action sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f9a74-115">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="f9a74-115">ActionData Messages</span></span>



| <span data-ttu-id="f9a74-116">Feld</span><span class="sxs-lookup"><span data-stu-id="f9a74-116">Field</span></span> | <span data-ttu-id="f9a74-117">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="f9a74-117">Description of action data</span></span>                          |
|-------|-----------------------------------------------------|
| <span data-ttu-id="f9a74-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="f9a74-118">\[1\]</span></span> | <span data-ttu-id="f9a74-119">Der Registrierungs Pfad zum Schlüssel des entfernten Registrierungs Werts.</span><span class="sxs-lookup"><span data-stu-id="f9a74-119">Registry path to key of removed registry value.</span></span>     |
| <span data-ttu-id="f9a74-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="f9a74-120">\[2\]</span></span> | <span data-ttu-id="f9a74-121">Formatierte Zeichenfolge mit dem Namen des entfernten Registrierungs Werts.</span><span class="sxs-lookup"><span data-stu-id="f9a74-121">Formatted string of name of removed registry value.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f9a74-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9a74-122">Remarks</span></span>

<span data-ttu-id="f9a74-123">Notieren Sie den Wert in der Spalte Wert der Registrierungs Tabelle, um einen Registrierungs Wert zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f9a74-123">To remove a registry value, record the value in the Value column of the Registry table.</span></span> <span data-ttu-id="f9a74-124">Wenn die Aktion "beschreiteregistryvalues" reg \_ MultiSZ-Zeichen folgen \_ an den Wert in der [Registrierungs Tabelle](registry-table.md)angehängt hat, entfernt die removeregistryvalues-Aktion nur diese Zeichen folgen aus dem Registrierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="f9a74-124">If the WriteRegistryValues action has attached REG\_MULTI\_SZ strings to the value in the [Registry table](registry-table.md), then the RemoveRegistryValues action removes only those strings from the registry value.</span></span>

 

 



