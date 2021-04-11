---
title: Server Anmerkung
description: Dieser Abschnitt enthält Informationen zur Verwendung der Server Anmerkung.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe1b8fba9849b25a29c50ea1f55507e61eb69f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036572"
---
# <a name="server-annotation"></a><span data-ttu-id="c0365-103">Server Anmerkung</span><span class="sxs-lookup"><span data-stu-id="c0365-103">Server Annotation</span></span>

<span data-ttu-id="c0365-104">Dieser Abschnitt enthält Informationen zur Verwendung der Server Anmerkung.</span><span class="sxs-lookup"><span data-stu-id="c0365-104">This section provides information about using server annotation.</span></span>

## <a name="summary"></a><span data-ttu-id="c0365-105">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="c0365-105">Summary</span></span>

<span data-ttu-id="c0365-106">Sie definieren eine Klasse, die [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver)implementiert, eine Instanz davon erstellt und dem System mitteilt, dass Sie bestimmte Eigenschaften für bestimmte UI-Elemente überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="c0365-106">You define a class that implements [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), create an instance of it, and tell the system that you want it to override specific properties on specific UI elements.</span></span> <span data-ttu-id="c0365-107">Wenn ein Client eine der Eigenschaften von einem der Benutzeroberflächen Elemente anfordert, wird das Objekt aufgerufen und erhält die Möglichkeit, einen Wert anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c0365-107">When a client requests one of the properties from one of the UI elements, your object is called and given an opportunity to provide a value.</span></span> <span data-ttu-id="c0365-108">Wenn das Objekt einen Wert zurückgibt, wird dieser Wert an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c0365-108">If your object returns a value, that value is passed back to the client.</span></span> <span data-ttu-id="c0365-109">Wenn das Objekt keinen Wert zurückgibt, wird der Standardwert für dieses UI-Element an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c0365-109">If your object does not return a value, the default value for that UI element is returned to the client.</span></span>

## <a name="when-to-use-this-technique"></a><span data-ttu-id="c0365-110">Verwendungszwecke dieser Technik</span><span class="sxs-lookup"><span data-stu-id="c0365-110">When to Use This Technique</span></span>

<span data-ttu-id="c0365-111">Verwenden Sie dieses Verfahren, wenn Sie die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften für ein Objekt überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="c0365-111">Use this technique when you want to override the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties for an object.</span></span> <span data-ttu-id="c0365-112">Diese Methode ist viel einfacher als vorherige **IAccessible** -Techniken.</span><span class="sxs-lookup"><span data-stu-id="c0365-112">This technique is much simpler than previous **IAccessible** techniques.</span></span> <span data-ttu-id="c0365-113">Weitere Informationen finden Sie unter [Alternativen zur dynamischen Anmerkung](alternatives-to-dynamic-annotation.md).</span><span class="sxs-lookup"><span data-stu-id="c0365-113">For more information, see [Alternatives to Dynamic Annotation](alternatives-to-dynamic-annotation.md).</span></span>

<span data-ttu-id="c0365-114">Sie können die-Server Anmerkung nicht verwenden, um die verfügbar gemachte Objektstruktur zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c0365-114">You cannot use server annotation to alter the exposed object structure.</span></span> <span data-ttu-id="c0365-115">Um die Struktur eines Objekts zu ändern, müssen Sie einen vollständigen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger implementieren.</span><span class="sxs-lookup"><span data-stu-id="c0365-115">To change the structure of an object, you must implement a full [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>

<span data-ttu-id="c0365-116">Weitere Informationen zur Server Anmerkung finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="c0365-116">For more information on server annotation, see the following topics:</span></span>

-   [<span data-ttu-id="c0365-117">Verwenden der Server Anmerkung</span><span class="sxs-lookup"><span data-stu-id="c0365-117">Using Server Annotation</span></span>](using-server-annotation.md)
-   [<span data-ttu-id="c0365-118">Beispiel für eine Server Anmerkung</span><span class="sxs-lookup"><span data-stu-id="c0365-118">Server Annotation Sample</span></span>](server-annotation-sample.md)

 

 




