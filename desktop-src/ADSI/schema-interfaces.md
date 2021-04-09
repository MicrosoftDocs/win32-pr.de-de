---
title: Schema Schnittstellen
description: Schema Schnittstellen
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- Schema Schnittstellen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f414fdea2418fb92a0a3c8c9e8bf88eb6d7f00b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947333"
---
# <a name="schema-interfaces"></a><span data-ttu-id="efa9a-104">Schema Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="efa9a-104">Schema Interfaces</span></span>

<span data-ttu-id="efa9a-105">Der Schema Container enthält einen Satz von Schema Definitionen, die an einen Teil der Namespace Struktur des Anbieters angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="efa9a-105">The schema container contains a set of schema definitions that are attached to part of the namespace tree of the provider.</span></span> <span data-ttu-id="efa9a-106">In der Regel verfügt jede Instanz eines Namespace über ein eigenes Schema.</span><span class="sxs-lookup"><span data-stu-id="efa9a-106">Typically, each instance of a namespace has its own schema.</span></span> <span data-ttu-id="efa9a-107">In der folgenden Abbildung definiert z. b. der ADSI-Beispiel Anbieter einen Schema Container in jedem der Stamm Knoten "Seattle" und "Toronto".</span><span class="sxs-lookup"><span data-stu-id="efa9a-107">For example, in the following figure, the ADSI example provider defines a schema container in each of the root nodes "Seattle" and "Toronto".</span></span>

![Schema Kapselung](images/schemacont.png)

<span data-ttu-id="efa9a-109">Zum Erstellen einer ADSI-Implementierung für einen Anbieter müssen Sie Schema Verwaltungs Objekte bereitstellen, die den zugrunde liegenden Namespace des Anbieters widerspiegeln und die ADSI-Schema Schnittstellen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="efa9a-109">To create an ADSI implementation for a provider, you need to supply schema management objects that reflect the underlying namespace of the provider and which support ADSI schema interfaces.</span></span> <span data-ttu-id="efa9a-110">Im folgenden finden Sie eine Liste der ADSI-Schema Schnittstellen, die im Schema Container enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="efa9a-110">The following is a list of the ADSI schema interfaces, which are contained in the schema container.</span></span>

-   <span data-ttu-id="efa9a-111">[**Iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) stellt Verzeichnisdienst Klassen dar.</span><span class="sxs-lookup"><span data-stu-id="efa9a-111">[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) represents directory service classes.</span></span>
-   <span data-ttu-id="efa9a-112">[**Iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) stellt Verzeichnisdienst Eigenschaften mit einzelnen oder mehreren Werten dar.</span><span class="sxs-lookup"><span data-stu-id="efa9a-112">[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) represents directory service properties that have single or multiple values.</span></span>
-   <span data-ttu-id="efa9a-113">[**Iadssyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) stellt den einzelnen Variant-Typ dar.</span><span class="sxs-lookup"><span data-stu-id="efa9a-113">[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) represents the single VARIANT type.</span></span>

<span data-ttu-id="efa9a-114">Von ADSI definierte Schnittstellen können bestimmte Eigenschaften und Syntaxen für Ihren Anbieter unterstützen.</span><span class="sxs-lookup"><span data-stu-id="efa9a-114">Interfaces defined by ADSI can support specific properties and syntaxes for your provider.</span></span> <span data-ttu-id="efa9a-115">Anbieter können eine ADSI-Definition mithilfe der Methoden erweitern, die Eigenschaften erstellen und aufrufen. Sie können z. b. die Methoden der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle verwenden, z. b. [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) und [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex).</span><span class="sxs-lookup"><span data-stu-id="efa9a-115">Providers can choose to extend an ADSI definition by using the methods that create and access properties, for example, you can use the methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface such as [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex).</span></span> <span data-ttu-id="efa9a-116">Anbieter können zusätzliche Eigenschaften auch über zusätzliche Schnittstellen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="efa9a-116">Providers can also support additional properties through additional interfaces.</span></span> <span data-ttu-id="efa9a-117">Eine umfassende Liste der ADSI-Schnittstellen finden Sie unter [ADSI-Schnittstellen](adsi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="efa9a-117">For a complete list of ADSI interfaces, see [ADSI Interfaces](adsi-interfaces.md).</span></span>

<span data-ttu-id="efa9a-118">Eine ADSI-Anbieter Komponente mit einem komplexen Namespace kann möglicherweise mehrere Schemas in einer Namespace Instanz enthalten, die jeweils in einem anderen Teil der Struktur vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="efa9a-118">An ADSI provider component with a complex namespace might allow multiple schemas to exist in a namespace instance, each at a different part of the tree.</span></span> <span data-ttu-id="efa9a-119">Die [**IADs:: Schema**](iads-property-methods.md) -Eigenschaft eines Objekts benennt jedoch immer seine eigene Schema Definition.</span><span class="sxs-lookup"><span data-stu-id="efa9a-119">The [**IADs::Schema**](iads-property-methods.md) property of an object, however, always names its own schema definition.</span></span>

 

 




