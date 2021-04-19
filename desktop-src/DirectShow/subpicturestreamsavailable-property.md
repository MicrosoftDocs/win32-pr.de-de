---
description: Die subpicturestreamsavailable-Eigenschaft ruft die Anzahl der im aktuellen Titel verfügbaren teilbildstreams ab.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Subpicturestreamsavailable (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e34f780a726966580a72d87b6f7900bb73c1a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360813"
---
# <a name="subpicturestreamsavailable-property"></a>Subpicturestreamsavailable (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `SubpictureStreamsAvailable` Eigenschaft ruft die Anzahl der im aktuellen Titel verfügbaren teilbildstreams ab.

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der verfügbaren Streams als Ganzzahl zurück.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf. Um jeden Stream für sein sprach Attribut abzufragen, müssen Sie zuerst diese Methode zum Abrufen der oberen Grenze aufruft.

Die Datenstrom Nummerierung ist NULL basiert.

 

 



