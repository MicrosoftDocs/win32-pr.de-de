---
title: Direct2D bietet keine Unterstützung für das Rendern von Rich-Metadateien in Internet Explorer 9.
description: Direct2D bietet keine Unterstützung für das Rendern von Rich-Metadateien in Internet Explorer 9.
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f51ae6d098c08c0a18656aae2adf3d79d68652
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314823"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a><span data-ttu-id="d45c9-103">Direct2D bietet keine Unterstützung für das Rendern von Rich-Metadateien in Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d45c9-103">Direct2D does not support rendering to rich metafiles in Internet Explorer 9</span></span>

## <a name="platforms"></a><span data-ttu-id="d45c9-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="d45c9-104">Platforms</span></span>

<span data-ttu-id="d45c9-105">**Clients** – Windows Vista, Windows 7, Windows 8</span><span class="sxs-lookup"><span data-stu-id="d45c9-105">**Clients** – Windows Vista, Windows 7, Windows 8</span></span>  
<span data-ttu-id="d45c9-106">**Server** – Windows Server 2008, Windows Server 2008 R2, Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d45c9-106">**Servers** – Windows Server 2008, Windows Server 2008 R2, Windows Server 2012</span></span>  




## <a name="description"></a><span data-ttu-id="d45c9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d45c9-107">Description</span></span>

<span data-ttu-id="d45c9-108">Aufgrund interner Renderingänderungen in Internet Explorer 9 erstellen die [ihtmlelementrender::D rawtodc](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) -und [IViewObject::D RAW](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) -APIs nun eine Metadatei mit einer einzelnen Bitmap, die den Webinhalt darstellt, anstelle einer umfangreichen Metadatei, die Text-und Vektor Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="d45c9-108">Due to internal rendering changes in Internet Explorer 9, the [IHTMLElementRender::DrawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) and [IViewObject::Draw](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) APIs will now create a metafile containing a single bitmap that represents the web content instead of a rich metafile containing text and vector info.</span></span> <span data-ttu-id="d45c9-109">Diese Änderung wurde durch den Wechsel vom GDI-Rendering zu einem D2D-Rendering (Hardware-Accelerated Direct2D) verursacht.</span><span class="sxs-lookup"><span data-stu-id="d45c9-109">This change was due to the move from GDI rendering to hardware-accelerated Direct2D (D2D) rendering.</span></span>

<span data-ttu-id="d45c9-110">Diese Änderung betrifft apps, die diese APIs verwenden und auf Text-oder Vektor Informationen in der Metadatei basieren.</span><span class="sxs-lookup"><span data-stu-id="d45c9-110">This change affects apps that use these APIs and rely on text or vector info in the metafile.</span></span>

## <a name="manifestation"></a><span data-ttu-id="d45c9-111">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="d45c9-111">Manifestation</span></span>

<span data-ttu-id="d45c9-112">Abhängig von der APP, die von dieser Änderung betroffen ist, sehen Benutzer möglicherweise ein fehlerhaftes oder falsches Verhalten in ihren apps.</span><span class="sxs-lookup"><span data-stu-id="d45c9-112">Depending on the app that is affected by this change, users might see broken or incorrect behavior in their apps.</span></span>

## <a name="mitigation"></a><span data-ttu-id="d45c9-113">Minderung</span><span class="sxs-lookup"><span data-stu-id="d45c9-113">Mitigation</span></span>

<span data-ttu-id="d45c9-114">Apps, die nur Textinformationen aus einem Webdokument (ohne Positionsinformationen) extrahieren müssen, können die [InnerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) -Eigenschaft verwenden, um Text zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="d45c9-114">Apps that only need to extract text info from a web document (without positioning info) can use the [innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) property to extract text.</span></span>

<span data-ttu-id="d45c9-115">Apps, die IViewObject::D RAW verwenden, können die [Funktion \_ iviewobjectdraw \_ DMLT9 mit dem \_ \_ GDI](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) -Funktions Steuerungs Schlüssel verwenden, um das GDI-Rendering wiederherzustellen, wenn der Dokument Modus:</span><span class="sxs-lookup"><span data-stu-id="d45c9-115">Apps that use IViewObject::Draw can use the [FEATURE\_IVIEWOBJECTDRAW\_DMLT9\_WITH\_GDI](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) feature control key to revert to GDI rendering if the document mode:</span></span>

-   <span data-ttu-id="d45c9-116">Ist kleiner oder gleich 8</span><span class="sxs-lookup"><span data-stu-id="d45c9-116">Is less or equal to 8</span></span>
-   <span data-ttu-id="d45c9-117">Der FCK autorisiert diesen Host für die Verwendung von GDI.</span><span class="sxs-lookup"><span data-stu-id="d45c9-117">The FCK authorizes that host to use GDI</span></span>
-   <span data-ttu-id="d45c9-118">Und ein metadateidc wird an die API übergeben.</span><span class="sxs-lookup"><span data-stu-id="d45c9-118">And a metafile DC is passed to the API</span></span>

## <a name="resources"></a><span data-ttu-id="d45c9-119">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d45c9-119">Resources</span></span>

-   <span data-ttu-id="d45c9-120">[Ihtmlelementrender::D rawmondc](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d45c9-120">[IHTMLElementRender::DrawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))</span></span>
-   [<span data-ttu-id="d45c9-121">IViewObject::D RAW</span><span class="sxs-lookup"><span data-stu-id="d45c9-121">IViewObject::Draw</span></span>](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   <span data-ttu-id="d45c9-122">[IHTMLElement:: InnerText-Eigenschaft](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d45c9-122">[IHTMLElement::innerText Property](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))</span></span>
-   <span data-ttu-id="d45c9-123">[Internet Funktions Steuerelemente (I... Int](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d45c9-123">[Internet Feature Controls (I..L)](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))</span></span>

 

 