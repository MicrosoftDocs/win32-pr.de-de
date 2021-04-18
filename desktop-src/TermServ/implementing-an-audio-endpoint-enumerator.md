---
title: Implementieren eines benutzerdefinierten audioendpunkt-Enumerators
description: Ab Windows Server 2008 R2 können Sie einen benutzerdefinierten remoteaudioendpunkt-Enumerator als Teil eines Remotedesktop Protokoll Anbieters implementieren.
ms.assetid: 684bd62e-1e28-4330-a3c5-6bce684d652d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ab2a572169f20a7f8f9db194449be5361e409
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "106340540"
---
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a>Implementieren eines benutzerdefinierten audioendpunkt-Enumerators

Ab Windows Server 2008 R2 können Sie einen benutzerdefinierten remoteaudioendpunkt-Enumerator als Teil eines Remotedesktop Protokoll Anbieters implementieren. Ein Remotedesktop-Protokoll Anbieter kann einen benutzerdefinierten audioendpunktenumerator zum Abrufen einer Auflistung von audioendpunkten verwenden, die über einen bestimmten Satz von Funktionen verfügen.

**So implementieren Sie einen benutzerdefinierten remoteaudioendpunkt-Enumerator**

1.  Die benutzerdefinierte Endpunkt-enumeratorlösung sollte vier Haupttypen von Objekten implementieren: Geräte Enumeratorobjekte, Geräte Sammlungsobjekte, Geräte Objekte und Eigenschaften Speicher Objekte.

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Objekttyp</th>
    <th>Beschreibung</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Geräte-Enumeratorobjekt<br/></td>
    <td>Ein geräteenumeratorobjekt stellt die Endpunkt-enumeratorfunktion bereit. Es macht Methoden verfügbar, die einen Standard Endpunkt und angegebene Auflistungen von Endpunkten zurückgeben. Abhängig von den angegebenen Kriterien kann der Enumerator z. b. Kommunikations Endpunkte, Wiedergabe Endpunkte oder Aufzeichnungs Endpunkte zurückgeben. Das geräteenumeratorobjekt muss die <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>immdeviceenumerator</strong></a> -Schnittstelle implementieren.<br/></td>
    </tr>
    <tr class="even">
    <td>Geräte Sammlungsobjekt<br/></td>
    <td>Ein Geräte Sammlungsobjekt stellt eine Sammlung von Audiogeräten dar. Es muss die <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>immdebug</strong></a> -Schnittstelle implementieren.<br/></td>
    </tr>
    <tr class="odd">
    <td>Geräteobjekt<br/></td>
    <td>Ein Geräte Objekt stellt ein bestimmtes Audiogerät dar. Sie ermöglicht den Zugriff auf den Eigenschaften Speicher des Audiogeräts und macht die auf dem Gerät verfügbaren Audiowiedergabe-und Erfassungs Schnittstellen verfügbar. Das Device-Objekt muss die <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>immdevice</strong></a> -und die <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>immendpoint</strong></a> -Schnittstelle implementieren.<br/></td>
    </tr>
    <tr class="even">
    <td>Eigenschaften Speicher Objekt<br/></td>
    <td>Ein Eigenschaften Speicher Objekt macht die einem Audiogerät zugeordneten Eigenschaften verfügbar. Einige dieser Eigenschaften werden vom System verwendet, aber Anwendungen können auch beliebige Eigenschaften mit dem audioendpunkt speichern.<br/> Alle Audiogeräte verfügen über die folgenden drei Eigenschaften:<br/>
    <ul>
    <li><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></li>
    <li><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></li>
    <li><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></li>
    </ul>
Das Eigenschaften Speicher Objekt muss die <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> -Schnittstelle implementieren.<br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Der benutzerdefinierte Endpunkt Enumerator muss in einer DLL implementiert werden, die in das Audiosystem und andere Anwendungen geladen werden kann. Die dll muss signiert werden, damit Sie von sicheren Prozessen geladen werden kann. Die dll muss die [**gettsaudioendpointenumeratorforsession**](gettsaudioendpointenumeratorforsession.md) -Funktion implementieren und exportieren, die als Einstiegspunkt für den benutzerdefinierten Endpunkt Enumerator fungiert.

