---
description: Das Windows-Abbild Erfassungsgerät (WIA) ist als hierarchische Struktur von iwiaitem-Objekten implementiert.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: WIA-Scanner-Geräte in WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443277b0b580a481b523739cd5bc21642d827252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751760"
---
# <a name="wia-scanner-devices-in-wia-10"></a>WIA-Scanner-Geräte in WIA 1,0

> [!Note]  
> In diesem Thema wird die Überprüfung der Gerätestruktur für Anwendungen erläutert, die den Windows-Abbild Erfassungs Dienst (WIA) 1,0 verwenden (der unter Windows XP oder früher unterstützt wird). Informationen zur Gerätestruktur von Windows-Abbild Erfassungs Elementen (WIA) 2,0 (die unter Windows Vista oder höher unterstützt werden) finden Sie unter [Informationen zur IWiaItem2-Element](-wia-about-item-tree.md)Struktur.

 

Das Windows-Abbild Erfassungsgerät (WIA) ist als hierarchische Struktur von [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Objekten implementiert. Aus dem Stamm Element kann eine Anwendung folgende Aktionen ausführen:

-   Funktionen für Abfrage Scanner
-   Festlegen der Eigenschaften von Scanner-Geräten
-   Steuern des Dokument Anlegers

Ein WIA-Überprüfungs Gerät unterscheidet sich von einem WIA-Kamera Gerät, da es im Allgemeinen nicht mehrere Abbilder im Arbeitsspeicher speichert.

Unterhalb des Stamm Elements verfügt ein typisches Scanner-Objekt über ein einzelnes [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Objekt, das die Daten Sammlungs Funktionen des Geräts darstellt, das Scan Element. Für dieses Element ist das [**wiaitemtypefile**](-wia-wia-item-type-flags.md) -Flag festgelegt, um anzugeben, dass Datenübertragungen für dieses Element möglich sind. Eine Anwendung richtet einen Scan durch Festlegen der Eigenschaften des Überprüfungs Elements ein, führt die Überprüfung durch und überträgt die Daten mithilfe einer Datenübertragungs Schnittstelle.

Das folgende Diagramm veranschaulicht die WIA-Implementierung für einen typischen Scanner:

![WIA-Implementierung eines typischen Scanners](images/wiscantr.gif)

Ein typischer Duplex Scanner wird in WIA durch ein [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Objekt dargestellt. Der Zugriff auf Front-und Back-Page-Daten erfolgt sequenziell auf eine Datenübertragung pro Seite. Daher ist die Darstellung eines Duplex Scanners mit der Darstellung eines typischen Scanners identisch.

Ein Folien Scanner, der mehrere Folien in einem einzelnen Scanvorgang scannen können, stellt jedes separate Bild als separates [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Objekt dar.

Das folgende Diagramm veranschaulicht die WIA-Darstellung eines Folien Scanners:

![Folien Scanner](images/wislscan.gif)

 

 



