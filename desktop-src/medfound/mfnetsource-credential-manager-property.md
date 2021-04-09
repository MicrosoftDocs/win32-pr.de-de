---
description: Enthält einen Zeiger auf die imfnetkredentialmanager-Schnittstelle.
ms.assetid: c0826956-9df1-40ec-8ad1-9e0dca34d847
title: MFNETSOURCE_CREDENTIAL_MANAGER-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3447369cedfa5c516e1d7696aae70834c6ce89a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130116"
---
# <a name="mfnetsource_credential_manager-property"></a>MF-Quelle \_ Credential \_ Manager (Eigenschaft)

Enthält einen Zeiger auf die [**imfnetkredentialmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) -Schnittstelle. Verwenden Sie diese Eigenschaft, um die Implementierung von [**imfnetkredentialmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) der Anwendung an die Netzwerkquelle zu übergeben.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**IUnknown** -Zeiger

VT \_ unbekannt

**punkVal**



## <a name="remarks"></a>Bemerkungen

Der Konstante **MF-Quell Anmelde Informations \_ \_ Manager** definiert die **GUID** für den Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Netzwerk Quellen Authentifizierung](network-source-authentication.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




