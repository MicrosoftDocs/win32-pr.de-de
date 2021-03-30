---
title: Ebenenenumerationen
description: Dieser Abschnitt enthält Informationen zu ebenenenumerationen.
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- Enumerationen, Direct3D 11-Ebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e1cca3fa500a529930c8d0c39005697045d18b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104976920"
---
# <a name="layer-enumerations"></a><span data-ttu-id="e90b2-104">Ebenenenumerationen</span><span class="sxs-lookup"><span data-stu-id="e90b2-104">Layer Enumerations</span></span>

<span data-ttu-id="e90b2-105">Dieser Abschnitt enthält Informationen zu ebenenenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e90b2-105">This section contains information about the layer enumerations.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="e90b2-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="e90b2-106">In this section</span></span>



| <span data-ttu-id="e90b2-107">Thema</span><span class="sxs-lookup"><span data-stu-id="e90b2-107">Topic</span></span>                                                                                             | <span data-ttu-id="e90b2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e90b2-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e90b2-109">**D3D11- \_ Nachrichten \_ Kategorie**</span><span class="sxs-lookup"><span data-stu-id="e90b2-109">**D3D11\_MESSAGE\_CATEGORY**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | <span data-ttu-id="e90b2-110">Kategorien von Debugmeldungen.</span><span class="sxs-lookup"><span data-stu-id="e90b2-110">Categories of debug messages.</span></span> <span data-ttu-id="e90b2-111">Dadurch wird die Kategorie einer Nachricht identifiziert, wenn eine Nachricht mit [**ID3D11InfoQueue:: getMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) abgerufen und eine Nachricht mit [**ID3D11InfoQueue:: addMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage)hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e90b2-111">This will identify the category of a message when retrieving a message with [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) and when adding a message with [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span></span> <span data-ttu-id="e90b2-112">Beim Erstellen eines [**Informations Warteschlangen Filters**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)können diese Werte verwendet werden, um nach Kategorien von Nachrichten zuzulassen oder zu verweigern, die die Speicher-und Abruf Filter passieren.</span><span class="sxs-lookup"><span data-stu-id="e90b2-112">When creating an [**info queue filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.</span></span><br/> |
| [<span data-ttu-id="e90b2-113">**D3D11 nach \_ richten- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="e90b2-113">**D3D11\_MESSAGE\_ID**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | <span data-ttu-id="e90b2-114">Debugmeldungen zum Einrichten eines Informations Warteschlangen Filters (siehe [**D3D11 \_ Info \_ Queue \_ Filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); verwenden Sie diese Meldungen, um Nachrichten Kategorien zuzulassen oder zu verweigern, die die Speicher-und Abruf Filter passieren.</span><span class="sxs-lookup"><span data-stu-id="e90b2-114">Debug messages for setting up an info-queue filter (see [**D3D11\_INFO\_QUEUE\_FILTER**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); use these messages to allow or deny message categories to pass through the storage and retrieval filters.</span></span> <span data-ttu-id="e90b2-115">Diese IDs werden von Methoden wie [**ID3D11InfoQueue:: getMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) oder [**ID3D11InfoQueue:: addMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage)verwendet.</span><span class="sxs-lookup"><span data-stu-id="e90b2-115">These IDs are used by methods such as [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) or [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span></span> <br/>                                                             |
| [<span data-ttu-id="e90b2-116">**D3D11- \_ Nachrichten \_ Schweregrad**</span><span class="sxs-lookup"><span data-stu-id="e90b2-116">**D3D11\_MESSAGE\_SEVERITY**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | <span data-ttu-id="e90b2-117">Debugnachrichten Schweregrade für eine Informations Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="e90b2-117">Debug message severity levels for an information queue.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="e90b2-118">**D3D11- \_ rldo- \_ Flags**</span><span class="sxs-lookup"><span data-stu-id="e90b2-118">**D3D11\_RLDO\_FLAGS**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | <span data-ttu-id="e90b2-119">Optionen für die Menge der Informationen, die über die Lebensdauer eines Geräte Objekts berichtet werden.</span><span class="sxs-lookup"><span data-stu-id="e90b2-119">Options for the amount of information to report about a device object's lifetime.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="e90b2-120">**D3D11- \_ Shader- \_ Überwachungs \_ Optionen**</span><span class="sxs-lookup"><span data-stu-id="e90b2-120">**D3D11\_SHADER\_TRACKING\_OPTIONS**</span></span>](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | <span data-ttu-id="e90b2-121">Optionen, die angeben, wie die Shader-Debugverfolgung durchgeführt wird</span><span class="sxs-lookup"><span data-stu-id="e90b2-121">Options that specify how to perform shader debug tracking.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="e90b2-122">**D3D11- \_ Shader-nach \_ Verfolgungs \_ \_ Ressourcentyp**</span><span class="sxs-lookup"><span data-stu-id="e90b2-122">**D3D11\_SHADER\_TRACKING\_RESOURCE\_TYPE**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | <span data-ttu-id="e90b2-123">Gibt an, welche Ressourcentypen nachverfolgt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e90b2-123">Indicates which resource types to track.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="e90b2-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e90b2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e90b2-125">Ebenenverweis</span><span class="sxs-lookup"><span data-stu-id="e90b2-125">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





