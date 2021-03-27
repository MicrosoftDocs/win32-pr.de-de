---
title: Allgemeine Versions Schnittstellen
description: Dieser Abschnitt enthält Informationen zu den allgemeinen Versions Schnittstellen.
ms.assetid: d228c3c2-e2ff-4723-aec1-5c3ce82c321d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f535650fa24593cc4b663c1a2b01a1a2d53a9b3b
ms.sourcegitcommit: 8f833c83be1accc119cc57e67b608ffe1e0159b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/07/2020
ms.locfileid: "103734681"
---
# <a name="common-version-interfaces"></a><span data-ttu-id="a3cf4-103">Allgemeine Versions Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a3cf4-103">Common version interfaces</span></span>

<span data-ttu-id="a3cf4-104">Dieser Abschnitt enthält Informationen zu den allgemeinen Versions Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="a3cf4-104">This section contains information about the common version interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a3cf4-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a3cf4-105">In this section</span></span>

| <span data-ttu-id="a3cf4-106">Thema</span><span class="sxs-lookup"><span data-stu-id="a3cf4-106">Topic</span></span> | <span data-ttu-id="a3cf4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3cf4-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="a3cf4-108">**ID3D10Blob**</span><span class="sxs-lookup"><span data-stu-id="a3cf4-108">**ID3D10Blob**</span></span>](/windows/win32/api/d3dcommon/nn-d3dcommon-id3d10blob) | <span data-ttu-id="a3cf4-109">Diese Schnittstelle wird verwendet, um Daten beliebiger Länge zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a3cf4-109">This interface is used to return arbitrary-length data.</span></span> |
| <span data-ttu-id="a3cf4-110">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a3cf4-110">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span> | <span data-ttu-id="a3cf4-111">Diese Schnittstelle wird verwendet, um Daten beliebiger Länge zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a3cf4-111">This interface is used to return data of arbitrary length.</span></span> |
| [<span data-ttu-id="a3cf4-112">**ID3DDestructionNotifier**</span><span class="sxs-lookup"><span data-stu-id="a3cf4-112">**ID3DDestructionNotifier**</span></span>](/windows/win32/api/d3dcommon/nn-d3dcommon-id3ddestructionotifier) | <span data-ttu-id="a3cf4-113">Wird verwendet, um für Rückrufe zu registrieren, wenn ein direktes 3D-Nano-com-Objekt zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="a3cf4-113">Used to register for callbacks when a Direct 3D nano-COM object is destroyed.</span></span> |
| [<span data-ttu-id="a3cf4-114">**ID3DInclude**</span><span class="sxs-lookup"><span data-stu-id="a3cf4-114">**ID3DInclude**</span></span>](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) | <span data-ttu-id="a3cf4-115">[**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) ist eine include-Schnittstelle, die der Benutzer implementiert, um es einer Anwendung zu ermöglichen, Benutzer über schreibbare Methoden zum Öffnen und Schließen von Shader-Includedateien aufzurufen \# .</span><span class="sxs-lookup"><span data-stu-id="a3cf4-115">[**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) is an include interface that the user implements to allow an application to call user-overridable methods for opening and closing shader \#include files.</span></span> |
| [<span data-ttu-id="a3cf4-116">**ID3DUserDefinedAnnotation**</span><span class="sxs-lookup"><span data-stu-id="a3cf4-116">**ID3DUserDefinedAnnotation**</span></span>](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) | <span data-ttu-id="a3cf4-117">Die [**ID3DUserDefinedAnnotation**](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) -Schnittstelle ermöglicht es einer Anwendung, konzeptionelle Abschnitte und Marker innerhalb des Code Flusses der Anwendung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a3cf4-117">The [**ID3DUserDefinedAnnotation**](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) interface enables an application to describe conceptual sections and markers within the application's code flow.</span></span> <span data-ttu-id="a3cf4-118">Ein entsprechend aktiviertes Tool, wie z. b. Microsoft Visual Studio Ultimate 2012, kann diese Abschnitte und Markierungen visuell entlang der Microsoft Direct3D-Zeilenlinie des Tools anzeigen, während das Tool die Anwendung debuggt.</span><span class="sxs-lookup"><span data-stu-id="a3cf4-118">An appropriately enabled tool, such as Microsoft Visual Studio Ultimate 2012, can display these sections and markers visually along the tool's Microsoft Direct3D time line, while the tool debugs the application.</span></span> <span data-ttu-id="a3cf4-119">Mit diesen visuellen Notizen können Benutzer eines solchen Tools zu den Teilen der zeitanzahl navigieren, die von Interesse sind, oder um zu verstehen, welche Direct3D-Aufrufe von bestimmten Abschnitten des Anwendungs Codes erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a3cf4-119">These visual notes allow users of such a tool to navigate to parts of the time line that are of interest, or to understand what set of Direct3D calls are produced by certain sections of the application's code.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="a3cf4-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a3cf4-120">Related topics</span></span>

[<span data-ttu-id="a3cf4-121">Allgemeine Versions Referenz</span><span class="sxs-lookup"><span data-stu-id="a3cf4-121">Common version reference</span></span>](d3d11-graphics-reference-d3d11-common.md)
