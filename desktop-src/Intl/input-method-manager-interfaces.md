---
description: In diesem Abschnitt werden die imm-Schnittstellen beschrieben.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Schnittstellen für Eingabemethoden-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bd04c02425aef19ed329867a5b228bd4838af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373072"
---
# <a name="input-method-manager-interfaces"></a><span data-ttu-id="5c525-103">Schnittstellen für Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="5c525-103">Input Method Manager Interfaces</span></span>

<span data-ttu-id="5c525-104">In diesem Abschnitt werden die imm-Schnittstellen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5c525-104">This section describes the IMM interfaces.</span></span>



| <span data-ttu-id="5c525-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5c525-105">Interface</span></span>                                                            | <span data-ttu-id="5c525-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c525-106">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c525-107">**Ifecommon**</span><span class="sxs-lookup"><span data-stu-id="5c525-107">**IFECommon**</span></span>](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | <span data-ttu-id="5c525-108">Bietet IME-bezogene Dienste, die für verschiedene Sprachen üblich sind.</span><span class="sxs-lookup"><span data-stu-id="5c525-108">Provides IME-related services that are common for different languages.</span></span>                                                                         |
| [<span data-ttu-id="5c525-109">**Ifedictionary**</span><span class="sxs-lookup"><span data-stu-id="5c525-109">**IFEDictionary**</span></span>](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | <span data-ttu-id="5c525-110">Ermöglicht Clients den Zugriff auf ein Microsoft IME-Benutzerwörterbuch.</span><span class="sxs-lookup"><span data-stu-id="5c525-110">Allows clients to access a Microsoft IME user dictionary.</span></span>                                                                                      |
| [<span data-ttu-id="5c525-111">**Ifelanguage**</span><span class="sxs-lookup"><span data-stu-id="5c525-111">**IFELanguage**</span></span>](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | <span data-ttu-id="5c525-112">Stellt sprach Verarbeitungsdienste mithilfe von Microsoft IME bereit.</span><span class="sxs-lookup"><span data-stu-id="5c525-112">Provides language processing services using the Microsoft IME.</span></span>                                                                                 |
| [<span data-ttu-id="5c525-113">**Iimepad**</span><span class="sxs-lookup"><span data-stu-id="5c525-113">**IImePad**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | <span data-ttu-id="5c525-114">Fügt Text aus imepadapplets in apps ein, die die [**iimepadapplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="5c525-114">Inserts text into apps from IMEPadApplets that implement the [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) interface.</span></span>                                 |
| [<span data-ttu-id="5c525-115">**Iimepadapplet**</span><span class="sxs-lookup"><span data-stu-id="5c525-115">**IImePadApplet**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | <span data-ttu-id="5c525-116">Eingaben von Zeichen folgen in Apps über die [**iimepad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5c525-116">Inputs strings into apps through the [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) interface.</span></span>                                                                     |
| [<span data-ttu-id="5c525-117">**Iimepluginditdiktattionarylist**</span><span class="sxs-lookup"><span data-stu-id="5c525-117">**IImePlugInDictDictionaryList**</span></span>](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | <span data-ttu-id="5c525-118">Bietet Zugriff auf die Liste der IME-Plug-in-Wörterbücher.</span><span class="sxs-lookup"><span data-stu-id="5c525-118">Provides access to the list of IME plug-in dictionaries.</span></span>                                                                                       |
| [<span data-ttu-id="5c525-119">**Iimespecifyapplets**</span><span class="sxs-lookup"><span data-stu-id="5c525-119">**IImeSpecifyApplets**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | <span data-ttu-id="5c525-120">Gibt Methoden an, die vom [**iimepad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) -Schnittstellen Objekt zum Emulieren der [**iimepadapplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) -Schnittstelle aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5c525-120">Specifies methods called from the [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) interface object to emulate the [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) interface.</span></span> |



 

 

 



