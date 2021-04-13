---
title: Barrierefreiheit für das fensterlose ActiveX-Steuerelement
description: In diesem Abschnitt wird beschrieben, wie Sie die Windows-Barrierefreiheits-API verwenden, um sicherzustellen, dass auf fensterlose Microsoft ActiveX-Steuerelemente
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb0489cdd5de3ac34df361bfa3e7b3624ee18f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390706"
---
# <a name="windowless-activex-control-accessibility"></a><span data-ttu-id="d2c0b-103">Barrierefreiheit für das fensterlose ActiveX-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d2c0b-103">Windowless ActiveX Control Accessibility</span></span>

<span data-ttu-id="d2c0b-104">In diesem Abschnitt wird beschrieben, wie Sie die Windows-Barrierefreiheits-API verwenden, um sicherzustellen, dass auf fensterlose Microsoft ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="d2c0b-104">This section describes how to use the Windows Accessibility API to ensure that windowless Microsoft ActiveX controls are accessible.</span></span>

<span data-ttu-id="d2c0b-105">Windows 8 enthält neue API-Schnittstellen für die Barrierefreiheit von Windows, die die Implementierung von Barrierefreiheit für fensterlose ActiveX-Steuerelemente vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-105">Windows 8 includes new Windows Accessibility API interfaces that simplify the task of implementing accessibility for windowless ActiveX controls.</span></span> <span data-ttu-id="d2c0b-106">Die API enthält Schnittstellen, die auf einem fensterlosen Steuerelement und im Steuerelement Container implementiert werden, sodass das fensterlose Steuerelement und sein Container zusammenarbeiten können, um Barrierefreiheits Informationen über das fensterlose Steuerelement bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-106">The API includes interfaces that are implemented on a windowless control and on the control container, enabling the windowless control and its container to work together to provide accessibility information about the windowless control.</span></span> <span data-ttu-id="d2c0b-107">Die API unterstützt die folgenden Szenarien:</span><span class="sxs-lookup"><span data-stu-id="d2c0b-107">The API supports the following scenarios:</span></span>

-   <span data-ttu-id="d2c0b-108">Microsoft Active Accessibility fensterlose Steuerelemente, die in einem Microsoft Active Accessibility Control-Container gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-108">Microsoft Active Accessibility windowless controls hosted in a Microsoft Active Accessibility control container.</span></span>
-   <span data-ttu-id="d2c0b-109">Microsoft Active Accessibility fensterlose Steuerelemente, die in einem Microsoft UI Automation Control-Container gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-109">Microsoft Active Accessibility windowless controls hosted in a Microsoft UI Automation control container.</span></span>
-   <span data-ttu-id="d2c0b-110">Benutzeroberflächen Automatisierung fensterlose Steuerelemente, die in einem Microsoft Active Accessibility Control-Container gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-110">UI Automation windowless controls hosted in a Microsoft Active Accessibility control container.</span></span>
-   <span data-ttu-id="d2c0b-111">Benutzeroberflächenautomatisierungs-Steuerelemente, die in einem Benutzeroberflächenautomatisierungs-Steuerungs Container gehostet werden</span><span class="sxs-lookup"><span data-stu-id="d2c0b-111">UI Automation windowless controls hosted in a UI Automation control container.</span></span>

<span data-ttu-id="d2c0b-112">In der folgenden Tabelle werden die Schnittstellen aufgelistet, die fensterlose ActiveX-Steuerelemente unterstützen und die Objekte identifizieren, die die Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="d2c0b-112">The following table lists the interfaces that support windowless ActiveX controls and identifies the objects that implement the interfaces.</span></span>



| <span data-ttu-id="d2c0b-113">Object</span><span class="sxs-lookup"><span data-stu-id="d2c0b-113">Object</span></span>              | <span data-ttu-id="d2c0b-114">MSAA</span><span class="sxs-lookup"><span data-stu-id="d2c0b-114">MSAA</span></span>                                                                             | <span data-ttu-id="d2c0b-115">Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="d2c0b-115">UI automation</span></span>                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c0b-116">Control-Objekt</span><span class="sxs-lookup"><span data-stu-id="d2c0b-116">Control object</span></span>      | [<span data-ttu-id="d2c0b-117">**IAccessibleHandler**</span><span class="sxs-lookup"><span data-stu-id="d2c0b-117">**IAccessibleHandler**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| <span data-ttu-id="d2c0b-118">Steuerungs Website</span><span class="sxs-lookup"><span data-stu-id="d2c0b-118">Control site</span></span>        | [<span data-ttu-id="d2c0b-119">**Iaccessiblewindowlesssite**</span><span class="sxs-lookup"><span data-stu-id="d2c0b-119">**IAccessibleWindowlessSite**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [<span data-ttu-id="d2c0b-120">**Irawelementproviderwindowlesssite**</span><span class="sxs-lookup"><span data-stu-id="d2c0b-120">**IRawElementProviderWindowlessSite**</span></span>](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| <span data-ttu-id="d2c0b-121">Stamm des Host Fensters</span><span class="sxs-lookup"><span data-stu-id="d2c0b-121">Root of host window</span></span> | [<span data-ttu-id="d2c0b-122">**Iaccessiblehostingelementproviders**</span><span class="sxs-lookup"><span data-stu-id="d2c0b-122">**IAccessibleHostingElementProviders**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [<span data-ttu-id="d2c0b-123">**Irawelementproviderhostingaccessibles**</span><span class="sxs-lookup"><span data-stu-id="d2c0b-123">**IRawElementProviderHostingAccessibles**</span></span>](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a><span data-ttu-id="d2c0b-124">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d2c0b-124">In this section</span></span>

-   [<span data-ttu-id="d2c0b-125">Verwenden der Benutzeroberflächen Automatisierung zum Zugreifen auf ein fensterloses ActiveX-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d2c0b-125">How to Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [<span data-ttu-id="d2c0b-126">Verwenden von MSAA zum Zugreifen auf ein fensterloses ActiveX-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d2c0b-126">How to Use MSAA to Make a Windowless ActiveX Control Accessible</span></span>](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [<span data-ttu-id="d2c0b-127">Hosten eines fensterlosen ActiveX-Steuer Elements für die Benutzeroberflächen Automatisierung</span><span class="sxs-lookup"><span data-stu-id="d2c0b-127">How to Host a UI Automation Windowless ActiveX Control</span></span>](host-a-ui-automation-windowless-activex-control.md)
-   [<span data-ttu-id="d2c0b-128">Hosten eines Windows-losen ActiveX-Steuer Elements mit MSAA</span><span class="sxs-lookup"><span data-stu-id="d2c0b-128">How to Host an MSAA Windowless ActiveX Control</span></span>](host-an-msaa-windowless-activex-control.md)

 

 