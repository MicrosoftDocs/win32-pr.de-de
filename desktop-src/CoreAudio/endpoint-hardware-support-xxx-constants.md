---
description: Die ENDPOINT \_ HARDWARE \_ SUPPORT \_ XXX-Konstanten sind Hardwareunterstützungsflags für ein Audioendpunktgerät.
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: ENDPOINT_HARDWARE_SUPPORT_XXX Konstanten (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c975a7bc00229943bb943035bf1fc84609414d83015ce4ae7d84d175b2e18a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053720"
---
# <a name="endpoint_hardware_support_xxx-constants"></a>\_ \_ ENDPUNKTHARDWAREUNTERSTÜTZUNG \_ XXX-Konstanten

Die ENDPOINT \_ HARDWARE \_ SUPPORT \_ XXX-Konstanten sind Hardwareunterstützungsflags für ein Audioendpunktgerät.



| Konstante/Wert                                                                                                                                                                                                                                                                           | BESCHREIBUNG                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <dt>**ENDPUNKT \_ HARDWAREUNTERSTÜTZUNG \_ \_ VOLUME**</dt> <dt>0X00000001</dt> </dl> | Das Audioendpunktgerät unterstützt eine Hardware-Volumesteuerung.<br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <dt>**ENDPUNKT \_ HARDWAREUNTERSTÜTZUNG \_ \_ MUTE**</dt> <dt>0X00000002</dt> </dl>       | Das Audioendpunktgerät unterstützt ein Hardwaremute-Steuerelement.<br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <dt>**ENDPUNKT \_ HARDWARE \_ SUPPORT \_ METER**</dt> <dt>0X00000004</dt> </dl>    | Das Audioendpunktgerät unterstützt eine Hardwarespitzenmessung.<br/>     |



## <a name="remarks"></a>Hinweise

Die [**Methoden IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) und [**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) verwenden die ENDPOINT \_ HARDWARE SUPPORT \_ \_ XXX-Konstanten.

Eine Hardwareunterstützungsmaske gibt an, welche Funktionen ein Audioendpunktgerät in der Hardware implementiert. Die Maske kann entweder 0 oder die bitweise OR-Kombination einer oder mehrerer ENDPOINT \_ HARDWARE \_ SUPPORT \_ XXX-Konstanten sein. Wenn ein Bit, das einer bestimmten ENDPOINT \_ HARDWARE \_ SUPPORT XXX-Konstante entspricht, in der Maske festgelegt ist, bedeutet dies, dass die durch diese Konstante dargestellte Funktion vom Gerät in der Hardware implementiert \_ wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kernaudiokonstten](core-audio-constants.md)
</dt> <dt>

[**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




