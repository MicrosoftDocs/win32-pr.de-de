---
description: Die PKEY \_ AudioEndpoint \_ GUID-Eigenschaft stellt den DirectSound-Gerätebezeichner zur Anwendung, der dem Audioendpunktgerät entspricht.
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357531a76316381e9ae39f867a5b6cfa0a055a04f41b0cba5fab95fcccbcc7fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104360"
---
# <a name="pkey_audioendpoint_guid"></a>\_PKEY-AudioEndpoint-GUID \_

Die **PKEY \_ AudioEndpoint \_ GUID-Eigenschaft** stellt den DirectSound-Gerätebezeichner zur Anwendung, der dem Audioendpunktgerät entspricht. Der Eigenschaftswert ist eine GUID, die der Client als Gerätebezeichner für die **DirectSoundCreate-** oder **DirectSoundCaptureCreate-Funktion** in der DirectSound-API angeben kann. Dieser Wert identifiziert das Audioendpunktgerät auf allen Audioendpunktgeräten im System eindeutig. Weitere Informationen zu DirectSound finden Sie in der DirectX SDK-Dokumentation.

Der **vt-Member** der **PROPVARIANT-Struktur** ist auf VT \_ LPWSTR festgelegt.

Der **pwszVal-Member** der **PROPVARIANT-Struktur** zeigt auf eine null endende Breitzeichenfolge, die eine GUID enthält, die das Audioendpunktgerät in DirectSound identifiziert.

Wie bereits erläutert, unterstützt die [MMDevice-API](mmdevice-api.md) [Geräterollen.](device-roles.md) Obwohl DirectSound Geräterollen nicht direkt unterstützt, kann ein DirectSound-Client die PKEY AudioEndpoint-GUID-Eigenschaft verwenden, um ein DirectSound-Rendering- oder -Erfassungsgerät basierend auf seiner Geräterolle \_ \_ auszuwählen.

Eine DirectSound-Anwendung führt beispielsweise die folgenden Schritte aus, um ein DirectSound-Gerät zu erstellen, das dem Renderingendpunktgerät entspricht, dem der Benutzer die eMultimedia-Rolle zugewiesen hat:

1.  Rufen Sie [**die IMMDeviceEnumerator::GetDefaultAudioEndpoint-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) auf, um die [**IMMDevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) des Renderingendpunktgeräts mit der eMultimedia-Rolle zu erhalten.
2.  Rufen Sie [**die IMMDevice::OpenPropertyStore-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) auf, um die **IPropertyStore-Schnittstelle** des eMultimedia-Geräts zu erhalten. Weitere Informationen zu **IPropertyStore finden** Sie in der Windows SDK-Dokumentation.
3.  Rufen Sie **die IPropertyStore::GetValue-Methode** auf, um den PKEY \_ AudioEndpoint \_ GUID-Eigenschaftswert zu erhalten.
4.  Konvertieren Sie den Eigenschaftswert von einer GUID im Zeichenfolgenformat in eine 16-Byte-GUID-Struktur.
5.  Rufen Sie **die DirectSoundCreate-Funktion** mit der GUID auf, um das Gerät mit der eMultimedia-Rolle zu erstellen.

> [!Note]  
> **PKEY \_ AudioEndpoint \_ GUID** ist eine schreibgeschützte Eigenschaft, unabhängig vom Speicherzugriffsmodus, der von der Anwendung in [**IMMDevice::OpenPropertyStore angefordert wird.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) Wenn eine Anwendung versucht, einen Wert mithilfe von **IPropertyStore::SetValue** festlegen, schlägt dieser Aufruf mit dem Fehlercode E \_ ACCESSDENIED fehl.

 

Beachten Sie, dass die in Schritt 4 generierte 16-Byte-GUID der Geräte-GUID entspricht, die das Gerät während der DirectSound-Geräteenumeration identifiziert. Die **DirectSoundEnumerate-Funktion** aufzählt Renderingendpunktgeräte, und die **DirectSoundCaptureEnumerate-Funktion** aufzählt Erfassungsendpunktgeräte. In beiden Fällen ist die Geräte-GUID der erste Parameter, der an die Enumerationsrückruffunktion übergeben wird. Weitere Informationen zur DirectSound-Enumeration finden Sie in der DirectX SDK-Dokumentation.

Ein Codebeispiel, in dem die Eigenschaft PKEY \_ AudioEndpoint GUID verwendet wird, finden Sie \_ unter [Geräterollen für DirectSound-Anwendungen.](device-roles-for-directsound-applications.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Audioendpunkteigenschaften**](audio-endpoint-properties.md)
</dt> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> </dl>

 

 




