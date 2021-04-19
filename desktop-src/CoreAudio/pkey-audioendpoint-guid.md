---
description: Die pkey \_ audioendpoint \_ GUID-Eigenschaft stellt den DirectSound-Geräte Bezeichner bereit, der dem audioendpunktgerät entspricht.
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45405cd2350777e535b50859e77aa56755d191fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346247"
---
# <a name="pkey_audioendpoint_guid"></a>Pkey- \_ audioendpunkt- \_ GUID

Die **pkey \_ audioendpoint \_ GUID** -Eigenschaft stellt den DirectSound-Geräte Bezeichner bereit, der dem audioendpunktgerät entspricht. Der Eigenschafts Wert ist eine GUID, die der Client als Geräte Bezeichner für die **directsoundcreate** -oder **directsoundcaptuneu** -Funktion in der DirectSound-API bereitstellen kann. Durch diesen Wert wird das audioendpunktgerät für alle audioendpunktgeräte im System eindeutig identifiziert. Weitere Informationen zu DirectSound finden Sie in der DirectX SDK-Dokumentation.

Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ LPWSTR festgelegt.

Der **pwszval** -Member der **PROPVARIANT** -Struktur verweist auf eine mit NULL endenden Zeichenfolge mit breit Zeichen, die eine GUID enthält, die das audioendpunktgerät in DirectSound identifiziert.

Wie bereits erläutert, unterstützt die [mmdevice-API](mmdevice-api.md) [Geräte Rollen](device-roles.md). Obwohl DirectSound Geräte Rollen nicht direkt unterstützt, kann ein DirectSound-Client die pkey \_ audioendpoint- \_ GUID-Eigenschaft verwenden, um auf der Grundlage seiner Geräte Rolle ein DirectSound-Rendering oder-Erfassungsgerät auszuwählen.

Beispielsweise führt eine DirectSound-Anwendung die folgenden Schritte aus, um ein DirectSound-Gerät zu erstellen, das dem renderingendpunktgerät entspricht, dem der Benutzer die emultimedia-Rolle zugewiesen hat:

1.  Aufrufen der [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) -Methode zum Abrufen der [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle des renderingendpunktgeräts, das über die emultimedia-Rolle verfügt.
2.  Rufen Sie die [**immdevice:: openpropertystore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) -Methode auf, um die **IPropertyStore** -Schnittstelle des emultimedia-Geräts abzurufen. Weitere Informationen zu **IPropertyStore** finden Sie in der Windows SDK-Dokumentation.
3.  Rufen Sie die **IPropertyStore:: GetValue** -Methode auf, um den pkey \_ audioendpoint- \_ GUID-Eigenschafts Wert zu erhalten.
4.  Konvertieren Sie den Eigenschafts Wert von einer GUID im Zeichen folgen Format in eine 16-Byte-GUID-Struktur.
5.  Rufen Sie die **DirectSound Create** -Funktion mit der GUID auf, um das Gerät mit der emultimedia-Rolle zu erstellen.

> [!Note]  
> **Pkey \_ Audioendpoint \_ GUID** ist eine schreibgeschützte Eigenschaft, unabhängig vom Speicherzugriffs Modus, der von der Anwendung in [**immdevice:: openpropertystore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore)angefordert wird. Wenn eine Anwendung versucht, mithilfe von **IPropertyStore:: SetValue** einen Wert festzulegen, schlägt dieser-Befehl mit dem \_ Fehlercode "E AccessDenied" fehl.

 

Beachten Sie, dass die in Schritt 4 generierte 16-Byte-GUID mit der Geräte-GUID übereinstimmt, die das Gerät während der DirectSound-Geräte Enumeration identifiziert. Die Funktion " **directsoundenumerate** " listet renderingendpunktgeräte auf, und die Funktion " **directsoundcaptureenumerate** " listet Erfassungs Endpunkt Geräte auf. In beiden Fällen ist die Geräte-GUID der erste Parameter, der an die enumerationsrückruf-Funktion übergeben wird. Weitere Informationen zur DirectSound-Enumeration finden Sie in der DirectX SDK-Dokumentation.

Ein Codebeispiel, in dem die pkey \_ audioendpoint- \_ GUID-Eigenschaft verwendet wird, finden Sie unter [Geräte Rollen für DirectSound-Anwendungen](device-roles-for-directsound-applications.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften des audioendpunkts**](audio-endpoint-properties.md)
</dt> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> </dl>

 

 




