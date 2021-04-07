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
# <a name="adding-an-attachment-snap-in-extension-node"></a>Erweiterungs Knoten "Anlage-Snap-in hinzufügen"

Eine Erweiterung des Erweiterungs-Snap-Ins muss sich selbst unter dem Knoten Dienste hinzufügen, wenn dieser Knoten von einem Benutzer erweitert wird.

Wenn ein Benutzer den Knoten Dienste unter einem der Sicherheitskonfigurations-Snap-Ins erweitert, verwendet MMC [**IComponentData:: notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) und die MMCN \_ Expand-Benachrichtigungs Meldung, um das Sicherheitskonfigurations-Snap-in sowie alle zugehörigen Erweiterungen zu benachrichtigen.

Das Sicherheitskonfigurations-Snap-in extrahiert dann das interne Format aus dem *lpdataobject*, das vom MMC-Haupt Framework als **lpdataobject**-Typ übergeben wird. Die Verarbeitung wird beendet, wenn der Knotentyp "Dienste" angezeigt wird. Die Erweiterungs-Snap-in-Erweiterung extrahiert dann den Knotentyp aus dem *lpdataobject*. Wenn der Knotentyp einer der von einem Dienst definierten Knoten Typen ist, fügt die Erweiterungs-Snap-in-Erweiterung seine Stamm Knoten unter den angegebenen übergeordneten Knoten ein.

Beachten Sie, dass in diesem Beispiel extractnodetype eine private Funktion ist, die von der Erweiterung implementiert wird. Die Erweiterung überprüft das Datenobjekt, um den Knotentyp zu erhalten. Die Implementierung von extractnodetype wird nicht angezeigt.


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



 

 