Der Remotedesktopdienste-Dienst ruft die [**queryproperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) -Methode auf und legt den *QueryType* -Parameter auf die **WTS- \_ Abfrage \_ audioenum- \_ dll** fest, um den Namen des Enumeratorobjekts abzurufen.

Benutzerdefinierte Enumeratorobjekte verwenden com-ähnliche Schnittstellen und einen com-ähnlichen Verweis Zählmechanismus, Sie sind jedoch keine echten com-Objekte. Der benutzerdefinierte Endpunkt Enumerator muss mit älteren Audioschnittstellen arbeiten können, die von Anwendungen verwendet werden, die com nicht unterstützen. Aus diesem Grund darf sich der benutzerdefinierte Endpunkt-Enumerator nicht auf den Verwaltungsmechanismus des Lebenszyklus von com verlassen. Consumer Ihres audioendpunktenumerators, wie z. b. MMDevAPI.dll, laden die benutzerdefinierte Endpunkt-enumeratordll, wenn Sie von Benutzer Anwendungen benötigt wird, und entladen den Enumerator nicht, während der Enumerator einen Verweis auf ein Geräte Enumeratorobjekt, ein Geräte Auflistungs Objekt, ein Geräte Objekt oder ein Eigenschafts Speicher Objekt enthält. Es ist jedoch nicht möglich, dass diese Consumer Verweise auf andere Typen von Objekten nachverfolgen, die im Besitz des benutzerdefinierten Endpunkt Enumerators sind. Dementsprechend wird empfohlen, dass der benutzerdefinierte Endpunkt Enumerator keine Objekte erstellt, die diese vier Objekttypen überstehen könnten.

## <a name="to-implement-a-custom-audio-endpoint"></a>So implementieren Sie einen benutzerdefinierten audioendpunkt

Um einen benutzerdefinierten audiogeräteenumerator zu implementieren, müssen Sie einen benutzerdefinierten audioendpunkt implementieren. Die Verknüpfung Ihrer benutzerdefinierten Audiogeräte erfolgt mithilfe der folgenden beiden-Anweisungen:

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

Es ist nicht zu erwarten, dass Sie die vollständige Liste der [**immdevice:: Aktivierungs**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) -Schnittstellen in Ihrem benutzerdefinierten Audiogeräte-Enumerator implementieren. Stattdessen sollten Sie [**iaudiooutputendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) und [**iaudioinputendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)implementieren. Optional können Sie einige weitere implementieren, z. b. [**iaudioendpointvolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume). Für jede Schnittstelle, die Sie nicht implementieren, sollten Sie **E \_ nointerface** zurückgeben (Sie müssen diesen spezifischen Fehlercode verwenden). Windows greift dann auf eine Aktien Implementierung der-Schnittstelle zurück (z. b. [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).

Eine weitere Referenz Dokumentation zum Implementieren und Registrieren von audioendpunkten finden Sie unter [**iaudioinputendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt). Ein Diagramm, das die Funktionsweise von WASAPI zeigt, finden Sie unter [benutzermodusaudiokomponenten](/windows/desktop/CoreAudio/user-mode-audio-components). Beachten Sie, dass alle Benutzermodus-Audiodaten ab Windows Server 2008 neu sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Remotedesktopprotokoll Anbieters](creating-a-custom-remote-protocol.md)
</dt> <dt>

[**Gettsaudioendpointenreeratorforsession**](gettsaudioendpointenumeratorforsession.md)
</dt> <dt>

[**Immdevice**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**Immde vicecollection**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
</dt> <dt>

[**Immdeviceenumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**Immendpoint**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint)
</dt> <dt>

[IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> </dl>