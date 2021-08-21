---
title: Durchführen der DRM-Individualisierung
description: Durchführen der DRM-Individualisierung
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- Windows Medienformat-SDK, erweiterte DRM-Client-APIs
- Windows Medienformat-SDK, erweiterte Client-APIs
- Windows Medienformat-SDK, erweiterte APIs
- Windows Medienformat-SDK, APIs
- Windows Medienformat-SDK, Digital Rights Management (DRM)
- Windows Medienformat-SDK, DRM-Individualisierung
- Windows Medienformat-SDK,Individualisierung
- Digital Rights Management (DRM), Erweiterte Client-APIs
- DRM (Digital Rights Management), Erweiterte Client-APIs
- Digital Rights Management (DRM), Erweiterte APIs
- DRM (Digital Rights Management), Erweiterte APIs
- Digital Rights Management (DRM), APIs
- DRM (Digital Rights Management), APIs
- Digital Rights Management (DRM), Individualisierung
- DRM (Digital Rights Management), Individualisierung
- Digital Rights Management (DRM), DRM-Individualisierung
- DRM (Digital Rights Management), DRM-Individualisierung
- Erweiterte APIs des DRM-Clients, Individualisierung
- Erweiterte Client-APIs, Individualisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c46d2cd6fccd2c6c1a8898a2d0215b6bc62a3655b12412192d1809021747ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027388"
---
# <a name="performing-drm-individualization"></a>Durchführen der DRM-Individualisierung

Bei der Individualisierung wird die DRM-Komponente auf dem Clientcomputer aktualisiert, verschlüsselt und eindeutig gemacht. Wenn ein Computer individualisiert wird, ist die DRM-Komponente an den Computer gebunden und kann keine Inhalte auf einem anderen Computer decodieren. Die erweiterten APIs Windows Media DRM-Clients bieten Unterstützung für die Individualisierung der DRM-Komponente auf Clientcomputern.

Die Individualisierung erfolgt durch Aufrufen der [**IWMDRMSecurity::P erformSecurityUpdate-Methode.**](iwmdrmsecurity-performsecurityupdate.md) Sie können **PerformSecurityUpdate** so aufrufen, dass es nur individualisiert wird, wenn die Version auf dem Server neuer ist als die auf dem Clientcomputer installierte Version, oder Sie können die Individualisierung ohne Berücksichtigung der relativen Sicherheitsversionen erzwingen. Das Flag für die bedarfsorientierte Individualisierung ist WMDRM \_ SECURITY \_ PERFORM \_ INDIV. Das Flag für die erzwungene Individualisierung ist WMDRM \_ SECURITY \_ PERFORM FORCE \_ \_ INDIV.

**PerformSecurityUpdate** ist ein asynchroner Aufruf. Sie gibt schnell zurück und generiert dann Ereignisse, um Statusinformationen zum Individualisierungsprozess bereitzustellen. Bei den meisten generierten Ereignissen handelt es sich um **MEWMDRMIndividualizationProgress-Ereignisse,** denen jeweils eine [**IWMDRMIndividualizationStatus-Schnittstelle**](iwmdrmindividualizationstatus.md) zugeordnet ist. Um die Statusschnittstelle abzurufen, müssen Sie **EINEN** **IUnknown-Zeiger** aufrufen, der sich im selben Objekt befindet, und ihn dann nach **IWMDRMIndividualizationStatus** abfragen.

Sie können Daten für eine [**WM \_ INDIVIDUALIZE \_ STATUS-Struktur**](drmwm-individualize-status.md) abrufen, indem [**Sie IWMDRMIndividualizeStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md)aufrufen. Jedes Ereignis, das generiert wird, verfügt über ein eigenes Objekt mit status. Daher müssen Sie jedes Mal den Vorgang zum Abrufen des Ereigniswerts und abfragen, um die Statusschnittstelle abzufragen.

Abhängig von der Größe des Downloads können Dutzende oder Hunderte von **MEWMDRMIndividualizationProgress-Ereignissen** vorhanden sein. Wenn der Individualisierungsprozess abgeschlossen ist, wird ein **MEWMDRMIndividualizationCompleted-Ereignis** generiert.

Wenn die Individualisierung abgeschlossen ist, sind die einzigen vorhandenen Objekte, die den neuen individualisierten Zustand widerspiegeln, diejenigen, die von [**IWMDRMSecurity**](iwmdrmsecurity.md)erben. Alle anderen vorhandenen Objekte werden nicht aktualisiert. Sie müssen alle anderen Objekte freigeben und neu erstellen, damit sie den neuen individualisierten Zustand widerspiegeln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiel für die DRM-Individualisierung**](drm-individualization-example.md)
</dt> <dt>

[**Programmierhandbuch**](drm-programming-guide.md)
</dt> <dt>

[**Verwenden des Media Foundation-Ereignismodells**](using-the-media-foundation-model.md)
</dt> <dt>

[Windows Bewährte Methoden für die Media DRM-Individualisierung](/previous-versions/ms867216(v=msdn.10))
</dt> </dl>

 

 




