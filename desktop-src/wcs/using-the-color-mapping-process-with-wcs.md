---
title: Verwenden des Farbzuordnungsprozesses mit WCS
description: Die WCS-Farbzuordnung basiert auf Geräte Profilen.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- Windows Color System (WCS), Farbzuordnung
- WCS (Windows Color System), Farbzuordnung
- Bild Farbverwaltung, Farbzuordnung
- Farbverwaltung, Farbzuordnung
- Farben, Farbzuordnung
- Farbzuordnung
- Windows Color System (WCS), Geräteprofile
- WCS (Windows Color System), Geräteprofile
- Bild Farbverwaltung, Geräteprofile
- Farbverwaltung, Geräteprofile
- Farben, Geräteprofile
- Windows Color System (WCS), profile
- WCS (Windows Color System), profile
- Bildfarben Verwaltung, profile
- Farbverwaltung, profile
- Farben, profile
- Geräteprofile
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 428b09749f3781def44e56ff6cea0539259d0464
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106351181"
---
# <a name="using-the-color-mapping-process-with-wcs"></a>Verwenden des Farbzuordnungsprozesses mit WCS

Die WCS-Farbzuordnung basiert auf [Geräte Profilen](d.md). Diese werden von Herstellern von Color-Hardware Geräten bereitgestellt und bei der Installation eines Geräts installiert. Wenn die Farbzuordnung von einem Anwendungsprogramm verwendet wird, greift WCS auf das Geräte Profil des Abbilds zu, um die Informationen zu erhalten, die zum Konvertieren des Abbilds auf den PCs erforderlich sind. Die Konvertierung erfolgt durch CMM.

Ein Geräte Profil kann in das Abbild selbst eingebettet werden. Das Geräte Profil wird also auch über das Internet mit dem Image bewegt. Ein Benutzer benötigt das Quellgerät nicht, um eine exakte Farbzuordnung zu erhalten. Wenn ein Image nicht über ein Geräte Profil verfügt, wird der sRGB-Speicherplatz als Standard verwendet. Weitere Informationen finden Sie unter [Verwenden der Farbverwaltung im Internet](using-color-management-on-the-internet.md).

Beachten Sie, dass Anwendungen, die WCS verwenden, das sRGB-Profil nie in ein Image einbetten sollten. Der sRGB-Farbraum bietet einen standardisierten Farbraum, der auf allen Geräten portabel ist. Es ist automatisch für Benutzer von Windows 98 und höher sowie Windows 2000 und höher verfügbar. Daher ist es nicht erforderlich, mit dem Image zu reisen.

Nachdem sich die Bildfarben auf den [PCs](p.md)befinden, greift WCS auf das Geräte Profil des Zielgeräts zu. Der CMM-Dienst erhält die Umwandlung der Bildfarben von PCs in den Farbskala des Zielgeräts.

Eine komplexere Farbzuordnung kann auch mit WCS durchgeführt werden. Beispielsweise kann es verwendet werden, um eine Vorstellung davon zu erhalten, wie ein Bild, das in einer Videoanzeige erstellt wurde, auf einem hochauflösenden Laserdrucker gedruckt wird. Das Beispiel wird komplexer, wenn es nur einen Standard-Inkjet-Drucker gibt, in dem die Vorschau angezeigt wird. Das Bild kann aus dem Spiel der Anzeige in den Spiel Schirm des Inkjet-Druckers konvertiert werden. Von dort aus kann es in das Spiel des Laserdruckers konvertiert werden. Das resultierende Bild kann auf dem Inkjet-Drucker gedruckt werden. Natürlich wäre das Image bei der Ausgabe auf dem Color-Laser-Drucker eine höhere Auflösung. Die Farben des auf dem Inkjet-Drucker gedruckten Druck Abbilds entsprechen jedoch der Farbe, die der Laserdrucker drucken würde.

Die Konvertierungen im Beispiel werden durch die Konvertierung der Bildfarben aus dem Farbskala der Anzeige in die PCs konvertiert. Nachdem die Bildfarben in die PCs konvertiert wurden, wird das Geräte Profil des Inkjet-Druckers verwendet, um Sie in die Fläche des Inkjet-Druckers umzuwandeln. Im nächsten Schritt wird die Transformation für PCs zu PCs verwendet, um die Farben zurück auf die PCs zu verschieben. Von dort aus wird das Geräte Profil des Laserdruckers zum Konvertieren der Farben von PCs in den Spiel-des Laserdruckers verwendet.

Durch die Möglichkeit, Farben von einem Geräte Spiel auf PCs und wieder zurück zu transformieren, können Bildfarben, die für ein Farbausgabe Gerät bestimmt sind, auf nahezu jedem anderen Gerät überprüft werden.

Im vorherigen Beispiel unterscheidet sich die Beschreibung von der eigentlichen Prozedur aus Gründen der Übersichtlichkeit. In der Realität werden alle im vorangehenden Absatz erwähnten Transformationen in einer einzigen Transformation verkettet.

 

 




