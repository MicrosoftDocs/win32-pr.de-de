---
title: Implementieren eines benutzerdefinierten Audioendpunkt-Enumerators
description: Ab Windows Server 2008 R2 können Sie einen benutzerdefinierten Enumerator für Remoteaudioendpunkte als Teil eines Remotedesktop Protokollanbieters implementieren.
ms.assetid: 684bd62e-1e28-4330-a3c5-6bce684d652d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ae135d19e13e3b78fddbdd58bccd476b7e5ee7a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478856"
---
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a>Implementieren eines benutzerdefinierten Audioendpunkt-Enumerators

Ab Windows Server 2008 R2 können Sie einen benutzerdefinierten Enumerator für Remoteaudioendpunkte als Teil eines Remotedesktop Protokollanbieters implementieren. Ein Remotedesktop Protokollanbieter kann einen benutzerdefinierten Audioendpunkt-Enumerator verwenden, um eine Sammlung von Audioendpunkten abzurufen, die über einen bestimmten Satz von Funktionen verfügen.

**So implementieren Sie einen benutzerdefinierten Enumerator für Remoteaudioendpunkte**

1.  Ihre benutzerdefinierte Endpunktenumeratorlösung sollte vier Haupttypen von Objekten implementieren: Geräteenumeratorobjekte, Gerätesammlungsobjekte, Geräteobjekte und Eigenschaftenspeicherobjekte.

    

    
| Objekttyp | Beschreibung | 
|-------------|-------------|
| Geräteenumeratorobjekt<br /> | Ein Geräteenumeratorobjekt stellt die Endpunktenumeratorfunktionalität bereit. Sie macht Methoden verfügbar, die einen Standardendpunkt und angegebene Auflistungen von Endpunkten zurückgeben. Abhängig von den angegebenen Kriterien kann der Enumerator beispielsweise Kommunikationsendpunkte, Wiedergabeendpunkte oder Erfassungsendpunkte zurückgeben. Das Geräteenumeratorobjekt muss die <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator-Schnittstelle</strong></a> implementieren.<br /> | 
| Gerätesammlungsobjekt<br /> | Ein Gerätesammlungsobjekt stellt eine Sammlung von Audiogeräten dar. Sie muss die <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection-Schnittstelle</strong></a> implementieren.<br /> | 
| Geräteobjekt<br /> | Ein Geräteobjekt stellt ein bestimmtes Audiogerät dar. Sie bietet Zugriff auf den Eigenschaftenspeicher des Audiogeräts und macht die audiowiedergabe- und erfassungsschnittstellen verfügbar, die auf dem Gerät verfügbar sind. Das Geräteobjekt muss die <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>SCHNITTSTELLEN IMMDevice</strong></a> und <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> implementieren.<br /> | 
| Eigenschaftenspeicherobjekt<br /> | Ein Eigenschaftenspeicherobjekt macht die einem Audiogerät zugeordneten Eigenschaften verfügbar. Einige dieser Eigenschaften werden vom System verwendet, aber Anwendungen können beliebige Eigenschaften auch mit dem Audioendpunkt speichern.<br /> Alle Audiogeräte verfügen über die folgenden drei Eigenschaften:<br /><ul><li><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></li><li><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></li><li><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></li></ul>    Das Eigenschaftenspeicherobjekt muss die <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore-Schnittstelle</a> implementieren.<br /> | 


    

     

2.  Der benutzerdefinierte Endpunktenumerator muss in einer DLL implementiert werden, die in das Audiosystem und andere Anwendungen geladen werden kann. Die DLL muss signiert sein, damit sie von sicheren Prozessen geladen werden kann. Die DLL muss die [**GetTSAudioEndpointEnumeratorForSession-Funktion**](gettsaudioendpointenumeratorforsession.md) implementieren und exportieren, die als Einstiegspunkt für den benutzerdefinierten Endpunktenumerator fungiert.

Der Remotedesktopdienste-Dienst ruft die [**QueryProperty-Methode**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) auf und legt den *QueryType-Parameter* auf **WTS QUERY \_ \_ AUDIOENUM \_ DLL** fest, um den Namen des Enumeratorobjekts abzurufen.

Benutzerdefinierte Enumeratorobjekte verwenden COM-ähnliche Schnittstellen und einen COM-ähnlichen Verweiszählungsmechanismus, sind jedoch keine echten COM-Objekte. Der benutzerdefinierte Endpunkt-Enumerator muss in der Lage sein, mit älteren Audioschnittstellen zu arbeiten, die von Anwendungen verwendet werden, die COM nicht unterstützen. Aus diesem Grund darf sich der benutzerdefinierte Endpunktenumerator nicht auf den Lebenszyklusverwaltungsmechanismus von COM verlassen. Consumer ihres Audioenumerators, z. B. MMDevAPI.dll, laden die benutzerdefinierte Endpunktenumerator-DLL, wenn dies für Benutzeranwendungen erforderlich ist, und entladen den Enumerator nicht, während der Enumerator einen Verweis auf ein Geräteenumeratorobjekt, ein Gerätesammlungsobjekt, ein Geräteobjekt oder ein Eigenschaftenspeicherobjekt enthält. Es ist jedoch nicht möglich, dass diese Consumer Verweise auf andere Objekttypen nachverfolgen, die im Besitz des benutzerdefinierten Endpunktenumerators sind. Daher wird empfohlen, dass Ihr benutzerdefinierter Endpunktenumerator keine Objekte erstellt, die diese vier Objekttypen überdauern könnten.

## <a name="to-implement-a-custom-audio-endpoint"></a>So implementieren Sie einen benutzerdefinierten Audioendpunkt

Um einen benutzerdefinierten Audiogeräte-Enumerator zu implementieren, müssen Sie einen benutzerdefinierten Audioendpunkt implementieren. Die Art und Weise, wie Ihre benutzerdefinierten Audiogeräte verknüpft werden, ist die Verwendung der folgenden beiden -Anweisungen:

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

Wir erwarten nicht, dass Sie die vollständige Liste der [**IMMDevice::Activate-Schnittstellen**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) in Ihrem benutzerdefinierten Audiogeräte-Enumerator implementieren. Stattdessen sollten Sie [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) und [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)implementieren. Sie können optional einige weitere implementieren, z. [**B. IAudioEndpointVolume.**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume) Für jede Schnittstelle, die Sie nicht implementieren, sollten Sie **E \_ NOINTERFACE** zurückgeben (Sie müssen diesen spezifischen Fehlercode verwenden). Windows wird dann auf eine stock-Implementierung der -Schnittstelle (z. B. [**IAudioClient2)**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)zurückgreifen.

Weitere Referenzdokumentationen zum Implementieren und Registrieren von Audioendpunkten finden Sie unter [**IAudioInputEndpointRT.**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) Ein Diagramm, das die Funktionsweise von WASAPI zeigt, finden Sie unter [Benutzermodus-Audiokomponenten.](/windows/desktop/CoreAudio/user-mode-audio-components) Beachten Sie, dass alle Benutzermodusaudiodaten mit Windows Server 2008 neu beginnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Remotedesktopprotokoll-Anbieters](creating-a-custom-remote-protocol.md)
</dt> <dt>

[**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md)
</dt> <dt>

[**IMMDevice**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDeviceCollection**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
</dt> <dt>

[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**IMMEndpoint**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint)
</dt> <dt>

[Ipropertystore](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> </dl>
