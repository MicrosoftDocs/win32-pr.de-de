---
description: Com+-objektkonstruktorzeichenfolgen sind Initialisierungs Zeichenfolgen, die für eine Komponente administrativ angegeben werden.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Konzepte der com+-objektkonstruktorzeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32bffd35ad230efe1f22b52da10e1b4910d71da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958276"
---
# <a name="com-object-constructor-strings-concepts"></a><span data-ttu-id="2d939-103">Konzepte der com+-objektkonstruktorzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="2d939-103">COM+ Object Constructor Strings Concepts</span></span>

<span data-ttu-id="2d939-104">Com+-objektkonstruktorzeichenfolgen sind Initialisierungs Zeichenfolgen, die für eine Komponente administrativ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2d939-104">COM+ object constructor strings are initialization strings that are administratively specified for a component.</span></span> <span data-ttu-id="2d939-105">Sie können objektkonstruktorzeichenfolgen verwenden, um eine einzelne Komponente mit einem gewissen Grad an Generalität zu schreiben, der es Ihnen ermöglicht, später für eine bestimmte Aufgabe angepasst zu werden. Das heißt, Sie können die parametrisierte Objekt Erstellung durchführen.</span><span class="sxs-lookup"><span data-stu-id="2d939-105">You can use object constructor strings to write a single component with a degree of generality that allows it to be later customized for a particular task; that is, you can perform parameterized object construction.</span></span>

<span data-ttu-id="2d939-106">Beispielsweise können Sie diese Funktion verwenden, um eine Komponente zu schreiben, die eine generische ODBC-Verbindung enthält, und später einen exakten DSN für die Komponente in administrativer Weise angeben.</span><span class="sxs-lookup"><span data-stu-id="2d939-106">For example, you might use this feature to write a component that holds a generic ODBC connection and later specify an exact DSN for the component administratively.</span></span> <span data-ttu-id="2d939-107">Wenn sich die Systemkonfiguration ändert, können Sie die Konstruktorzeichenfolge entsprechend ändern.</span><span class="sxs-lookup"><span data-stu-id="2d939-107">If the system configuration changes, you can change the constructor string accordingly.</span></span>

> [!Note]  
> <span data-ttu-id="2d939-108">Objektkonstruktorzeichenfolgen sollten nicht verwendet werden, um sicherheitsrelevante Informationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2d939-108">Object constructor strings should not be used to store security-sensitive information.</span></span>

 

<span data-ttu-id="2d939-109">Objektkonstruktorzeichenfolgen können in Verbindung mit dem [Objekt Pooling](com--object-pooling.md) verwendet werden, um einen höheren Grad an Granularität beim zusammenfassen und wieder verwenden von Ressourcen zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="2d939-109">You can use object constructor strings in conjunction with [object pooling](com--object-pooling.md) to achieve a greater degree of granularity in how you pool and reuse resources.</span></span> <span data-ttu-id="2d939-110">Beispielsweise können Sie mehrere unterschiedliche Komponenten erstellen, die mit Ausnahme der Konstruktorzeichenfolgen und CLSIDs identisch sind, um unterschiedliche Pools von Objekten zu verwalten, die Verbindungen von unterschiedlichen Client Gruppen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d939-110">For example, you might create several distinct components, identical except for constructor strings and CLSIDs, to maintain distinct pools of objects holding connections usable by distinct groups of clients.</span></span> <span data-ttu-id="2d939-111">Dies wäre nützlich, wenn Verbindungen so geöffnet werden, dass Sie an bestimmte Sicherheitsrollen gebunden werden – z. b. wenn die Verbindungen mit einer bestimmten Authentifizierung in der Datenbank geöffnet werden – wenn Sie in der Regel nicht wiederverwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="2d939-111">This would be useful if connections are opened in a manner that binds them to particular security roles—such as when the connections are opened with some specific authentication at the database—rendering them non-reusable in the general case.</span></span>

<span data-ttu-id="2d939-112">Zu diesem Zweck können Sie eine einzelne generische Komponente schreiben, die mithilfe von [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)auf objektkonstruktorzeichenfolgen basiert, und Sie neu kompilieren, um verschiedene anpassbare Komponenten zu erstellen, die jeweils über eine eindeutige CLSID verfügen.</span><span class="sxs-lookup"><span data-stu-id="2d939-112">To do this, you can write a single generic component that relies on object constructor strings, using [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct), and recompile it to produce several customizable components each with a distinct CLSID.</span></span> <span data-ttu-id="2d939-113">Anschließend können Sie jede Komponente administrativ so anpassen, dass Sie eine geeignete Verbindung mit einer Konstruktorzeichenfolge öffnet, Sie für die Zusammenstellung konfigurieren und in unterschiedlichen Pools pro CLSID verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="2d939-113">You can then administratively tailor each component to open an appropriate connection with a constructor string, configure them to be pooled, and they will be maintained in distinct pools per CLSID.</span></span>

<span data-ttu-id="2d939-114">Sie können eine Konstruktorzeichenfolge angeben, wenn eine Komponente speziell zum Erkennen der von Ihnen eingegebenen Zeichenfolge geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="2d939-114">You can specify a constructor string when a component has been written specifically to recognize the string that you enter.</span></span> <span data-ttu-id="2d939-115">Komponenten können mithilfe von [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)Programm gesteuert auf diese Zeichen folgen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2d939-115">Components can access these strings programmatically by using [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).</span></span>

<span data-ttu-id="2d939-116">Konstruktorzeichenfolgen werden zur Objekt Erstellungszeit nur übergeben, wenn die Objektkonstruktion administrativ aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2d939-116">Constructor strings are passed in at object creation time only when object construction is administratively enabled.</span></span> <span data-ttu-id="2d939-117">Com+ Ruft die [**IObjectConstruct:: Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) -Methode auf, die implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="2d939-117">COM+ calls the [**IObjectConstruct::Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) method that it implements.</span></span> <span data-ttu-id="2d939-118">In dieser Methode können Sie auf die Konstruktorzeichenfolge mithilfe von [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring)zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2d939-118">Within that method, you can access the constructor string by using [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring).</span></span> <span data-ttu-id="2d939-119">Leere Zeichen folgen können gültige Einträge sein.</span><span class="sxs-lookup"><span data-stu-id="2d939-119">Empty strings can be valid entries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d939-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d939-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d939-121">Com+-Objekt Pooling</span><span class="sxs-lookup"><span data-stu-id="2d939-121">COM+ Object Pooling</span></span>](com--object-pooling.md)
</dt> <dt>

[<span data-ttu-id="2d939-122">Angeben einer Objektkonstruktorzeichenfolge für eine Komponente</span><span class="sxs-lookup"><span data-stu-id="2d939-122">Specifying an Object Constructor String for a Component</span></span>](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="2d939-123">Verwenden einer Objektkonstruktorzeichenfolge zum Erstellen einer Komponente</span><span class="sxs-lookup"><span data-stu-id="2d939-123">Using an Object Constructor String to Construct a Component</span></span>](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



