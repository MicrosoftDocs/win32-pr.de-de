---
description: Registrieren von DirectShow-Filtern
ms.assetid: 2b6304c0-4b67-4723-94a0-7b1fff534f91
title: Registrieren von DirectShow-Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301f26884115526e25e8875867f7cc2bdc628698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392573"
---
# <a name="how-to-register-directshow-filters"></a><span data-ttu-id="772c8-103">Registrieren von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="772c8-103">How to Register DirectShow Filters</span></span>

<span data-ttu-id="772c8-104">In diesem Artikel wird beschrieben, wie Sie einen Microsoft DirectShow-Filter selbst registrieren.</span><span class="sxs-lookup"><span data-stu-id="772c8-104">This article describes how to make a Microsoft DirectShow filter self-registering.</span></span> <span data-ttu-id="772c8-105">Sie enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="772c8-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="772c8-106">Layout der Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="772c8-106">Layout of the Registry Keys</span></span>](layout-of-the-registry-keys.md)
-   [<span data-ttu-id="772c8-107">Deklarieren von Filter Informationen</span><span class="sxs-lookup"><span data-stu-id="772c8-107">Declaring Filter Information</span></span>](declaring-filter-information.md)
-   [<span data-ttu-id="772c8-108">Deklarieren der Factory-Vorlage</span><span class="sxs-lookup"><span data-stu-id="772c8-108">Declaring the Factory Template</span></span>](declaring-the-factory-template.md)
-   [<span data-ttu-id="772c8-109">Implementieren von DllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="772c8-109">Implementing DllRegisterServer</span></span>](implementing-dllregisterserver.md)
-   [<span data-ttu-id="772c8-110">Richtlinien zum Registrieren von Filtern</span><span class="sxs-lookup"><span data-stu-id="772c8-110">Guidelines for Registering Filters</span></span>](guidelines-for-registering-filters.md)
-   [<span data-ttu-id="772c8-111">Aufheben der Registrierung eines Filters</span><span class="sxs-lookup"><span data-stu-id="772c8-111">Unregistering a Filter</span></span>](unregistering-a-filter.md)

<span data-ttu-id="772c8-112">In diesem Artikel wird nicht beschrieben, wie Sie eine DLL für einen DirectShow-Filter erstellen.</span><span class="sxs-lookup"><span data-stu-id="772c8-112">This article does not describe how to create a DLL for a DirectShow filter.</span></span> <span data-ttu-id="772c8-113">Weitere Informationen zum Erstellen von DLLs finden [Sie unter Erstellen einer DirectShow-Filter-DLL](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="772c8-113">For information on creating DLLs, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="772c8-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="772c8-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="772c8-115">DirectShow und com</span><span class="sxs-lookup"><span data-stu-id="772c8-115">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



