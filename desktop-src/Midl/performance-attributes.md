---
title: Leistungs Attribute
description: Verwenden Sie die folgenden Attribute in einer IDL-Datei, um die Größe des stubcodes zu verringern oder die Leistung anderweitig zu verbessern.
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- IDL-Mittell, Attribute, Leistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbfa518b400d237c9fd3789f61b7e74a0c38276
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037601"
---
# <a name="performance-attributes"></a><span data-ttu-id="82af2-104">Leistungs Attribute</span><span class="sxs-lookup"><span data-stu-id="82af2-104">Performance Attributes</span></span>

<span data-ttu-id="82af2-105">Verwenden Sie die folgenden Attribute in einer IDL-Datei, um die Größe des stubcodes zu verringern oder die Leistung anderweitig zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="82af2-105">Use the following attributes in an IDL file to reduce the size of the stub code or otherwise improve performance.</span></span>



| <span data-ttu-id="82af2-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="82af2-106">Attribute</span></span>                             | <span data-ttu-id="82af2-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="82af2-107">Usage</span></span>                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82af2-108">**lassen**</span><span class="sxs-lookup"><span data-stu-id="82af2-108">**ignore**</span></span>](ignore.md)              | <span data-ttu-id="82af2-109">Gibt an, dass ein in einer Struktur oder Union enthaltener Zeiger und das vom Zeiger festgestellte Objekt nicht übertragen werden soll.</span><span class="sxs-lookup"><span data-stu-id="82af2-109">Designates that a pointer contained in a structure or union and the object indicated by the pointer is not to be transmitted.</span></span>                        |
| [<span data-ttu-id="82af2-110">**nah**</span><span class="sxs-lookup"><span data-stu-id="82af2-110">**local**</span></span>](local.md)                | <span data-ttu-id="82af2-111">Gibt eine Funktion an, die für die Anwendung lokal ist, für die die Mittel-l keinen Stub-Code generieren muss.</span><span class="sxs-lookup"><span data-stu-id="82af2-111">Designates a function that is local to the application for which MIDL does not need to generate stub code.</span></span>                                           |
| [<span data-ttu-id="82af2-112">**Wire \_ Marshal**</span><span class="sxs-lookup"><span data-stu-id="82af2-112">**wire\_marshal**</span></span>](wire-marshal.md) | <span data-ttu-id="82af2-113">Definiert einen Datentyp als einfacheren Typ für die Übertragung über ein Netzwerk und ermöglicht das Implementieren von Marshalling-und unmarshallingroutinen für den Typ.</span><span class="sxs-lookup"><span data-stu-id="82af2-113">Defines a data type as a simpler type for transmission over a network and allows you to implement marshaling and unmarshaling routines for the type.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="82af2-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="82af2-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82af2-115">ACF-Attribute für die Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="82af2-115">Memory Management ACF Attributes</span></span>](memory-management-acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="82af2-116">ACF-Attribute der Stub-Optimierung</span><span class="sxs-lookup"><span data-stu-id="82af2-116">Stub Optimization ACF Attributes</span></span>](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 




