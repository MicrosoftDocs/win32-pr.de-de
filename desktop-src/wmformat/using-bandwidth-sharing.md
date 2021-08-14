---
title: Verwenden der Bandbreitenfreigabe
description: Verwenden der Bandbreitenfreigabe
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- Windows Medienformat-SDK, Bandbreitenfreigabe
- Bandbreitenfreigabe, Informationen
- Profile,Bandbreitenfreigabe
- Streams, Bandbreitenfreigabe
- Bandbreitenfreigabe, IWMProfile-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7259ddf441a4e32eb7eb4aea19a52d633c6aacd3a27ad6d392e4fea41c3f4fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845156"
---
# <a name="using-bandwidth-sharing"></a>Verwenden der Bandbreitenfreigabe

Sie können Bandbreitenfreigabeobjekte verwenden, um anzugeben, dass bestimmte Streams in Kombination nicht mehr Bandbreite als angegeben verwenden. Die Informationen in einem Bandbreitenfreigabeobjekt werden weder vom Writer generiert oder überprüft noch vom Reader für etwas verwendet.

Wenn eine Datei geschrieben wird, deren Profil Informationen zur Bandbreitenfreigabe enthält, werden die Daten im Headerabschnitt gespeichert. Sie können die [**IWMProfile-Schnittstelle**](iwmprofile.md) im Reader verwenden, um nach Informationen zur Bandbreitenfreigabe zu überprüfen, wenn die Datei abgespielt wird.

Jedes Bandbreitenfreigabeobjekt wird durch zwei Einstellungen definiert. Erstens ist die Bandbreite, wie durch eine Bandbreite und ein Pufferfenster definiert. Die zweite Einstellung ist ein Bandbreitenfreigabetyp, der entweder exklusiv oder partiell sein kann. Exklusive Bandbreitenfreigabe bedeutet, dass die konstituierenden Streams nach und nach abgespielt werden, während teilteilig bedeutet, dass die Streams gleichzeitig übermittelt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMProfile-Schnittstelle**](iwmprofile.md)
</dt> <dt>

[**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)
</dt> <dt>

[**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)
</dt> <dt>

[**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)
</dt> <dt>

[**IWMProfile3::GetBandwidthSharingCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

 




