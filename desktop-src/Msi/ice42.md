---
description: ICE42 überprüft, ob Inproc-Server nicht mit den exe-Dateien in der Klassen Tabelle verknüpft sind. Außerdem wird überprüft, ob nur LocalServer-und LocalServer32-Klassen Argumente und definproc-Werte aufweisen.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe2ea09431870ac7b52ccd69d0ae16c646286ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356253"
---
# <a name="ice42"></a><span data-ttu-id="f02c6-104">ICE42</span><span class="sxs-lookup"><span data-stu-id="f02c6-104">ICE42</span></span>

<span data-ttu-id="f02c6-105">ICE42 überprüft, ob Inproc-Server nicht mit den exe-Dateien in der [Klassen Tabelle](class-table.md)verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="f02c6-105">ICE42 validates that InProc servers are not linked to EXE files in the [Class table](class-table.md).</span></span> <span data-ttu-id="f02c6-106">Außerdem wird überprüft, ob nur LocalServer-und LocalServer32-Klassen Argumente und definproc-Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f02c6-106">It also validates that only LocalServer and LocalServer32 classes have arguments and DefInProc values.</span></span>

## <a name="result"></a><span data-ttu-id="f02c6-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="f02c6-107">Result</span></span>

<span data-ttu-id="f02c6-108">ICE42 gibt einen Fehler aus, wenn in der Klassen Tabelle Inproc-Server mit exe-Dateien verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="f02c6-108">ICE42 posts an error if there are InProc servers linked to EXE files in the Class table.</span></span>

## <a name="example"></a><span data-ttu-id="f02c6-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f02c6-109">Example</span></span>

<span data-ttu-id="f02c6-110">ICE42 würde die folgenden Fehler für das gezeigte Beispiel melden.</span><span class="sxs-lookup"><span data-stu-id="f02c6-110">ICE42 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="f02c6-111">ICE42-Fehler</span><span class="sxs-lookup"><span data-stu-id="f02c6-111">ICE42 error</span></span>                                                                                                                             | <span data-ttu-id="f02c6-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f02c6-112">Description</span></span>                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f02c6-113">Die CLSID "{GUID1}" ist ein Inproc-Server, aber die implementierende Komponente "Component1" hat eine exe-Datei ("test.exe") als Schlüsseldatei.</span><span class="sxs-lookup"><span data-stu-id="f02c6-113">CLSID '{GUID1}' is an InProc server, but the implementing component 'Component1' has an EXE ('test.exe') as its KeyFile.</span></span>                | <span data-ttu-id="f02c6-114">Es gibt eine ausführbare Datei, die als Inproc-Server angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f02c6-114">There is an executable file specified as an InProc server.</span></span> <span data-ttu-id="f02c6-115">EXE-Dateien können keine Inproc-Server sein.</span><span class="sxs-lookup"><span data-stu-id="f02c6-115">EXE files cannot be InProc servers.</span></span>                                                                                                                            |
| <span data-ttu-id="f02c6-116">Die CLSID "{GUID1}" im Kontext "InprocServer32" weist ein Argument auf.</span><span class="sxs-lookup"><span data-stu-id="f02c6-116">CLSID '{GUID1}' in context 'InProcServer32' has an argument.</span></span> <span data-ttu-id="f02c6-117">Nur LocalServer-Kontexte können Argumente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f02c6-117">Only LocalServer contexts can have arguments.</span></span>                              | <span data-ttu-id="f02c6-118">Entfernen Sie das-Argument, um diesen Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="f02c6-118">To fix this error, remove the argument.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="f02c6-119">Die CLSID "{GUID1}" im Kontext "InprocServer32" gibt einen standardmäßigen InProc-Wert an.</span><span class="sxs-lookup"><span data-stu-id="f02c6-119">CLSID '{GUID1}' in context 'InProcServer32' specifies a default InProc value.</span></span> <span data-ttu-id="f02c6-120">Nur LocalServer-Kontexte können standardmäßige INPROC-Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f02c6-120">Only LocalServer contexts can have default InProc values.</span></span> | <span data-ttu-id="f02c6-121">Es gibt ein Objekt mit einem standardmäßigen InProc-Wert, der kein Objekt ist, das in den LocalServer-oder LocalServer32-Kontexten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f02c6-121">There is an object with a default InProc value that is not an object operating in the LocalServer or LocalServer32 contexts.</span></span> <span data-ttu-id="f02c6-122">Entfernen Sie den deflnproc-Wert, oder ändern Sie den Kontext der-Klasse, um diesen Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="f02c6-122">To fix this error, remove the DeflnProc value or change the context of the class.</span></span><br/> |



 

<span data-ttu-id="f02c6-123">[Klassen Tabelle](class-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="f02c6-123">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="f02c6-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="f02c6-124">CLSID</span></span>   | <span data-ttu-id="f02c6-125">Kontext</span><span class="sxs-lookup"><span data-stu-id="f02c6-125">Context</span></span>        | <span data-ttu-id="f02c6-126">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="f02c6-126">Component\_</span></span> | <span data-ttu-id="f02c6-127">Definprochandler</span><span class="sxs-lookup"><span data-stu-id="f02c6-127">DefInProcHandler</span></span> | <span data-ttu-id="f02c6-128">Argument</span><span class="sxs-lookup"><span data-stu-id="f02c6-128">Argument</span></span> |
|---------|----------------|-------------|------------------|----------|
| <span data-ttu-id="f02c6-129">GUID1</span><span class="sxs-lookup"><span data-stu-id="f02c6-129">{GUID1}</span></span> | <span data-ttu-id="f02c6-130">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="f02c6-130">InProcServer32</span></span> | <span data-ttu-id="f02c6-131">Component1</span><span class="sxs-lookup"><span data-stu-id="f02c6-131">Component1</span></span>  | <span data-ttu-id="f02c6-132">InprocServer</span><span class="sxs-lookup"><span data-stu-id="f02c6-132">InProcServer</span></span>     | <span data-ttu-id="f02c6-133">Gebeut</span><span class="sxs-lookup"><span data-stu-id="f02c6-133">Arg</span></span>      |



 

<span data-ttu-id="f02c6-134">[Komponenten Tabelle](component-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="f02c6-134">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="f02c6-135">Komponente</span><span class="sxs-lookup"><span data-stu-id="f02c6-135">Component</span></span>  | <span data-ttu-id="f02c6-136">KEYPATH</span><span class="sxs-lookup"><span data-stu-id="f02c6-136">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="f02c6-137">Component1</span><span class="sxs-lookup"><span data-stu-id="f02c6-137">Component1</span></span> | <span data-ttu-id="f02c6-138">Datei1</span><span class="sxs-lookup"><span data-stu-id="f02c6-138">File1</span></span>   |



 

<span data-ttu-id="f02c6-139">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="f02c6-139">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="f02c6-140">File</span><span class="sxs-lookup"><span data-stu-id="f02c6-140">File</span></span>  | <span data-ttu-id="f02c6-141">Dateiname</span><span class="sxs-lookup"><span data-stu-id="f02c6-141">Filename</span></span> |
|-------|----------|
| <span data-ttu-id="f02c6-142">Datei1</span><span class="sxs-lookup"><span data-stu-id="f02c6-142">File1</span></span> | <span data-ttu-id="f02c6-143">test.exe</span><span class="sxs-lookup"><span data-stu-id="f02c6-143">test.exe</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f02c6-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f02c6-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f02c6-145">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="f02c6-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




