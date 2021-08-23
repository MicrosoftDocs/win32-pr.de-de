---
description: Das WiA-Scannergerät (Windows Image Acquisition) wird als hierarchische Struktur von IWiaItem-Objekten implementiert.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: WIA-Scannergeräte in WIA 1.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd22cc9fe330a3acf231034b61c72178f3b282cb9e66a1f455d4b6939a1c3cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592670"
---
# <a name="wia-scanner-devices-in-wia-10"></a>WIA-Scannergeräte in WIA 1.0

> [!Note]  
> In diesem Thema wird die Scannergerätestruktur für Anwendungen erläutert, die den Wia 1.0-Dienst (Windows Image Acquisition) verwenden (der auf Windows XP oder früher unterstützt wird). Informationen zur Gerätestruktur von Windows Wia 2.0-Elementen (Image Acquisition, Bilderfassung) (die auf Windows Vista oder höher unterstützt werden) finden Sie unter [Informationen zur IWiaItem2-Elementstruktur.](-wia-about-item-tree.md)

 

Das WiA-Scannergerät (Windows Image Acquisition) wird als hierarchische Struktur von [**IWiaItem-Objekten**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) implementiert. Aus dem Stammelement kann eine Anwendung Folgendes:

-   Funktionen der Abfragescanner
-   Festlegen der Eigenschaften des Scannergeräts
-   Steuern des Dokumentfeeders

Ein WIA-Scannergerät unterscheidet sich von einem WIA-Kameragerät, da es im Allgemeinen nicht mehrere Bilder im Arbeitsspeicher speichert.

Unterhalb des Stammelements verfügt ein typisches Scannerobjekt über ein einzelnes [**IWiaItem-Objekt,**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) das die Datensammlungsfunktionalität des Geräts darstellt, das Scanelement. Für dieses Element ist das [**WiaItemTypeFile-Flag**](-wia-wia-item-type-flags.md) festgelegt, um anzugeben, dass Datenübertragungen für dieses Element möglich sind. Eine Anwendung richtet eine Überprüfung durch Festlegen der Eigenschaften des Scanelements ein, führt dann die Überprüfung durch und überträgt die Daten über eine Datenübertragungsschnittstelle.

Das folgende Diagramm veranschaulicht die WIA-Implementierung für einen typischen Scanner:

![wia-Implementierung eines typischen Scanners](images/wiscantr.gif)

Ein typischer Duplexscanner wird in WIA durch ein [**IWiaItem-Objekt**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) dargestellt. Auf Front-Page- und Back-Page-Daten wird sequenziell eine Datenübertragung pro Seite zugegriffen. Daher ist die Darstellung eines Duplexscanners mit der Darstellung eines typischen Scanners identisch.

Ein Diascanner, der mehrere Folien in einem einzelnen Scanvorgang scannen kann, stellt jedes separate Bild als separates [**IWiaItem-Objekt**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) dar.

Das folgende Diagramm veranschaulicht die WIA-Darstellung eines Diascanners:

![Schieberegler](images/wislscan.gif)

 

 



