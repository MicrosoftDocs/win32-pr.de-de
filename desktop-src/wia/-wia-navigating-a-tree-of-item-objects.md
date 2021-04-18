---
description: 'Weitere Informationen finden Sie unter: Navigieren in einer Struktur von Element Objekten'
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: Navigieren in einer Struktur von Element Objekten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04e87444c2b9c473268c5e97dd9c26d04d95b93b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354494"
---
# <a name="navigating-a-tree-of-item-objects"></a>Navigieren in einer Struktur von Element Objekten

> [!Note]  
> Dieses Skript System wurde durch die Windows-Abbild Erwerbs-Automatisierungs Schicht (WIA) ersetzt. Weitere Informationen finden Sie unter [Automatisierungs Schicht für Windows-Abbild](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)

 

Eine Anwendung oder ein Skript navigiert von der Elementstruktur eines Windows-Abbild Erwerbs (WIA), um Images auf diesem Gerät zu suchen und auszuwählen. Mithilfe dieses Verfahrens wählt eine Anwendung ein Bild aus und ruft es ab, ohne ein Dialogfeld zu verwenden.

Ein WIA-Gerät wird als Stamm Element in einer Struktur von [**Item**](-wia-item.md) -Objekten dargestellt. Die untergeordneten Elemente in der Struktur stellen Ordner und Bilder für eine Kamera oder Scan Betten für einen Scanner dar.

Nachdem Sie eine Verbindung mit einem Gerät hergestellt haben, rufen Sie die [**Children**](-wia-iwiadispatchitem-children.md) -Eigenschaft des [**Item**](-wia-item.md) -Objekts auf, das das Gerät darstellt (das Stamm Element der Struktur), um eine Auflistung der untergeordneten Elemente (die Bilder oder Scan Betten) des Geräts zu erhalten.

Auflisten Sie diese Auflistung (bei Bedarf rekursiv), um die Elementstruktur zu navigieren.

 

 
