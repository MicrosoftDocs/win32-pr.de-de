---
title: Änderungen in DX9 Legacy Hardwareunterstützung
description: Änderungen in DX9 Legacy Hardwareunterstützung
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1ae5c4b15a2019450cc5b209f34561d8ec672d
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "106341969"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a>Änderungen in DX9 Legacy Hardwareunterstützung

## <a name="platform"></a>Plattform

**Clients** – Windows 8 


## <a name="description"></a>BESCHREIBUNG

Intel und AMD/ATI unterstützen Ihre DX9-Grafik Teile nicht mehr und aktualisieren die Treiber für diese Geräte nicht für Windows 8. Außerdem werden diese Geräte nicht in Box für Windows 8 behandelt. Die letzten Treiber für diese Geräte sind auf Wu und auf den Websites von OEM/IHV verfügbar. viele Datumsangaben von Vista, und viele dieser endgültigen Versions Treiber zeigen Probleme unter Windows 8 an. Außerdem hat NVIDIA vor kurzem festgestellt, dass Ihre DX9-(Vista und ältere) mobilen (Notebook-) Teile für Windows 8 nicht unterstützt werden. Sie unterstützen weiterhin Ihre Desktop-DX9-Teile.

Alle diese Treiber/Teil-Kombinationen finden Sie in der Internet Explorer 9-Software Fall Back Liste. Dies bedeutet, dass Internet Explorer 9 aus Leistungs-oder Stabilitätsgründen das Software Rendering auf diesen Geräten verwendet. Dies ist ein guter Hinweis darauf, dass die Verwendung von Windows Store-Apps für diese Treiber und Teile nicht zufriedenstellend ist.

## <a name="manifestation"></a>Ausstrahlung

Da es keine Unterstützung für diese Geräte gibt, werden viele Benutzer mit diesen Teilen auf dem Microsoft Basic-Anzeigetreiber ausgeführt. Dabei handelt es sich um eine auf Warp basierende WDDM 1,2-softwaregpu, die tatsächlich schneller ist als einige der Teile in dieser Klasse, z. b. die Intel GMA500-Serie). Es werden Aero-Glass und DWM unterstützt, und es können Windows Store-Apps ausgeführt werden.

Es bestehen jedoch einige wichtige Einschränkungen:

-   Es unterstützt nicht mehrere Monitore oder Projektionen.
-   Der Standbymodus wird nicht unterstützt, obwohl er Ruhe Zustands unterstützt.
-   Das Ändern der Bildschirmauflösung wird häufig nicht zugelassen.

## <a name="mitigation"></a>Minderung

Wenn Sie nach dem Testen feststellen, dass die Benutzer Leistung nicht akzeptabel ist, können Sie Hardwareanforderungen für Ihre Produkte festlegen, die diese älteren DX9 Intel-und AMD-Komponenten ausschließen. Sie können auch eine Warnung für Ihre Kunden angeben, dass Sie für diese Teile möglicherweise nicht akzeptabel sind.

## <a name="tests"></a>Tests

Bewerten Sie die Leistung und die Leistung auf diesen Geräten:

-   Wie sieht die endgültige Treiber Version aus?
-   Wie sieht das auf msbdd aus?

 

 




