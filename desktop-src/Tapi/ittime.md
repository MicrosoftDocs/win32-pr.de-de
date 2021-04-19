---
description: Die ittime-Schnittstelle ist eine anbieterspezifische Schnittstelle für ein Sitzungs Deskriptor Protocol (SDP)-Konferenz-BLOB-Objekt.
ms.assetid: 24d33259-dcbe-47e4-9c71-fcc25f6e9a76
title: Ittime-Schnittstelle (sdpblb. h)
ms.topic: interface
ms.date: 05/31/2018
ms.openlocfilehash: 964fa197318d8cbe9614beb97c5bea0db94f242b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354104"
---
# <a name="ittime-interface"></a>Ittime-Schnittstelle

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **ittime** -Schnittstelle ist eine anbieterspezifische Schnittstelle für ein Sitzungs Deskriptor Protocol (SDP)-Konferenz-BLOB-Objekt. Sie ermöglicht den Zugriff auf einen Satz von Aktivierungs Zeiten für die Sitzung. Die [**ienumtime:: Next**](ienumtime-next.md) -Methode und die [**ittimecollection:: Create**](ittimecollection-create.md) -Methode erstellen die **ittime** -Schnittstelle.

## <a name="members"></a>Member

Die **ittime** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ittime** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ittime** -Schnittstelle verfügt über diese Methoden.



| Methode                                         | BESCHREIBUNG                                                                 |
|:-----------------------------------------------|:----------------------------------------------------------------------------|
| [**\_StartTime aufrufen**](ittime-get-starttime.md) | Ruft den Start Zeitwert der 32-Bit-NTP (Netzwerk Zeitprotokoll) ab.<br/> |
| [**\_Stopp Zeit erhalten**](ittime-get-stoptime.md)   | Ruft den NTP-Endzeit Wert ab.<br/>                                  |
| [**\_StartTime ablegen**](ittime-put-starttime.md) | Legt den Wert von 32-Bit-NTP-Start Zeitwert fest.<br/>                         |
| [**\_Stopp Zeit einfügen**](ittime-put-stoptime.md)   | Legt den NTP-Endzeit Wert fest.<br/>                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

