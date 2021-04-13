---
title: Durchführen der DRM-Individualisierung
description: Durchführen der DRM-Individualisierung
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- Windows Media-Format-SDK, erweiterte DRM-Client-APIs
- Windows Media-Format-SDK, erweiterte Client-APIs
- Windows Media-Format-SDK, erweiterte APIs
- SDK für Windows Media-Format, APIs
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Windows Media-Format-SDK, DRM-Individualisierung
- Windows Media-Format-SDK, Individualisierung
- Digital Rights Management (DRM), erweiterte Client-APIs
- DRM (Digital Rights Management), erweiterte Client-APIs
- Digital Rights Management (DRM), erweiterte APIs
- DRM (Digital Rights Management), erweiterte APIs
- Digital Rights Management (DRM), APIs
- DRM (Digital Rights Management), APIs
- Digital Rights Management (DRM), Individualisierung
- DRM (Digital Rights Management), Individualisierung
- Digital Rights Management (DRM), DRM-Individualisierung
- DRM (Digital Rights Management), DRM-Individualisierung
- Erweiterte APIs für den DRM-Client, Individualisierung
- Erweiterte Client-APIs, Individualisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d8f7f04add4ed626985651d5220e69ea713e4d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310896"
---
# <a name="performing-drm-individualization"></a>Durchführen der DRM-Individualisierung

Die Individualisierung ist der Prozess, bei dem die DRM-Komponente auf dem Client Computer aktualisiert, verschlüsselt und eindeutig gemacht wird. Wenn ein Computer individuell ist, ist die DRM-Komponente an den Computer gebunden und kann keinen Inhalt auf einem anderen Computer decodieren. Die erweiterten APIs des Windows Media DRM-Clients bieten Unterstützung für die individuelle Bereitstellung der DRM-Komponente auf Client Computern.

Die Individualisierung wird durch Aufrufen der Methode [**iwmdrmsecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) durchgeführt. Sie können " **performsecurityupdate** " so aufzurufen, dass es nur dann individualisiert wird, wenn die Version auf dem Server neuer ist als die auf dem Client Computer installierte Version, oder Sie können die individuelle Personalisierung ohne Berücksichtigung der relativen Sicherheits Versionen erzwingen. Das Flag für die Bedarfs gesteuerte Individualisierung ist WMDRM \_ Security \_ Durchführen von \_ indiv. Das Flag für die erzwungene Individual alisierung ist WMDRM \_ Security do \_ \_ Force \_ indiv.

**Performsecurityupdate** ist ein asynchroner-Befehl. Sie wird schnell zurückgegeben und generiert dann Ereignisse, um Statusinformationen zum Individualisierungsprozess bereitzustellen. Die Mehrzahl der generierten Ereignisse sind **mewmdrmindividualizationprogress** -Ereignisse, und jede verfügt über eine zugehörige [**iwmdrmindividualizationstatus**](iwmdrmindividualizationstatus.md) -Schnittstelle. Zum Abrufen der Status Schnittstelle müssen Sie **imfmediaevent:: GetValue** aufrufen, um einen **IUnknown** -Zeiger abzurufen, der sich auf dem gleichen Objekt befindet, und ihn dann für **iwmdrmindividualizationstatus** Abfragen.

Sie können Daten für eine [**WM \_ Individual- \_ Status**](drmwm-individualize-status.md) Struktur abrufen, indem Sie [**iwmdrmindividualizestatus:: GetStatus**](iwmdrmindividualizationstatus-getstatus.md)aufrufen. Jedes Ereignis, das generiert wird, verfügt über ein eigenes Objekt mit dem Status. Sie müssen daher jedes Mal den Ereignis Wert abrufen und die Status Schnittstelle Abfragen.

Abhängig von der Größe des Downloads können Dutzende oder Hunderte von **mewmdrmindividualizationprogress** -Ereignissen vorhanden sein. Wenn der Individualisierungsprozess abgeschlossen ist, wird ein **mewmdrmindividualizationabgeschlossene** -Ereignis generiert.

Wenn die Individualisierung abgeschlossen ist, sind die einzigen Objekte, die den neuen, individualisierten Zustand widerspiegeln, diejenigen, die von [**iwmdrmsecurity**](iwmdrmsecurity.md)erben. Alle anderen vorhandenen Objekte werden nicht aktualisiert. Sie müssen alle anderen Objekte freigeben und neu erstellen, damit Sie den neuen, individualisierten Zustand widerspiegeln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiel für DRM-Individualisierung**](drm-individualization-example.md)
</dt> <dt>

[**Programmierhandbuch**](drm-programming-guide.md)
</dt> <dt>

[**Verwenden des Media Foundation-Ereignis Modells**](using-the-media-foundation-model.md)
</dt> <dt>

[Bewährte Methoden für die Windows Media DRM-Individualisierung](/previous-versions/ms867216(v=msdn.10))
</dt> </dl>

 

 




