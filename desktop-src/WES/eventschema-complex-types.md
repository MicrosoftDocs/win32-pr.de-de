---
title: Komplexe Typen von Ereignis Schemas
description: Im folgenden finden Sie die komplexen Typen, die vom Ereignis Schema definiert werden.
ms.assetid: bc995483-7e54-4224-a372-4e63b0dd764c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2844fef209aedf6819aeaa5a5b6b8a2d698b39a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339015"
---
# <a name="event-schema-complex-types"></a><span data-ttu-id="34f9a-103">Komplexe Typen von Ereignis Schemas</span><span class="sxs-lookup"><span data-stu-id="34f9a-103">Event Schema Complex Types</span></span>

<span data-ttu-id="34f9a-104">Im folgenden finden Sie die komplexen Typen, die vom Ereignis Schema definiert werden.</span><span class="sxs-lookup"><span data-stu-id="34f9a-104">The following are the complex types that the Event schema defines.</span></span>



| <span data-ttu-id="34f9a-105">Komplexer Typ</span><span class="sxs-lookup"><span data-stu-id="34f9a-105">Complex type</span></span>                                                                       | <span data-ttu-id="34f9a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34f9a-106">Description</span></span>                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34f9a-107">**Complexdatatype**</span><span class="sxs-lookup"><span data-stu-id="34f9a-107">**ComplexDataType**</span></span>](eventschema-complexdatatype-complextype.md)                 | <span data-ttu-id="34f9a-108">Definiert eine-Struktur, die ein oder mehrere Datenelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="34f9a-108">Defines a structure that contains one or more data items.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="34f9a-109">**DataType**</span><span class="sxs-lookup"><span data-stu-id="34f9a-109">**DataType**</span></span>](eventschema-datafieldtype-complextype.md)                          | <span data-ttu-id="34f9a-110">Definiert ein Datenelement.</span><span class="sxs-lookup"><span data-stu-id="34f9a-110">Defines a data item.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="34f9a-111">**Debug DataType**</span><span class="sxs-lookup"><span data-stu-id="34f9a-111">**DebugDataType**</span></span>](eventschema-debugdatatype-complextype.md)                     | <span data-ttu-id="34f9a-112">Definiert die Daten, die für Windows-Software-Ablaufverfolgungs-präprozessorereignisse (WPP) protokolliert werden können.</span><span class="sxs-lookup"><span data-stu-id="34f9a-112">Defines the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="34f9a-113">**Eventdatatype**</span><span class="sxs-lookup"><span data-stu-id="34f9a-113">**EventDataType**</span></span>](eventschema-eventdatatype-complextype.md)                     | <span data-ttu-id="34f9a-114">Definiert die Ereignisdaten Elemente und-Strukturen, die die Ereignisdaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="34f9a-114">Defines the event data items and structures that contains the event data.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="34f9a-115">**EventType**</span><span class="sxs-lookup"><span data-stu-id="34f9a-115">**EventType**</span></span>](eventschema-eventtype-complextype.md)                             | <span data-ttu-id="34f9a-116">Definiert den Stamm Knoten des Ereignis Schemas.</span><span class="sxs-lookup"><span data-stu-id="34f9a-116">Defines the root node of the Event schema.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="34f9a-117">**Processingerrordatatype**</span><span class="sxs-lookup"><span data-stu-id="34f9a-117">**ProcessingErrorDataType**</span></span>](eventschema-processingerrordatatype-complextype.md) | <span data-ttu-id="34f9a-118">Definiert einen Fehler, der beim Rendern der Ereignisdaten für das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="34f9a-118">Defines an error that occurred while rendering the event data for the event.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="34f9a-119">**Renderinginfotype**</span><span class="sxs-lookup"><span data-stu-id="34f9a-119">**RenderingInfoType**</span></span>](eventschema-renderingtype-complextype.md)                 | <span data-ttu-id="34f9a-120">Definiert die gerenderten Nachrichten für das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="34f9a-120">Defines the rendered messages for the event.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="34f9a-121">**Systempropertiestype**</span><span class="sxs-lookup"><span data-stu-id="34f9a-121">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)       | <span data-ttu-id="34f9a-122">Definiert die Informationen, die den Anbieter identifizieren und wie er aktiviert wurde, das Ereignis, den Kanal, in den das Ereignis geschrieben wurde, und Systeminformationen, wie z. b. die Prozess-und Thread-IDs.</span><span class="sxs-lookup"><span data-stu-id="34f9a-122">Defines the information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span><br/> |
| [<span data-ttu-id="34f9a-123">**Userdatatype**</span><span class="sxs-lookup"><span data-stu-id="34f9a-123">**UserDataType**</span></span>](eventschema-userdatatype-complextype.md)                       | <span data-ttu-id="34f9a-124">Definiert ein XML-Fragment, das das Layout der Ereignisdaten angibt.</span><span class="sxs-lookup"><span data-stu-id="34f9a-124">Defines an XML fragment that specifies the layout of the event data.</span></span><br/>                                                                                                                           |



 

 

 





