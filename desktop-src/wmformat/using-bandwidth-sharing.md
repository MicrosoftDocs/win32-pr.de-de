---
title: Verwenden der Bandbreiten Freigabe
description: Verwenden der Bandbreiten Freigabe
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- Windows Media-Format-SDK, Bandbreiten Freigabe
- Bandbreiten Freigabe, Informationen zu
- Profile, Bandbreiten Freigabe
- Streams, Bandbreiten Freigabe
- Bandbreiten Freigabe, iwmprofile-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298c690b484a8b4b5990aacd5d525867da8923c0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104390062"
---
# <a name="using-bandwidth-sharing"></a>Verwenden der Bandbreiten Freigabe

Mit Bandbreiten Freigabe Objekten können Sie angeben, dass bestimmte Datenströme, wenn kombiniert, nicht mehr Bandbreite als angegeben verwenden. Die Informationen in einem Bandbreiten Freigabe Objekt werden weder vom Writer generiert noch überprüft.

Wenn eine Datei mit Informationen zur Bandbreiten Freigabe im Profil geschrieben wird, werden die Daten im Header Abschnitt gespeichert. Sie können die [**iwmprofile**](iwmprofile.md) -Schnittstelle im Reader verwenden, um Informationen zur Bandbreiten Freigabe zu überprüfen, wenn die Datei wiedergegeben wird.

Jedes Bandbreiten Freigabe Objekt wird durch zwei Einstellungen definiert. Die erste ist die Bandbreite, wie durch die Bandbreite und ein Puffer Fenster definiert. Die zweite Einstellung ist ein Typ der Bandbreiten Freigabe, der entweder exklusiv oder partiell sein kann. Exklusive Bandbreiten Freigabe bedeutet, dass die einzelnen Datenströme nacheinander wiedergegeben werden, während partiell bedeutet, dass die Streams gleichzeitig übermittelt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmprofile-Schnittstelle**](iwmprofile.md)
</dt> <dt>

[**IWMProfile3:: addbandwidthsharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)
</dt> <dt>

[**IWMProfile3:: kreatenewbandwidthsharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)
</dt> <dt>

[**IWMProfile3:: getbandwidthsharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)
</dt> <dt>

[**IWMProfile3:: getbandwidthsharingcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

 




