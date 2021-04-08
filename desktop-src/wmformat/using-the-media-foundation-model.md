---
title: Verwenden des Media Foundation-Ereignis Modells
description: Verwenden des Media Foundation-Ereignis Modells
ms.assetid: c07425dc-25d0-430b-a1f6-6373303a0cc7
keywords:
- Windows Media-Format-SDK, DRM Media Foundation-Ereignis Modell
- Windows Media-Format-SDK, Media Foundation-Ereignis Modell
- Windows Media-Format-SDK, DRM-Ereignis Modell
- Digital Rights Management (DRM), Media Foundation-Ereignis Modell
- DRM (Digital Rights Management), Media Foundation-Ereignis Modell
- Digital Rights Management (DRM), Ereignis Modell
- DRM (Digital Rights Management), Ereignis Modell
- Digital Rights Management (DRM), iwmdrmeventgenerator-Schnittstelle
- DRM (Digital Rights Management), iwmdrmeventgenerator-Schnittstelle
- Media Foundation
- Iwmdrmeventgenerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58d48157072cf8814ff8ac74d97a965f9e772e3
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104038626"
---
# <a name="using-the-media-foundation-event-model"></a>Verwenden des Media Foundation-Ereignis Modells

Die asynchronen Methoden, die von den erweiterten APIs des Windows Media DRM-Clients unterstützt werden, verwenden dasselbe Ereignis Modell, das vom Media Foundation SDK verwendet wird. Jedes Objekt, das asynchrone Methoden unterstützt, implementiert die [**iwmdrmeventgenerator**](iwmdrmeventgenerator.md) -Schnittstelle, die verwendet werden kann, um ein Ereignis abzurufen, wenn ein asynchroner Vorgang beendet ist.

Die **iwmdrmeventgenerator** -Schnittstelle erbt von der **IMF mediaeventgenerator** -Schnittstelle, die in der Media Foundation SDK-Dokumentation dokumentiert ist.

Der Beispielcode im Beispiel für eine [DRM-Individualisierung](drm-individualization-example.md) verwendet die **imfmediaeventgenerator:: GetEvent** -Methode, um Ereignisse einzeln aus der Warteschlange abzurufen. Die Verwendung von **GetEvent** ist einfacher als die Verwendung von **imfmediaeventgenerator:: begingetevent** und **imfmediaeventgenerator:: endgetevent** mit einem Rückruf, wodurch die Codebeispiele leichter verständlich werden. Unabhängig davon, ob Sie **GetEvent** in Ihrem Code verwenden oder **imfasynccallback** implementieren und **begingetevent** und **endgetevent** verwenden, ist die Logik zum Verarbeiten des Ereignisses nach dem Empfang identisch.

Einige der asynchronen Methoden generieren Ereignisse, die Verweise auf Objekte enthalten, die zum Abrufen ausführlicherer Statusinformationen verwendet werden können. In diesen Fällen weist das generierte Ereignis einen **IUnknown** -Zeiger als Wert auf, der abgefragt werden kann, um die Status Schnittstelle abzurufen. In der folgenden Liste werden die Beziehungen zwischen asynchronen Aufrufen, generierten Ereignissen und anderen Schnittstellen zusammengefasst.

-   Die [**iwmdrmlicensmanagement:: backuplicenses**](iwmdrmlicensemanagement-backuplicenses.md) -Methode generiert **mewmdrmlicenabbackupprogress** -Ereignisse mit zugeordneten [**iwmdrmlicenabbackuprestorestatus**](iwmdrmlicensebackuprestorestatus.md) -Schnittstellen.
-   Die [**iwmdrmlicensemanagement:: restorelicenses**](iwmdrmlicensemanagement-restorelicenses.md) -Methode generiert **mewmdrmlicenserestoreprogress** -Ereignisse mit zugeordneten [**iwmdrmlicensebackuprestorestatus**](iwmdrmlicensebackuprestorestatus.md) -Schnittstellen.
-   Die [**iwmdrmsecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) -Methode, wenn Sie zur Durchführung von Individualisierungen verwendet wird, generiert **mewmdrmindividualizationprogress** -Ereignisse mit zugeordneten [**iwmdrmindividualizationstatus**](iwmdrmindividualizationstatus.md) -Schnittstellen.
-   Wenn die [**iwmdrmlicensemanagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) -Methode zum Vorbereiten von Daten für den nicht automatischen Lizenz Abruf verwendet wird, wird ein **mewmdrmlicenseacquisitionabgeschlossene** -Ereignis mit einer zugeordneten [**iwmdrmnonsilentlicenseaquisition**](iwmdrmnonsilentlicenseaquisition.md) -Schnittstelle generiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiel für DRM-Individualisierung**](drm-individualization-example.md)
</dt> <dt>

[**Einstieg**](drm-getting-started.md)
</dt> <dt>

[Media Foundation SDK-Dokumentation](https://www.microsoft.com/?ref=go)
</dt> </dl>

 

 




