---
description: Gibt den Hostnamen des Proxy Servers an.
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: MFNETSOURCE_PROXYHOSTNAME-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc59d5b827276eb5063febf7a8cb7647002ca72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368124"
---
# <a name="mfnetsource_proxyhostname-property"></a>Eigenschaft "MF NetSource \_ proxyhostname"

Gibt den Hostnamen des Proxy Servers an.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

Breit Zeichen-Zeichenfolge (**WCHAR** \* )

VT \_ LPWSTR

**pwszval**



## <a name="remarks"></a>Bemerkungen

Die Konstante " **MF NetSource \_ proxyhostname** " definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um beim Erstellen des proxylocator-Objekts den standardproxylocator zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger im *pproxyconfig* -Parameter der [**mfkreateproxylocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) -Funktion. Diese Eigenschaft muss von der Anwendung festgelegt werden, wenn der proxylocator für den Betrieb im manuellen Modus konfiguriert ist.

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

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Proxy Unterstützung für Netzwerk Quellen](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




