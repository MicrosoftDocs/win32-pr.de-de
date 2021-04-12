---
description: Die Endpunkt \_ Hardware \_ Unterstützung \_ xxx-Konstanten sind Hardwareunterstützungs-Flags für ein audioendpunktgerät.
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: ENDPOINT_HARDWARE_SUPPORT_XXX Konstanten (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffb5b2255330b205519ce3065ccb5f7eebb6b65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127665"
---
# <a name="endpoint_hardware_support_xxx-constants"></a>Endpunkt \_ Hardware \_ Unterstützung \_ xxx-Konstanten

Die Endpunkt \_ Hardware \_ Unterstützung \_ xxx-Konstanten sind Hardwareunterstützungs-Flags für ein audioendpunktgerät.



| Konstante/Wert                                                                                                                                                                                                                                                                           | BESCHREIBUNG                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <dt>**Endpunkt \_ Hardware \_ Support \_ Volume**</dt> <dt>0x00000001</dt> </dl> | Das audioendpunktgerät unterstützt ein Hardware Volume-Steuerelement.<br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <dt>**Endpunkt \_ Hardware \_ Unterstützung \_ stumm schalten**</dt> <dt>0x00000002</dt> </dl>       | Das audioendpunktgerät unterstützt ein Hardware stumm Steuerelement.<br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <dt>**Endpunkt \_ Hardware \_ Support \_ Meter**</dt> <dt>0x00000004</dt> </dl>    | Das audioendpunktgerät unterstützt einen Hardware Spitzen Zähler.<br/>     |



## <a name="remarks"></a>Bemerkungen

Die [**iaudioendpointvolume:: queryhardwaresupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport) -Methode und die [**iaudiometerinformation:: queryhardwaresupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport) -Methode verwenden die Endpoint \_ Hardware- \_ Unterstützung \_ xxx-Konstanten.

Eine Hardware Unterstützungs Maske gibt an, welche Funktionen ein audioendpunktgerät in der Hardware implementiert. Die Maske kann entweder 0 oder eine bitweise OR-Kombination von mindestens einem Endpunkt Hardware- \_ \_ Unterstützung \_ xxx-Konstanten sein. Wenn ein Bit, das einer bestimmten Endpunkt \_ Hardware \_ Unterstützung xxx-Konstante entspricht \_ , in der Maske festgelegt ist, ist die Bedeutung, dass die durch diese Konstante dargestellte Funktion vom Gerät in der Hardware implementiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kernaudiokonstanten](core-audio-constants.md)
</dt> <dt>

[**Iaudioendpointvolume:: queryhardwaresupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[**Iaudiometerinformation:: queryhardwaresupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 




