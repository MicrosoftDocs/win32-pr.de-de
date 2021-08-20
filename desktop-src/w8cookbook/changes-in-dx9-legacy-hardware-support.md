---
title: Änderungen an der DX9-Legacyhardwareunterstützung
description: Änderungen an der DX9-Legacyhardwareunterstützung
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfd0b8bbb05161ffe14ff57cc5db97fe88a22bf6e64a495e2b43dd8240def82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211806"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a>Änderungen an der DX9-Legacyhardwareunterstützung

## <a name="platform"></a>Plattform

**Clients** – Windows 8 


## <a name="description"></a>Beschreibung

Intel und AMD/ATI unterstützen ihre DX9-Grafikteile nicht mehr und aktualisieren keine Treiber für diese Geräte für Windows 8. Darüber hinaus werden diese Geräte nicht im Feld für Windows 8. Die letzten Treiber für diese Geräte sind diejenigen, die auf WU und auf den Websites des OEM/IHV verfügbar sind. viele Datums- und Zielversionen von Vista, und viele dieser endgültigen Versionstreiber weisen Probleme Windows 8. Darüber hinaus hat nVidia kürzlich erklärt, dass sie ihre DX9-Teile (Vista und ältere) mobile (Notebook)-Teile für Windows 8. Sie unterstützen weiterhin ihre DX9-Desktopteile.

Alle diese Treiber-/Teilkombinationen befinden sich in der Internet Explorer 9-Softwarefallbackliste. Dies bedeutet, dass Internet Explorer 9 aus Leistungs- oder Stabilitätsgründen Softwarerendering auf diesen Geräten verwendet. Dies ist ein guter Hinweis darauf, dass die Erfahrung mit Windows Store-Apps für diese Treiber und Teile nicht zufriedenstellend ist.

## <a name="manifestation"></a>Manifestation

Da für diese Geräte keine unterstützungsbasierte Unterstützung verfügbar ist, werden viele Benutzer mit diesen Teilen auf dem Microsoft Basic-Anzeigetreiber ausgeführt. Dies ist eine WARP-basierte WDDM 1.2-Software-GPU und ist tatsächlich schneller als einige teile in dieser Klasse, z. B. die Intel GMA500-Serie). Es unterstützt Die-Glass-App und DWM und kann Windows Store ausführen.

Es gelten jedoch einige wichtige Einschränkungen:

-   Mehrere Monitore oder Projektionen werden nicht unterstützt.
-   Der Ruhezustand wird nicht unterstützt, aber der Ruhezustand wird unterstützt.
-   Häufig ist es nicht möglich, die Bildschirmauflösung zu ändern.

## <a name="mitigation"></a>Minderung

Wenn Sie nach dem Testen feststellen, dass die Benutzeroberfläche nicht akzeptabel ist, können Sie Hardwareanforderungen für die Produkte festlegen, die diese älteren DX9 Intel- und AMD-Teile ausschließen. Sie können Ihre Kunden auch darauf aufmerksam machen, dass sie in diesen Teilen möglicherweise eine inakzeptable Erfahrung haben.

## <a name="tests"></a>Tests

Bewerten Sie die Leistung und Benutzererfahrung auf diesen Geräten:

-   Wie sieht die Erfahrung mit der endgültigen verfügbaren Treiberversion aus?
-   Wie sieht die Erfahrung auf dem MSBDD aus?

 

 




