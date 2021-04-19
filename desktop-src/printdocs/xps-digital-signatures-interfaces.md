---
description: XPS-API-Schnittstellen für digitale Signaturen
ms.assetid: 44244035-f7d5-47f1-b4d8-b895562be855
title: XPS-API-Schnittstellen für digitale Signaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160fc532ed90cb41e4d0cb524daba87f72edefd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357000"
---
# <a name="xps-digital-signature-api-interfaces"></a><span data-ttu-id="4df5c-103">XPS-API-Schnittstellen für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="4df5c-103">XPS Digital Signature API Interfaces</span></span>

## <a name="contents"></a><span data-ttu-id="4df5c-104">Inhalte</span><span class="sxs-lookup"><span data-stu-id="4df5c-104">Contents</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4df5c-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="4df5c-105">In this section</span></span>



| <span data-ttu-id="4df5c-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4df5c-106">Interface</span></span>                                                                           | <span data-ttu-id="4df5c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4df5c-107">Description</span></span>                                                                                         |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4df5c-108">**Ixpssignature**</span><span class="sxs-lookup"><span data-stu-id="4df5c-108">**IXpsSignature**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)<br/>                                   | <span data-ttu-id="4df5c-109">Stellt eine einzelne digitale Signatur dar.</span><span class="sxs-lookup"><span data-stu-id="4df5c-109">Represents a single digital signature.</span></span><br/>                                                   |
| [<span data-ttu-id="4df5c-110">**Ixpssignatureblock**</span><span class="sxs-lookup"><span data-stu-id="4df5c-110">**IXpsSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)<br/>                         | <span data-ttu-id="4df5c-111">Stellt einen Block von Signatur Anforderungen dar, die in einem signaturedefinitions-Teil gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4df5c-111">Represents a block of signature requests that are stored in a SignatureDefinitions part.</span></span><br/> |
| [<span data-ttu-id="4df5c-112">**Ixpssignatureblockcollection**</span><span class="sxs-lookup"><span data-stu-id="4df5c-112">**IXpsSignatureBlockCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)<br/>     | <span data-ttu-id="4df5c-113">Eine Auflistung von [**ixpssignatureblock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4df5c-113">A collection of [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) interfaces.</span></span><br/>             |
| [<span data-ttu-id="4df5c-114">**Ixpssignaturückruf**</span><span class="sxs-lookup"><span data-stu-id="4df5c-114">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)<br/>               | <span data-ttu-id="4df5c-115">Eine Auflistung von [**ixpssignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) -Schnittstellen Zeigern.</span><span class="sxs-lookup"><span data-stu-id="4df5c-115">A collection of [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) interface pointers.</span></span><br/>               |
| [<span data-ttu-id="4df5c-116">**Ixpssignaturemanager**</span><span class="sxs-lookup"><span data-stu-id="4df5c-116">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)<br/>                     | <span data-ttu-id="4df5c-117">Verwaltet die digitalen Signaturen und die digitalen Signatur Anforderungen eines XPS-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="4df5c-117">Manages the digital signatures and digital signature requests of an XPS document.</span></span><br/>        |
| [<span data-ttu-id="4df5c-118">**Ixpssignaturerequest**</span><span class="sxs-lookup"><span data-stu-id="4df5c-118">**IXpsSignatureRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)<br/>                     | <span data-ttu-id="4df5c-119">Greift auf die Komponenten einer Signatur Anforderung zu.</span><span class="sxs-lookup"><span data-stu-id="4df5c-119">Accesses the components of a signature request.</span></span><br/>                                          |
| [<span data-ttu-id="4df5c-120">**Ixpssignaturerequestcollection**</span><span class="sxs-lookup"><span data-stu-id="4df5c-120">**IXpsSignatureRequestCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)<br/> | <span data-ttu-id="4df5c-121">Eine Auflistung von [**ixpssignaturerequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4df5c-121">A collection of [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) interfaces.</span></span><br/>         |
| [<span data-ttu-id="4df5c-122">**Ixpssigningoptions**</span><span class="sxs-lookup"><span data-stu-id="4df5c-122">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)<br/>                         | <span data-ttu-id="4df5c-123">Bietet Zugriff auf die einzelnen Signierungs Optionen, die von neuen Signaturen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4df5c-123">Provides access to the individual signing options that are used by new signatures.</span></span><br/>       |



 

 

 




