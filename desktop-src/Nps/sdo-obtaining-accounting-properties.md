---
title: Abrufen von Buchhaltungs Eigenschaften
description: Das Accounting-Objekt ist eines der Objekte in der Auflistung von Anforderungs Handlern.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9911397c1de3521ccb5a275405416d8b88c1fa6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390596"
---
# <a name="obtaining-accounting-properties"></a><span data-ttu-id="c271c-103">Abrufen von Buchhaltungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c271c-103">Obtaining Accounting Properties</span></span>

> [!Note]  
> <span data-ttu-id="c271c-104">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="c271c-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="c271c-105">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="c271c-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="c271c-106">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="c271c-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="c271c-107">Das Accounting-Objekt ist eines der Objekte in der Auflistung von Anforderungs Handlern.</span><span class="sxs-lookup"><span data-stu-id="c271c-107">The accounting object is one of the objects in the Request Handlers collection.</span></span> <span data-ttu-id="c271c-108">Der Enumerationswert für die Auflistung von Anforderungs Handlern ist die **\_ IAS \_ requesthandlers \_**-Auflistung der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c271c-108">The enumeration value for the request handlers collection is **PROPERTY\_IAS\_REQUESTHANDLERS\_COLLECTION**.</span></span> <span data-ttu-id="c271c-109">Der Name des Handlers für das Buchhaltungs Objekt ist "Microsoft Accounting".</span><span class="sxs-lookup"><span data-stu-id="c271c-109">The name of the handler for the accounting object is "Microsoft Accounting".</span></span>

<span data-ttu-id="c271c-110">Der folgende Visual Basic Code greift auf die Eigenschaften zu, die vom Buchhaltungs Objekt Handler zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c271c-110">The following Visual Basic code accesses the properties available from the accounting object handler.</span></span>


```VB
Set sdoRequestHandler = sdoCollRequestHandlers.Item("Microsoft Accounting")
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_AUTHENTICATION)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE)
```



<span data-ttu-id="c271c-111">Um mit C++ auf die Buchhaltungs Eigenschaften zuzugreifen, rufen Sie zuerst die Auflistung der Anforderungs Handler ab.</span><span class="sxs-lookup"><span data-stu-id="c271c-111">To access the accounting properties using C++, first obtain the request handlers collection.</span></span> <span data-ttu-id="c271c-112">Das [Abrufen einer](/windows/desktop/Nps/sdo-retrieving-a-collection) Auflistung enthält C++-Code, der veranschaulicht, wie eine Auflistung abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c271c-112">The [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection) contains C++ code that demonstrates how to obtain a collection.</span></span> <span data-ttu-id="c271c-113">Der Enumerationswert für die Auflistung von Anforderungs Handlern ist die **\_ IAS \_ requesthandlers \_**-Auflistung der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c271c-113">The enumeration value for the request handlers collection is **PROPERTY\_IAS\_REQUESTHANDLERS\_COLLECTION**.</span></span> <span data-ttu-id="c271c-114">(Die Werte, die den verschiedenen NPS-Auflistungen entsprechen, werden durch den Enumerationstyp [**iasproperties**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) aufgelistet.)</span><span class="sxs-lookup"><span data-stu-id="c271c-114">(The values corresponding to the various NPS collections are enumerated by the [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeration type.)</span></span>

<span data-ttu-id="c271c-115">Die Sammlung der Anforderungs Handler enthält ein Objekt mit dem Namen "Microsoft Accounting".</span><span class="sxs-lookup"><span data-stu-id="c271c-115">The request handlers collection contains an object named "Microsoft Accounting".</span></span> <span data-ttu-id="c271c-116">Rufen Sie dieses-Objekt aus der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="c271c-116">Retrieve this object from the collection.</span></span> <span data-ttu-id="c271c-117">Der Abschnitt [Abrufen eines Objekts aus einer](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) Auflistung enthält C++-Code, der veranschaulicht, wie ein Objekt aus einer Auflistung abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c271c-117">The section [Retrieving an Object from a Collection](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contains C++ code that demonstrates how to obtain an object from a collection.</span></span>

<span data-ttu-id="c271c-118">Wenn Sie über das Microsoft Accounting-Objekt verfügen, rufen Sie mithilfe von [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))eine [**isdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) -Schnittstelle für das Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="c271c-118">Once you have the Microsoft Accounting object, obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface for the object using [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="c271c-119">Der Abschnitt [Abrufen eines Benutzers SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) enthält C++-Code, der veranschaulicht, wie eine **isdo** -Schnittstelle für ein Objekt abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c271c-119">The section [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contains C++ code that demonstrates how obtain an **ISdo** interface for an object.</span></span> <span data-ttu-id="c271c-120">Anschließend können Sie die [**isdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) -Methode verwenden, um Eigenschaftswerte für das Microsoft Accounting-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c271c-120">You can then use the [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) method to obtain property values for the Microsoft Accounting object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c271c-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c271c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c271c-122">Abrufen einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="c271c-122">Retrieving a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[<span data-ttu-id="c271c-123">Abrufen eines Objekts aus einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="c271c-123">Retrieving an Object from a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[<span data-ttu-id="c271c-124">Abrufen eines Benutzers (SDO)</span><span class="sxs-lookup"><span data-stu-id="c271c-124">Retrieving a User SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[<span data-ttu-id="c271c-125">**Isdo**</span><span class="sxs-lookup"><span data-stu-id="c271c-125">**ISdo**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

<span data-ttu-id="c271c-126">[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="c271c-126">[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
</dt> <dt>

[<span data-ttu-id="c271c-127">**Iasproperties**</span><span class="sxs-lookup"><span data-stu-id="c271c-127">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 