---
title: Active Accessibility Text Dienste
description: In diesem Abschnitt werden die Schnittstellen der Active Accessibility Text Dienste erläutert.
ms.assetid: 8bbc647f-1687-45b8-8b63-a6ea45a0a721
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe9fdb4d9d9972f93db780d274b39e587e51c03b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473612"
---
# <a name="active-accessibility-text-services"></a><span data-ttu-id="c79b6-103">Active Accessibility Text Dienste</span><span class="sxs-lookup"><span data-stu-id="c79b6-103">Active Accessibility Text Services</span></span>

<span data-ttu-id="c79b6-104">In diesem Abschnitt werden die Schnittstellen der Active Accessibility Text Dienste erläutert.</span><span class="sxs-lookup"><span data-stu-id="c79b6-104">This section discusses the Active Accessibility Text Services interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="c79b6-105">Active Accessibility Text Dienste sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="c79b6-105">Active Accessibility Text Services is deprecated.</span></span> <span data-ttu-id="c79b6-106">Weitere Informationen zu erweiterten Text Eingaben und Technologien für natürliche Sprache finden Sie im [Microsoft Windows-Text Dienst-Framework](../tsf/text-services-framework.md) .</span><span class="sxs-lookup"><span data-stu-id="c79b6-106">Please see [Microsoft Windows Text Services Framework](../tsf/text-services-framework.md) for more information on advanced text input and natural language technologies.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c79b6-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c79b6-107">In this section</span></span>

| <span data-ttu-id="c79b6-108">Thema</span><span class="sxs-lookup"><span data-stu-id="c79b6-108">Topic</span></span>                                                     | <span data-ttu-id="c79b6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c79b6-109">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c79b6-110">**Iaccserverdocmgr**</span><span class="sxs-lookup"><span data-stu-id="c79b6-110">**IAccServerDocMgr**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-iaccserverdocmgr)   | <span data-ttu-id="c79b6-111">Macht Methoden verfügbar, die für Client Anwendungen auf die Dokumente zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="c79b6-111">Exposes methods that make documents accessible to client applications.</span></span>                              |
| [<span data-ttu-id="c79b6-112">**Iaccclientdocmgr**</span><span class="sxs-lookup"><span data-stu-id="c79b6-112">**IAccClientDocMgr**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-iaccclientdocmgr)   | <span data-ttu-id="c79b6-113">Macht Methoden verfügbar, mit denen Client Anwendungen Dokumente abrufen können.</span><span class="sxs-lookup"><span data-stu-id="c79b6-113">Exposes methods for client applications to retrieve documents.</span></span>                                      |
| [<span data-ttu-id="c79b6-114">**Iaccdictionary**</span><span class="sxs-lookup"><span data-stu-id="c79b6-114">**IAccDictionary**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary)       | <span data-ttu-id="c79b6-115">Macht Methoden für die Zeichen folgen Bearbeitung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c79b6-115">Exposes methods for string manipulation.</span></span>                                                            |
| [<span data-ttu-id="c79b6-116">**Icokreatelocal**</span><span class="sxs-lookup"><span data-stu-id="c79b6-116">**ICoCreateLocally**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-icocreatelocally)   | <span data-ttu-id="c79b6-117">Macht eine Methode verfügbar, die es einer Client Anwendung ermöglicht, ein Hilfsobjekt im Server Kontext zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c79b6-117">Exposes a method that enables a client application to create a helper object in the server context.</span></span> |
| [<span data-ttu-id="c79b6-118">**Icokreatedlokal**</span><span class="sxs-lookup"><span data-stu-id="c79b6-118">**ICoCreatedLocally**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-icocreatedlocally) | <span data-ttu-id="c79b6-119">Macht eine Methode verfügbar, um Informationen über ein lokales Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="c79b6-119">Exposes a method to return information about a local object.</span></span>                                        |
| [<span data-ttu-id="c79b6-120">**Iversioninfo**</span><span class="sxs-lookup"><span data-stu-id="c79b6-120">**IVersionInfo**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-iversioninfo)           | <span data-ttu-id="c79b6-121">Macht Methoden verfügbar, die Versionsinformationen für barrierefreie Elemente bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c79b6-121">Exposes methods that supply version information for accessible elements.</span></span>                            |

## <a name="related-topics"></a><span data-ttu-id="c79b6-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c79b6-122">Related topics</span></span>

[<span data-ttu-id="c79b6-123">Active Accessibility von Benutzeroberflächen Diensten</span><span class="sxs-lookup"><span data-stu-id="c79b6-123">Active Accessibility User Interface Services</span></span>](active-accessibility-user-interface-services-dev-guide.md)