---
description: Verwenden einer Objektkonstruktorzeichenfolge zum Erstellen einer Komponente
ms.assetid: 57d66988-2a65-4309-957a-36a5972233b5
title: Verwenden einer Objektkonstruktorzeichenfolge zum Erstellen einer Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8cbbb1c156fd7ee675b6c21c8ae097494da59ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483411"
---
# <a name="using-an-object-constructor-string-to-construct-a-component"></a><span data-ttu-id="1ac56-103">Verwenden einer Objektkonstruktorzeichenfolge zum Erstellen einer Komponente</span><span class="sxs-lookup"><span data-stu-id="1ac56-103">Using an Object Constructor String to Construct a Component</span></span>

<span data-ttu-id="1ac56-104">Im folgenden Beispiel wird veranschaulicht, wie eine Objektkonstruktorzeichenfolge Programm gesteuert abgerufen und verwendet wird, wenn eine Komponente instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="1ac56-104">The following example illustrates how to programmatically retrieve and use an object constructor string when a component is instantiated.</span></span> <span data-ttu-id="1ac56-105">Es zeigt eine Implementierung der [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) -Schnittstelle, die eine Objektkonstruktorzeichenfolge abruft.</span><span class="sxs-lookup"><span data-stu-id="1ac56-105">It shows an implementation of the [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) interface that retrieves an object constructor string.</span></span> <span data-ttu-id="1ac56-106">Die Zeichenfolge kann dann analysiert werden, um Anfangswerte festzulegen oder das Verhalten der Komponente zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="1ac56-106">The string can then be parsed to set initial values or influence the behavior of the component.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="1ac56-107">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1ac56-107">Visual Basic</span></span>


```VB
Implements IObjectConstruct
Private Sub IObjectConstruct_Construct( ByVal pCtorObj As Object )
    Dim strConstructorString As String
    strConstructorString = pCtorObj.ConstructString
     Parse and use strConstructorString here. 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="1ac56-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ac56-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ac56-109">Konzepte der com+-objektkonstruktorzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="1ac56-109">COM+ Object Constructor Strings Concepts</span></span>](com--object-constructor-strings-concepts.md)
</dt> <dt>

[<span data-ttu-id="1ac56-110">Angeben einer Objektkonstruktorzeichenfolge für eine Komponente</span><span class="sxs-lookup"><span data-stu-id="1ac56-110">Specifying an Object Constructor String for a Component</span></span>](specifying-an-object-constructor-string-for-a-component.md)
</dt> </dl>

 

 



