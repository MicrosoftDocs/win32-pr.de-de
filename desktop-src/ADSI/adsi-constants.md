---
title: ADSI-Konstanten
description: In der folgenden Tabelle sind die Konstanten aufgelistet, die in Active Directory Service Interfaces (ADSI) definiert und verwendet werden.
ms.assetid: facc00e8-2ecd-4428-bddd-cfa1ff1b8538
ms.tgt_platform: multiple
keywords:
- ADS_EXT_INITCREDENTIALS
- ADS_EXT_INITIALIZE_COMPLETE
- ADS_EXT_MAXEXTDISPID
- ADS_EXT_MINEXTDISPID
- ADS_VLV_RESPONSE
- DBPROPFLAGS_ADSISEARCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc4aaf5043f9fcd2a61dfa68124b6cb1a1a69b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707487"
---
# <a name="adsi-constants"></a><span data-ttu-id="a051f-109">ADSI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="a051f-109">ADSI Constants</span></span>

<span data-ttu-id="a051f-110">In der folgenden Tabelle sind die Konstanten aufgelistet, die in Active Directory Service Interfaces (ADSI) definiert und verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a051f-110">The following table lists constants defined and used in Active Directory Service Interfaces (ADSI).</span></span>



| <span data-ttu-id="a051f-111">ADSI-Konstante</span><span class="sxs-lookup"><span data-stu-id="a051f-111">ADSI constant</span></span>                      | <span data-ttu-id="a051f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a051f-112">Value</span></span>                                   | <span data-ttu-id="a051f-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a051f-113">Description</span></span>                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a051f-114">**ADS \_ - \_ Anmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="a051f-114">**ADS\_EXT\_INITCREDENTIALS**</span></span>      | <span data-ttu-id="a051f-115">1</span><span class="sxs-lookup"><span data-stu-id="a051f-115">1</span></span>                                       | <span data-ttu-id="a051f-116">Ein Steuercode, der angibt, dass die benutzerdefinierten Daten, die für die [**iadsextension::**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) Operation-Methode bereitgestellt werden, Benutzer Anmelde Informationen enthalten</span><span class="sxs-lookup"><span data-stu-id="a051f-116">A control code that indicates that the custom data supplied to the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method contains user credentials.</span></span>                                                     |
| <span data-ttu-id="a051f-117">**Werbung \_ zum \_ Initialisieren von anzeigen \_**</span><span class="sxs-lookup"><span data-stu-id="a051f-117">**ADS\_EXT\_INITIALIZE\_COMPLETE**</span></span> | <span data-ttu-id="a051f-118">2</span><span class="sxs-lookup"><span data-stu-id="a051f-118">2</span></span>                                       | <span data-ttu-id="a051f-119">Ein Steuerelement Code, der mit [**iadsextension::**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) Operation verwendet wird, um anzugeben, dass Erweiterungen jede erforderliche Initialisierung ausführen können, abhängig von den Funktionen, die vom übergeordneten Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a051f-119">A control code used with [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) to indicate that extensions can perform any necessary initialization, depending on the features supported by the parent object.</span></span> |
| <span data-ttu-id="a051f-120">**ADS \_ Ext \_ maxextdispid**</span><span class="sxs-lookup"><span data-stu-id="a051f-120">**ADS\_EXT\_MAXEXTDISPID**</span></span>         | <span data-ttu-id="a051f-121">16777215</span><span class="sxs-lookup"><span data-stu-id="a051f-121">16777215</span></span>                                | <span data-ttu-id="a051f-122">Die höchste dispid, die ein Erweiterungs Objekt für seine Methoden und Eigenschaften verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="a051f-122">The highest DISPID an extension object can use for its methods and properties.</span></span>                                                                                                                                   |
| <span data-ttu-id="a051f-123">**ADS \_ Ext \_ minextdispid**</span><span class="sxs-lookup"><span data-stu-id="a051f-123">**ADS\_EXT\_MINEXTDISPID**</span></span>         | <span data-ttu-id="a051f-124">1</span><span class="sxs-lookup"><span data-stu-id="a051f-124">1</span></span>                                       | <span data-ttu-id="a051f-125">Die niedrigste DISPID, die ein Erweiterungs Objekt für seine Methoden und Eigenschaften verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="a051f-125">The lowest DISPID an extension object can use for its methods and properties.</span></span>                                                                                                                                    |
| <span data-ttu-id="a051f-126">**Anzeigen der \_ VLV- \_ Antwort**</span><span class="sxs-lookup"><span data-stu-id="a051f-126">**ADS\_VLV\_RESPONSE**</span></span>             | <span data-ttu-id="a051f-127">L "fc8cb04d-311d-406c-8cb9-1ae8b843b419"</span><span class="sxs-lookup"><span data-stu-id="a051f-127">L"fc8cb04d-311d-406c-8cb9-1ae8b843b419"</span></span> | <span data-ttu-id="a051f-128">Wird mit der [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) -Methode zum Abrufen von VLV-Such Metadaten verwendet.</span><span class="sxs-lookup"><span data-stu-id="a051f-128">Used with the [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) method to retrieve VLV search metadata.</span></span> <span data-ttu-id="a051f-129">Weitere Informationen finden Sie unter Vorgehens [Weise beim Suchen mit VLV](how-to-search-using-vlv.md).</span><span class="sxs-lookup"><span data-stu-id="a051f-129">For more information, see [How to Search Using VLV](how-to-search-using-vlv.md).</span></span>        |
| <span data-ttu-id="a051f-130">**dbpropflags \_ adsisearch**</span><span class="sxs-lookup"><span data-stu-id="a051f-130">**DBPROPFLAGS\_ADSISEARCH**</span></span>        | <span data-ttu-id="a051f-131">0x0000c000</span><span class="sxs-lookup"><span data-stu-id="a051f-131">0x0000C000</span></span>                              | <span data-ttu-id="a051f-132">Wird verwendet, um mit dem OLE DB-Anbieter zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a051f-132">Used to work with the OLE DB provider.</span></span>                                                                                                                                                                           |



 

 

 




