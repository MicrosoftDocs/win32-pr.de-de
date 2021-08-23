---
title: Verwenden des Farbzuordnungsprozesses mit WCS
description: Die WCS-Farbzuordnung basiert auf Geräteprofilen.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- Windows Farbsystem (WCS), Farbzuordnung
- WCS (Windows Color System), Farbzuordnung
- Bildfarbverwaltung, Farbzuordnung
- Farbverwaltung, Farbzuordnung
- Farben,Farbzuordnung
- Farbzuordnung
- Windows Farbsystem (WCS), Geräteprofile
- WCS (Windows Color System), Geräteprofile
- Bildfarbverwaltung, Geräteprofile
- Farbverwaltung, Geräteprofile
- Farben, Geräteprofile
- Windows Farbsystem (WCS), Profile
- WCS (Windows Color System), Profiles
- Bildfarbverwaltung,Profile
- Farbverwaltung,Profile
- Farben,Profile
- Geräteprofile
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe785af9fa4160c2aa1e54c6765857edc9c7aacb1a8fa40a0ad04e634b4ab602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934260"
---
# <a name="using-the-color-mapping-process-with-wcs"></a>Verwenden des Farbzuordnungsprozesses mit WCS

Die WCS-Farbzuordnung basiert auf [Geräteprofilen.](d.md) Diese werden von Anbietern von Farbhardwaregeräten bereitgestellt und installiert, wenn ein Gerät installiert wird. Wenn die Farbzuordnung von einem Anwendungsprogramm verwendet wird, greifen WCS auf das Geräteprofil des Images zu, um die Informationen zu erhalten, die zum Konvertieren des Bilds in den PCS erforderlich sind. Die Konvertierung wird vom CMM durchgeführt.

Ein Geräteprofil kann in das Image selbst eingebettet werden. Das Geräteprofil wird also mit dem Bild übertragen, sogar über das Internet. Ein Benutzer benötigt das Quellgerät nicht, um eine genaue Farbzuordnung zu erhalten. Wenn ein Image nicht über ein Geräteprofil verfügt, wird der sRGB-Speicherplatz standardmäßig verwendet. Weitere Informationen finden Sie unter [Verwenden der Farbverwaltung im Internet.](using-color-management-on-the-internet.md)

Beachten Sie, dass Anwendungen, die WCS verwenden, nie das sRGB-Profil in ein Image einbetten sollten. Der sRGB-Farbraum bietet einen standardisierten Farbraum, der auf allen Geräten portierbar ist. Es ist automatisch für Benutzer ab Windows 98 sowie 2000 Windows 2000 und höher verfügbar. Daher muss er nicht mit dem Bild reisen.

Nachdem sich die Bildfarben im [PCS befinden,](p.md)greifen WCS auf das Geräteprofil des Zielgeräts zu. Es ruft den CMM ab, um die Bildfarben von PCS in die Gamut des Zielgeräts zu konvertieren.

Eine komplexere Farbzuordnung kann auch mit WCS durchgeführt werden. Sie kann beispielsweise verwendet werden, um sich einen Überblick darüber zu verschaffen, wie ein Bild, das auf einer Videoanzeige erstellt wird, aussehen würde, wenn es auf einem hochauflösenden Drucker gedruckt wird. Das Beispiel wird komplexer, wenn es nur einen Standarddrucker für die Vorschau gibt. Das Bild kann aus dem Gamut der Anzeige in den Gamut des Druckers "Printer" konvertiert werden. Von dort aus kann sie in den Gamut des Druckers konvertiert werden. Das resultierende Bild kann auf dem Drucker "Printer" gedruckt werden. Natürlich würde das Bild eine höhere Auflösung haben, wenn es auf dem Farblaserdrucker gedruckt wird. Die Farben des Aufdruckbilds, das auf dem Drucker "Drucker" gedruckt wird, würden jedoch mit den Farben übereinstimmen, die der Drucker drucken würde.

Die Konvertierungen in diesem Beispiel werden durchgeführt, um die Bildfarben aus dem Gamut der Anzeige in die PCS zu konvertieren. Nachdem die Bildfarben in den PCS konvertiert wurden, wird das Geräteprofil des Druckers verwendet, um sie in den Gamut des Druckers zu transformieren. Als Nächstes wird die Gamut to PCS-Transformation verwendet, um die Farben zurück in den PCS zu verschieben. Von dort aus wird das Geräteprofil des Druckers verwendet, um die Farben von PCS in die Gamut des Druckers zu konvertieren.

Die Möglichkeit, Farben problemlos von einem Gerät gamut zum PCS und zurück zu transformieren, ermöglicht es, Bildfarben, die für ein Farbausgabegerät vorgesehen sind, auf fast jedem anderen Gerät zu beweisen.

Im vorherigen Beispiel variiert die Beschreibung aus Gründen der Übersichtlichkeit etwas von der tatsächlichen Prozedur. In Wirklichkeit würden alle im vorherigen Absatz erwähnten Transformationen zu einer einzigen Transformation verkettet werden.

 

 




