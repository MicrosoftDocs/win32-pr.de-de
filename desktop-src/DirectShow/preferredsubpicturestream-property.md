---
description: Die PreferredSubpictureStream-Eigenschaft ruft den bevorzugten Bildstrom für die aktuelle Anzeigesitzung ab.
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: PreferredSubpictureStream-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e28b98163607e31a207bffb3974fee3b32505ff60ba3700b452b2dff2625f421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583540"
---
# <a name="preferredsubpicturestream-property"></a>PreferredSubpictureStream-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `PreferredSubpictureStream` -Eigenschaft ruft den bevorzugten Bildstrom für die aktuelle Anzeigesitzung ab.

``` syntax
[iStream = ] MSWebDVD.PreferredSubpictureStream
```

## <a name="return-value"></a>Rückgabewert

Gibt einen Ganzzahlwert zurück, der den aktuellen bevorzugten Datenstrom in der Systemregistrierung darstellt.

## <a name="remarks"></a>Hinweise

Der bevorzugte Unterbilddatenstrom wird mit der [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md)des [MSDVDAdm-Objekts](msdvdadm-object.md) festgelegt.

 

 



