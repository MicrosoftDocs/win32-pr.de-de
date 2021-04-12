---
description: Die isolatecomponents-Aktion installiert eine Kopie einer Komponente (in der Regel eine freigegebene DLL) an einem privaten Speicherort, der von einer bestimmten Anwendung (i. a. exe) verwendet wird.
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: Isolatecomponents-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fe36f8c30e67591662ca2fce6c0b0ac2150ebb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348979"
---
# <a name="isolatecomponents-action"></a><span data-ttu-id="00a78-103">Isolatecomponents-Aktion</span><span class="sxs-lookup"><span data-stu-id="00a78-103">IsolateComponents Action</span></span>

<span data-ttu-id="00a78-104">Die isolatecomponents-Aktion installiert eine Kopie einer Komponente (in der Regel eine freigegebene DLL) an einem privaten Speicherort, der von einer bestimmten Anwendung (i. a. exe) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00a78-104">The IsolateComponents action installs a copy of a component (commonly a shared DLL) into a private location for use by a specific application (typically an .exe).</span></span> <span data-ttu-id="00a78-105">Dadurch wird die Anwendung von anderen Kopien der Komponente isoliert, die möglicherweise an einem freigegebenen Speicherort auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="00a78-105">This isolates the application from other copies of the component that may be installed to a shared location on the computer.</span></span> <span data-ttu-id="00a78-106">Weitere Informationen finden Sie unter [isolierte Komponenten](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="00a78-106">For more information, see [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="00a78-107">Die Aktion bezieht sich auf jeden Datensatz der [isolatedcomponent-Tabelle](isolatedcomponent-table.md) und ordnet die Dateien der Komponente, die im Feld für die freigegebene Komponente aufgeführt sind, der Komponente zu, die \_ im Feld Komponenten Anwendung aufgelistet ist \_ .</span><span class="sxs-lookup"><span data-stu-id="00a78-107">The action refers to each record of the [IsolatedComponent table](isolatedcomponent-table.md) and associates the files of the component listed in the Component\_Shared field with the component listed in the Component\_Application field.</span></span> <span data-ttu-id="00a78-108">Das Installationsprogramm installiert die Dateien der-Komponente, die \_ in demselben Verzeichnis wie die Komponenten Anwendung freigegeben werden \_ .</span><span class="sxs-lookup"><span data-stu-id="00a78-108">The installer installs the files of Component\_Shared into the same directory as Component\_Application.</span></span> <span data-ttu-id="00a78-109">Das Installationsprogramm generiert eine Datei in diesem Verzeichnis mit einer Länge von 0 (null) Bytes, wobei der kurze Dateiname der Schlüsseldatei für die Komponenten \_ Anwendung (in der Regel der Dateiname der exe-Datei) mit dem Namen. local vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="00a78-109">The installer generates a file in this directory, zero bytes in length, having the short filename name of the key file for Component\_Application (typically this is the same file name as the .exe) appended with .local.</span></span> <span data-ttu-id="00a78-110">Die isolatedcomponent-Aktion wirkt sich nicht auf die Installation der Komponenten \_ Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="00a78-110">The IsolatedComponent action does not affect the installation of Component\_Application.</span></span> <span data-ttu-id="00a78-111">Beim Deinstallieren \_ der Komponenten Anwendung werden auch die frei \_ gegebenen Komponenten Dateien und die lokale Datei aus dem Verzeichnis entfernt.</span><span class="sxs-lookup"><span data-stu-id="00a78-111">Uninstalling Component\_Application also removes the Component\_Shared files and the .local file from the directory.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="00a78-112">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="00a78-112">Sequence Restrictions</span></span>

<span data-ttu-id="00a78-113">Die isolatecomponents-Aktion kann nur in der Tabelle [InstallUISequence](installuisequence-table.md) und in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00a78-113">The IsolateComponents action can be used only in the [InstallUISequence table](installuisequence-table.md) and the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="00a78-114">Diese Aktion muss nach der [Aktion "costinitialize](costinitialize-action.md) " und vor der [Aktion "costfinalize](costfinalize-action.md)" erfolgen.</span><span class="sxs-lookup"><span data-stu-id="00a78-114">This action must come after the [CostInitialize action](costinitialize-action.md) and before the [CostFinalize action](costfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="00a78-115">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="00a78-115">ActionData Messages</span></span>

<span data-ttu-id="00a78-116">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="00a78-116">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="00a78-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00a78-117">Remarks</span></span>

<span data-ttu-id="00a78-118">Wenn die Spalte Bedingung für die isolatecomponents-Aktion als true ausgewertet wird oder leer gelassen wird, isoliert das Installationsprogramm alle in der [isolatedcomponent-Tabelle](isolatedcomponent-table.md)aufgeführten Komponenten.</span><span class="sxs-lookup"><span data-stu-id="00a78-118">If the Condition column for the IsolateComponents action evaluates to True, or is left blank, the installer isolates all the components listed in the [IsolatedComponent table](isolatedcomponent-table.md).</span></span> <span data-ttu-id="00a78-119">Wenn die Spalte Bedingung als false ausgewertet wird, wird die isolatedcomponent-Tabelle vom Installationsprogramm ignoriert, und die Komponenten werden normalerweise gemeinsam freigelegt.</span><span class="sxs-lookup"><span data-stu-id="00a78-119">If the Condition column evaluates to False, the installer ignores the IsolatedComponent table and shares the components usual.</span></span> <span data-ttu-id="00a78-120">Die [**redirecteddllsupport**](redirecteddllsupport.md) -Eigenschaft kann verwendet werden, um diese Aktion zu bedinieren.</span><span class="sxs-lookup"><span data-stu-id="00a78-120">The [**RedirectedDllSupport**](redirecteddllsupport.md) property may be used to condition this action.</span></span> <span data-ttu-id="00a78-121">Weitere Informationen finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="00a78-121">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



