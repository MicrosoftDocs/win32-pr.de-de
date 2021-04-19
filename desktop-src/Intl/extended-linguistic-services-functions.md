---
description: Els unterstützt die in der folgenden Tabelle definierten Funktionen.
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: Erweiterte Funktionen für linguistische Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5b8acff7601955f8ed6e37f430caa0a52aa880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358543"
---
# <a name="extended-linguistic-services-functions"></a><span data-ttu-id="932c6-103">Erweiterte Funktionen für linguistische Dienste</span><span class="sxs-lookup"><span data-stu-id="932c6-103">Extended Linguistic Services Functions</span></span>

<span data-ttu-id="932c6-104">Els unterstützt die in der folgenden Tabelle definierten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="932c6-104">ELS supports the functions defined in the following table.</span></span>



| <span data-ttu-id="932c6-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="932c6-105">Function</span></span>                                                 | <span data-ttu-id="932c6-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="932c6-106">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="932c6-107">**Mappingcallbackproc**</span><span class="sxs-lookup"><span data-stu-id="932c6-107">**MappingCallbackProc**</span></span>](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | <span data-ttu-id="932c6-108">Eine Anwendungs definierte Rückruffunktion, die Daten asynchron verarbeitet, die von der **mappingrecognizetext** -Funktion erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="932c6-108">An application-defined callback function that asynchronously processes data produced by the **MappingRecognizeText** function.</span></span>                 |
| [<span data-ttu-id="932c6-109">**Mappingdoaction**</span><span class="sxs-lookup"><span data-stu-id="932c6-109">**MappingDoAction**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | <span data-ttu-id="932c6-110">Bewirkt, dass ein Els-Dienst eine Aktion ausführt, nachdem die Texterkennung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="932c6-110">Causes an ELS service to perform an action after text recognition has occurred.</span></span>                                                                |
| [<span data-ttu-id="932c6-111">**Mappingfrepropertybag**</span><span class="sxs-lookup"><span data-stu-id="932c6-111">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | <span data-ttu-id="932c6-112">Gibt Arbeitsspeicher und Ressourcen frei, die während eines Els-Text Erkennungs Vorgangs zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="932c6-112">Frees memory and resources allocated during an ELS text recognition operation.</span></span>                                                                 |
| [<span data-ttu-id="932c6-113">**Mappingfreeservices**</span><span class="sxs-lookup"><span data-stu-id="932c6-113">**MappingFreeServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | <span data-ttu-id="932c6-114">Gibt Arbeitsspeicher und Ressourcen frei, die der Anwendung für die Interaktion mit einem oder mehreren Els-Diensten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="932c6-114">Frees memory and resources allocated for the application to interact with one or more ELS services.</span></span>                                            |
| [<span data-ttu-id="932c6-115">**Mappinggetservices**</span><span class="sxs-lookup"><span data-stu-id="932c6-115">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | <span data-ttu-id="932c6-116">Ruft nach den von der Anwendung angegebenen Kriterien eine Liste der verfügbaren, von der Plattform unterstützten Dienste zusammen mit zugeordneten Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="932c6-116">Retrieves a list of available ELS platform-supported services, along with associated information, according to application-specified criteria.</span></span> |
| [<span data-ttu-id="932c6-117">**Mappingrecognizetext**</span><span class="sxs-lookup"><span data-stu-id="932c6-117">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | <span data-ttu-id="932c6-118">Ruft auf einem Els-Dienst auf, um Text zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="932c6-118">Calls upon an ELS service to recognize text.</span></span>                                                                                                   |



 

 

 



