---
description: Ein 802.1 x-Profil enthält die folgenden Schema Elemente.
ms.assetid: be3f1986-d0c2-47f6-b4dd-8defb89bd03a
title: Onex-Schema Elemente
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b7f3e7bac256b915d0e134720fc63b3519b21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756457"
---
# <a name="onex-schema-elements"></a><span data-ttu-id="6cd6a-103">Onex-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="6cd6a-103">OneX Schema Elements</span></span>

<span data-ttu-id="6cd6a-104">Ein 802.1 x-Profil enthält die folgenden Schema Elemente.</span><span class="sxs-lookup"><span data-stu-id="6cd6a-104">An 802.1X profile contains the following schema elements.</span></span> <span data-ttu-id="6cd6a-105">Alle Onex-Schema Elemente gelten für Kabel-und drahtlos Profile.</span><span class="sxs-lookup"><span data-stu-id="6cd6a-105">All OneX schema elements apply to both wired and wireless profiles.</span></span> <span data-ttu-id="6cd6a-106">Die meisten benannten Elemente befinden sich im-Namespace `https://www.microsoft.com/networking/OneX/v1` , mit Ausnahme von [**eapconfig (Onex)**](onexschema-eapconfig-onex-element.md) , der sich im-Namespace befindet `https://www.microsoft.com/provisioning/EapHostConfig` .</span><span class="sxs-lookup"><span data-stu-id="6cd6a-106">Most of the named elements are in the namespace `https://www.microsoft.com/networking/OneX/v1`, except for [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md) which is in the namespace `https://www.microsoft.com/provisioning/EapHostConfig`.</span></span>

<span data-ttu-id="6cd6a-107">In der folgenden Liste werden die definierten Elemente in der Reihenfolge angezeigt, in der die Elemente in einem Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6cd6a-107">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="6cd6a-108">Die Reihenfolge der Elemente wird erzwungen.</span><span class="sxs-lookup"><span data-stu-id="6cd6a-108">The ordering of elements is enforced.</span></span> <span data-ttu-id="6cd6a-109">Nicht alle Elemente befinden sich in jedem Profil, da einige Elemente optional sind.</span><span class="sxs-lookup"><span data-stu-id="6cd6a-109">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="6cd6a-110">In dieser Liste werden nicht alle möglichen Elemente angezeigt, die in einem Profil angezeigt werden können, da Elemente in **xs: beliebige** Einfügepunkte hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="6cd6a-110">This list does not show all possible elements that can appear in a profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="6cd6a-111">**Onex**</span><span class="sxs-lookup"><span data-stu-id="6cd6a-111">**OneX**</span></span>](onexschema-onex-element.md)
    -   [<span data-ttu-id="6cd6a-112">**cacheuserdata (Onex)**</span><span class="sxs-lookup"><span data-stu-id="6cd6a-112">**cacheUserData (OneX)**</span></span>](onexschema-cacheuserdata-onex-element.md)
    -   [<span data-ttu-id="6cd6a-113">**heldperiod (Onex)**</span><span class="sxs-lookup"><span data-stu-id="6cd6a-113">**heldPeriod (OneX)**</span></span>](onexschema-heldperiod-onex-element.md)
    -   [<span data-ttu-id="6cd6a-114">**authperiod (Onex)**</span><span class="sxs-lookup"><span data-stu-id="6cd6a-114">**authPeriod (OneX)**</span></span>](onexschema-authperiod-onex-element.md)
    -   [<span data-ttu-id="6cd6a-115">**startperiod (Onex)**</span><span class="sxs-lookup"><span data-stu-id="6cd6a-115">**startPeriod (OneX)**</span></span>](onexschema-startperiod-onex-element.md)
    -   [<span data-ttu-id="6cd6a-116">**maxstart (Onex)**</span><span class="sxs-lookup"><span data-stu-id="6cd6a-116">**maxStart (OneX)**</span></span>](onexschema-maxstart-onex-element.md)
    -   [<span data-ttu-id="6cd6a-117">**maxauthfailure (Onex)**</span><span class="sxs-lookup"><span data-stu-id="6cd6a-117">**maxAuthFailures (OneX)**</span></span>](onexschema-maxauthfailures-onex-element.md)
    -   [<span data-ttu-id="6cd6a-118">**supplicantmode (Onex)**</span><span class="sxs-lookup"><span data-stu-id="6cd6a-118">**supplicantMode (OneX)**</span></span>](onexschema-supplicantmode-onex-element.md)
    -   [<span data-ttu-id="6cd6a-119">**authmode (Onex)**</span><span class="sxs-lookup"><span data-stu-id="6cd6a-119">**authMode (OneX)**</span></span>](onexschema-authmode-onex-element.md)
    -   [<span data-ttu-id="6cd6a-120">**SingleSignOn (Onex)**</span><span class="sxs-lookup"><span data-stu-id="6cd6a-120">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
        -   [<span data-ttu-id="6cd6a-121">**Type (SingleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="6cd6a-121">**type (singleSignOn)**</span></span>](onexschema-type-singlesignon-element.md)
        -   [<span data-ttu-id="6cd6a-122">**MaxDelay (SingleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="6cd6a-122">**maxDelay (singleSignOn)**</span></span>](onexschema-maxdelay-singlesignon-element.md)
        -   [<span data-ttu-id="6cd6a-123">**userbasedvirtuallan (SingleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="6cd6a-123">**userBasedVirtualLan (singleSignOn)**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md)
    -   [<span data-ttu-id="6cd6a-124">**Eapconfig (Onex)**</span><span class="sxs-lookup"><span data-stu-id="6cd6a-124">**EAPConfig (OneX)**</span></span>](onexschema-eapconfig-onex-element.md)

 

 



