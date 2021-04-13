---
title: Klassenmoniker
description: Obwohl Klassen normalerweise direkt mit CLSIDs für Funktionen wie cokreatanstance oder CoGetClassObject identifiziert werden, können Klassen jetzt auch mit einem Moniker identifiziert werden, der als klassenmoniker bezeichnet wird.
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80886ce49ea25d2fb5acbf4dddf550c9d2c3ae29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311177"
---
# <a name="class-monikers"></a><span data-ttu-id="6e172-103">Klassenmoniker</span><span class="sxs-lookup"><span data-stu-id="6e172-103">Class Monikers</span></span>

<span data-ttu-id="6e172-104">Obwohl Klassen normalerweise direkt mit CLSIDs für Funktionen wie [**cokreatanstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)identifiziert werden, können Klassen jetzt auch mit einem Moniker identifiziert werden, der als *klassenmoniker* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="6e172-104">Although classes are typically identified directly with CLSIDs to functions such as [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), classes may also now be identified with a moniker called a *class moniker*.</span></span> <span data-ttu-id="6e172-105">Klassenmoniker binden an das Klassenobjekt der Klasse, für die Sie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6e172-105">Class monikers bind to the class object of the class for which they are created.</span></span>

<span data-ttu-id="6e172-106">Die Möglichkeit zum Identifizieren von Klassen mit einem Moniker unterstützt nützliche Vorgänge, die ansonsten unhandlich sind.</span><span class="sxs-lookup"><span data-stu-id="6e172-106">The ability to identify classes with a moniker supports useful operations that are otherwise unwieldy.</span></span> <span data-ttu-id="6e172-107">Beispielsweise unterstützten dateimoniker in der Regel nur eine umfangreiche Bindung an die Klasse, die der Klasse der Datei zugeordnet ist, auf die Sie verweisen. ein Moniker für eine Excel-Datei würde eine Bindung an eine Instanz eines Excel-Objekts herstellen, und ein Moniker für ein GIF-Bild würde an eine Instanz des aktuell registrierten GIF-Handlers gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="6e172-107">For example, file monikers traditionally supported rich binding only to the class associated with the class of file they referred to; a moniker to an Excel file would bind to an instance of an Excel object, and a moniker to a GIF image would bind to an instance of the currently registered GIF handler.</span></span> <span data-ttu-id="6e172-108">Mit einem klassenmoniker können Sie die Klasse angeben, die Sie verwenden möchten, um eine Datei durch Komposition mit einem dateimoniker zu manipulieren.</span><span class="sxs-lookup"><span data-stu-id="6e172-108">A class moniker allows you to indicate the class you want to use to manipulate a file through composition with a file moniker.</span></span> <span data-ttu-id="6e172-109">Ein klassenmoniker für eine 3D-Diagramm Klasse, die mit einem Moniker in einer Excel-Datei zusammengesetzt wird, erzeugt einen Moniker, der an eine Instanz des 3D-Diagramm Objekts gebunden ist, und initialisiert das Objekt mit dem Inhalt der Excel-Datei.</span><span class="sxs-lookup"><span data-stu-id="6e172-109">A class moniker for a 3D charting class composed with a moniker to an Excel file yields a moniker that binds to an instance of the 3D charting object and initializes the object with the contents of the Excel file.</span></span>

<span data-ttu-id="6e172-110">Klassenmoniker sind daher am nützlichsten bei der Komposition mit anderen Typen von Monikern, z. b. dateimonikern oder elementmoniker.</span><span class="sxs-lookup"><span data-stu-id="6e172-110">Class monikers are therefore most useful in composition with other types of monikers, such as file monikers or item monikers.</span></span>

<span data-ttu-id="6e172-111">Klassenmoniker können auch rechts von Monikern zusammengesetzt werden, die die Bindung an die [**iclassactivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) -Schnittstelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6e172-111">Class monikers may also be composed to the right of monikers supporting binding to the [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) interface.</span></span> <span data-ttu-id="6e172-112">Wenn Sie auf diese Weise zusammengesetzt wird, bietet **iclassactivator** einfach Zugriff auf das Klassenobjekt und Instanzen der Klasse über [**iclassactivator:: GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject).</span><span class="sxs-lookup"><span data-stu-id="6e172-112">When composed in this manner, **IClassActivator** simply gives access to the class object and instances of the class through [**IClassActivator::GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject).</span></span> <span data-ttu-id="6e172-113">Klassenmoniker können über [**IMoniker:: IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker)identifiziert werden, der den MKSYS- \_ classmoniker in *pdwmksys* zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6e172-113">Class monikers may be identified through [**IMoniker::IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), which returns MKSYS\_CLASSMONIKER in *pdwMksys*.</span></span>

<span data-ttu-id="6e172-114">Programmierer erstellen üblicherweise klassenmoniker mithilfe der Funktion " [**deeclassmoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) " oder mithilfe von " [**mkparsetdisplayname**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname)".</span><span class="sxs-lookup"><span data-stu-id="6e172-114">Programmers typically create class monikers using the [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) function or through [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname).</span></span> <span data-ttu-id="6e172-115">(Weitere Informationen finden Sie unter [**IMoniker::P armendisplayname**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) .)</span><span class="sxs-lookup"><span data-stu-id="6e172-115">(See [**IMoniker::ParseDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) for details.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e172-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e172-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e172-117">Anti-Moniker</span><span class="sxs-lookup"><span data-stu-id="6e172-117">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="6e172-118">Zusammengesetzte Moniker</span><span class="sxs-lookup"><span data-stu-id="6e172-118">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="6e172-119">Dateimoniker</span><span class="sxs-lookup"><span data-stu-id="6e172-119">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="6e172-120">Elementmoniker</span><span class="sxs-lookup"><span data-stu-id="6e172-120">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="6e172-121">Zeigermoniker</span><span class="sxs-lookup"><span data-stu-id="6e172-121">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




