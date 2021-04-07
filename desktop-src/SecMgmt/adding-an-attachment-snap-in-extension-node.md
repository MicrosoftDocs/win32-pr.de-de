---
description: Eine Erweiterung des Erweiterungs-Snap-Ins muss sich selbst unter dem Knoten Dienste hinzufügen, wenn dieser Knoten von einem Benutzer erweitert wird.
ms.assetid: af853c29-11c2-4fd0-ad81-80aebeb74cc3
title: Erweiterungs Knoten "Anlage-Snap-in hinzufügen"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2604a58284af7bc55ff57ae114bc77d8f0cd42ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758035"
---
# <a name="adding-an-attachment-snap-in-extension-node"></a><span data-ttu-id="e482a-103">Erweiterungs Knoten "Anlage-Snap-in hinzufügen"</span><span class="sxs-lookup"><span data-stu-id="e482a-103">Adding an Attachment Snap-in Extension Node</span></span>

<span data-ttu-id="e482a-104">Eine Erweiterung des Erweiterungs-Snap-Ins muss sich selbst unter dem Knoten Dienste hinzufügen, wenn dieser Knoten von einem Benutzer erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="e482a-104">An attachment snap-in extension must add itself under the Services node when that node is expanded by a user.</span></span>

<span data-ttu-id="e482a-105">Wenn ein Benutzer den Knoten Dienste unter einem der Sicherheitskonfigurations-Snap-Ins erweitert, verwendet MMC [**IComponentData:: notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) und die MMCN \_ Expand-Benachrichtigungs Meldung, um das Sicherheitskonfigurations-Snap-in sowie alle zugehörigen Erweiterungen zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="e482a-105">When a user expands the Services node under one of the Security Configuration snap-ins, MMC uses [**IComponentData::Notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) and the MMCN\_EXPAND notification message to notify the Security Configuration snap-in, plus all its extensions.</span></span>

<span data-ttu-id="e482a-106">Das Sicherheitskonfigurations-Snap-in extrahiert dann das interne Format aus dem *lpdataobject*, das vom MMC-Haupt Framework als **lpdataobject**-Typ übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e482a-106">The Security Configuration snap-in then extracts its internal format from the *lpDataObject*, which is passed in from the MMC main framework as type **LPDATAOBJECT**.</span></span> <span data-ttu-id="e482a-107">Die Verarbeitung wird beendet, wenn der Knotentyp "Dienste" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e482a-107">It stops processing when it sees the Services node type.</span></span> <span data-ttu-id="e482a-108">Die Erweiterungs-Snap-in-Erweiterung extrahiert dann den Knotentyp aus dem *lpdataobject*.</span><span class="sxs-lookup"><span data-stu-id="e482a-108">The attachment snap-in extension then extracts the node type from the *lpDataObject*.</span></span> <span data-ttu-id="e482a-109">Wenn der Knotentyp einer der von einem Dienst definierten Knoten Typen ist, fügt die Erweiterungs-Snap-in-Erweiterung seine Stamm Knoten unter den angegebenen übergeordneten Knoten ein.</span><span class="sxs-lookup"><span data-stu-id="e482a-109">If the node type is one of the service's defined node types, the attachment snap-in extension inserts its root nodes under the specified parent node.</span></span>

<span data-ttu-id="e482a-110">Beachten Sie, dass in diesem Beispiel extractnodetype eine private Funktion ist, die von der Erweiterung implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="e482a-110">Note that in this example, ExtractNodeType, is a private function that the extension implements.</span></span> <span data-ttu-id="e482a-111">Die Erweiterung überprüft das Datenobjekt, um den Knotentyp zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e482a-111">The extension examines the data object to get the node type.</span></span> <span data-ttu-id="e482a-112">Die Implementierung von extractnodetype wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e482a-112">The implementation of ExtractNodeType is not shown.</span></span>


```C++
//  Detect which extension node to expand.
GUID* nodeType = ExtractNodeType(lpdataObject);

if (NULL == nodeType)
{
  return S_OK;
}

if (TRUE == ::IsEqualGUID(*nodeType, cNodetypeSceTemplateServices))
{
  folderType = ATTACHMENT_STATIC;  // defined by attachment writer
}

else if (TRUE == ::IsEqualGUID
    (*nodeType, cNodetypeSceAnalysisServices))
{
  folderType = ATTACHMENT_STATIC_ANALYSIS;
               // defined by attachment writer
}

//  Free resources.
::GlobalFree(reinterpret_cast<HANDLE>(nodeType));

//  Add service attachment root node and remember it as the
//  root of the SMB extension namespace.
//  ...
```



 

 
