---
title: Tastatur Behandlung in Steuerelementen
description: Tastatur Behandlung in Steuerelementen
ms.assetid: 33affb3f-5d52-4ada-9751-0775b31a375e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f32610732ddbf88c6a587d5bc0fd7de1188152d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338622"
---
# <a name="keyboard-handling-in-controls"></a>Tastatur Behandlung in Steuerelementen

Die Unterstützung der Tastatur Behandlung für die folgenden Funktionen wird dringend empfohlen, auch wenn erkannt wird, dass Sie nicht auf alle Container anwendbar ist.

-   Unterstützung für OLEMISC \_ actslikelabel-und OLEMISC \_ actslikebutton-Status Bits.
-   Implementieren der Eigenschaft DisplayAsDefault Ambient (wenn Sie vorhanden ist, kann Sie **false** zurückgeben).
-   Implementieren von Registerkarten Behandlung, einschließlich Aktivier Reihenfolge

Einige Container verwenden ActiveX-Steuerelemente in herkömmlichen Verbund Dokument Szenarien. Beispielsweise kann ein Benutzer mit einer Tabelle ein ActiveX-Steuerelement in ein Arbeitsblatt einbetten. In solchen Szenarios würde der Container die Tastatur Verarbeitung anders durchführen, da die Tastaturschnittstelle mit den Erwartungen des Benutzers in Übereinstimmung bleiben soll. Die Dokumentation für derartige Produkte sollte Benutzer über Unterschiede bei der Steuerungs Behandlung in diesen verschiedenen Szenarien informieren. Andere Container sollten die oben genannten Funktionen ordnungsgemäß beachten, einschließlich der mnetmonischen Handhabung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Container](containers.md)
</dt> </dl>

 

 




