---
description: Die DVDAdm.DefaultAudioLCID-Eigenschaft legt die Registrierungseinstellung für die vom Benutzer angegebene Standard-LCID für den Audiostream fest oder ruft sie ab.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: DefaultAudioLCID-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7ebcd864f8ac3bff8cfd8556703dd091985a72c0dfea4f0eefb9f974213165
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953005"
---
# <a name="defaultaudiolcid-property"></a>DefaultAudioLCID-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die -Eigenschaft legt die Registrierungseinstellung für die vom Benutzer angegebene Standard-LCID für den Audiostream fest `DVDAdm.DefaultAudioLCID` oder ruft sie ab.

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a>Rückgabewert

Gibt einen Ganzzahlwert zurück, der die vom Benutzer angegebene Standardaudio-LCID darstellt, die in den Registrierungseinstellungen für die DVD-Anwendung gespeichert ist. Dieser Wert ist nicht notwendigerweise mit dem Standardaudiostream identisch, der auf der DVD erstellt wurde.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist Lese-/Schreibzugriff ohne Standardwert. Wenn keine Standardaudio-LCID angegeben ist, gibt das MSDVDAdm-Objekt den Audiostream wieder, der als Standardstream auf dem Datenträger markiert ist.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MSDVDAdm-Objekt](msdvdadm-object.md)
</dt> </dl>

 

 



