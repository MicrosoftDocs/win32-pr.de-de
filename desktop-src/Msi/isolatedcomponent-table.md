---
description: Jeder Datensatz der isolatedcomponent-Tabelle ordnet die in der Spalte Komponenten Anwendung angegebene Komponente \_ (i. a. exe) der Komponente zu, die in der freigegebenen Spalte der Komponente angegeben ist \_ (häufig eine freigegebene DLL).
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: Isolatedcomponent-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3e6c5bdba6efc546a36e77fa793c0b397f6d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343308"
---
# <a name="isolatedcomponent-table"></a><span data-ttu-id="b0336-103">Isolatedcomponent-Tabelle</span><span class="sxs-lookup"><span data-stu-id="b0336-103">IsolatedComponent Table</span></span>

<span data-ttu-id="b0336-104">Jeder Datensatz der isolatedcomponent-Tabelle ordnet die in der Spalte Komponenten Anwendung angegebene Komponente \_ (i. a. exe) der Komponente zu, die in der freigegebenen Spalte der Komponente angegeben ist \_ (häufig eine freigegebene DLL).</span><span class="sxs-lookup"><span data-stu-id="b0336-104">Each record of the IsolatedComponent table associates the component specified in the Component\_Application column (commonly an .exe) with the component specified in the Component\_Shared column (commonly a shared DLL).</span></span> <span data-ttu-id="b0336-105">Die [isolatecomponents-Aktion](isolatecomponents-action.md) installiert eine Kopie der freigegebenen Komponente an \_ einem privaten Speicherort, der von der Komponenten Anwendung verwendet werden soll \_ .</span><span class="sxs-lookup"><span data-stu-id="b0336-105">The [IsolateComponents action](isolatecomponents-action.md) installs a copy of Component\_Shared into a private location for use by Component\_Application.</span></span> <span data-ttu-id="b0336-106">Dadurch wird die Komponenten \_ Anwendung von anderen Kopien von freigegebenen Komponenten isoliert \_ , die an einem freigegebenen Speicherort auf dem Computer installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="b0336-106">This isolates the Component\_Application from other copies of Component\_Shared that may be installed to a shared location on the computer.</span></span> <span data-ttu-id="b0336-107">Siehe [isolierte Komponenten](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="b0336-107">See [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="b0336-108">Um eine Komponente \_ zu verknüpfen, die mit mehreren Komponenten Anwendungen gemeinsam verwendet \_ wird, fügen Sie für jedes Paar in der isolatedcomponents-Tabelle einen separaten Datensatz ein.</span><span class="sxs-lookup"><span data-stu-id="b0336-108">To link one Component\_Shared to multiple Component\_Application, include a separate record for each pair in the IsolatedComponents table.</span></span> <span data-ttu-id="b0336-109">Das Installationsprogramm kopiert die Dateien der \_ gemeinsam genutzten Komponenten in das Verzeichnis der einzelnen \_ installierten Komponenten Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="b0336-109">The installer copies the files of Component\_Shared into the directory of each Component\_Application that is installed.</span></span>

<span data-ttu-id="b0336-110">Die isolatedcomponent-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="b0336-110">The IsolatedComponent table has the following columns.</span></span>



| <span data-ttu-id="b0336-111">Spalte</span><span class="sxs-lookup"><span data-stu-id="b0336-111">Column</span></span>                 | <span data-ttu-id="b0336-112">Typ</span><span class="sxs-lookup"><span data-stu-id="b0336-112">Type</span></span>                         | <span data-ttu-id="b0336-113">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b0336-113">Key</span></span> | <span data-ttu-id="b0336-114">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="b0336-114">Nullable</span></span> |
|------------------------|------------------------------|-----|----------|
| <span data-ttu-id="b0336-115">Frei \_ gegebene Komponente</span><span class="sxs-lookup"><span data-stu-id="b0336-115">Component\_Shared</span></span>      | [<span data-ttu-id="b0336-116">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b0336-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="b0336-117">J</span><span class="sxs-lookup"><span data-stu-id="b0336-117">Y</span></span>   | <span data-ttu-id="b0336-118">N</span><span class="sxs-lookup"><span data-stu-id="b0336-118">N</span></span>        |
| <span data-ttu-id="b0336-119">Komponenten \_ Anwendung</span><span class="sxs-lookup"><span data-stu-id="b0336-119">Component\_Application</span></span> | [<span data-ttu-id="b0336-120">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b0336-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="b0336-121">J</span><span class="sxs-lookup"><span data-stu-id="b0336-121">Y</span></span>   | <span data-ttu-id="b0336-122">N</span><span class="sxs-lookup"><span data-stu-id="b0336-122">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b0336-123">Spalten</span><span class="sxs-lookup"><span data-stu-id="b0336-123">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b0336-124"><span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Frei \_ gegebene Komponente</span><span class="sxs-lookup"><span data-stu-id="b0336-124"><span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Component\_Shared</span></span>
</dt> <dd>

<span data-ttu-id="b0336-125">Fremdschlüssel in der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="b0336-125">Foreign key into the [Component table](component-table.md).</span></span> <span data-ttu-id="b0336-126">Die Komponente, die die freigegebene Datei enthält, normalerweise eine DLL.</span><span class="sxs-lookup"><span data-stu-id="b0336-126">The component that contains the shared file, usually a DLL.</span></span> <span data-ttu-id="b0336-127">Die dll sollte die Schlüsseldatei für diese Komponente sein.</span><span class="sxs-lookup"><span data-stu-id="b0336-127">The DLL should be the key file for this component.</span></span> <span data-ttu-id="b0336-128">Dabei muss es sich um eine andere Komponente handeln als in der \_ Spalte Komponenten Anwendung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0336-128">This must be a different component than listed in the Component\_Application column.</span></span>

<span data-ttu-id="b0336-129">Die freigegebene Komponente steuert die Registrierung für alle isolierten Kopien der Komponente, und das Flag " **msidbcomponentattributesshareddllrefcount** " muss in der Spalte Attribute der Komponenten Tabelle festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="b0336-129">The shared component controls the registration for all the isolated copies of the component and must have the **msidbComponentAttributesSharedDllRefCount** flag set in the Attributes column of the Component table.</span></span> <span data-ttu-id="b0336-130">Dadurch wird sichergestellt, dass das Installationsprogramm die Lebensdauer der freigegebenen Komponente verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="b0336-130">This ensures that the installer can manage the life of the shared component.</span></span>

</dd> <dt>

<span data-ttu-id="b0336-131"><span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Komponenten \_ Anwendung</span><span class="sxs-lookup"><span data-stu-id="b0336-131"><span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Component\_Application</span></span>
</dt> <dd>

<span data-ttu-id="b0336-132">Fremdschlüssel in der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="b0336-132">Foreign key into the [Component table](component-table.md).</span></span> <span data-ttu-id="b0336-133">Die Komponente mit der exe-Datei, die die freigegebene Datei lädt.</span><span class="sxs-lookup"><span data-stu-id="b0336-133">The component that contains the .exe which loads the shared file.</span></span> <span data-ttu-id="b0336-134">Die exe-Datei sollte die Schlüsseldatei für diese Komponente sein.</span><span class="sxs-lookup"><span data-stu-id="b0336-134">The .exe should be the key file for this component.</span></span> <span data-ttu-id="b0336-135">Dabei muss es sich um eine andere Komponente handeln als in der freigegebenen Spalte der Komponente aufgeführt \_ .</span><span class="sxs-lookup"><span data-stu-id="b0336-135">This must be a different component than listed in the Component\_Shared column.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="b0336-136">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="b0336-136">Validation</span></span>

<dl>

[<span data-ttu-id="b0336-137">ICE03</span><span class="sxs-lookup"><span data-stu-id="b0336-137">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b0336-138">ICE06</span><span class="sxs-lookup"><span data-stu-id="b0336-138">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b0336-139">ICE32</span><span class="sxs-lookup"><span data-stu-id="b0336-139">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="b0336-140">ICE62</span><span class="sxs-lookup"><span data-stu-id="b0336-140">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="b0336-141">ICE66</span><span class="sxs-lookup"><span data-stu-id="b0336-141">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="b0336-142">ICE97</span><span class="sxs-lookup"><span data-stu-id="b0336-142">ICE97</span></span>](ice97.md)  
</dl>

 

 



