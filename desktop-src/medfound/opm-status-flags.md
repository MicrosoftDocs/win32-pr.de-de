---
description: Die Flags in der folgenden Tabelle geben den Status einer OPM-Sitzung (Output Protection Manager) an.
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: OPM-Statusflags (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc044d9159ad6e6a6e957c4be0228a8e2531164
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480196"
---
# <a name="opm-status-flags"></a>OPM-Statusflags

Die Flags in der folgenden Tabelle geben den Status einer OPM-Sitzung (Output Protection Manager) an.




| Konstante/Wert | BESCHREIBUNG | 
|----------------|-------------|
| <span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl><dt><strong>OPM_STATUS_NORMAL</strong></dt><dt>0x00</dt></dl> | Normaler Status.<br /> | 
| <span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl><dt><strong>OPM_STATUS_LINK_LOST</strong></dt><dt>0x01</dt></dl> | Die Integrität der Verbindung wurde gefährdet. Beispiele für Ereignisse, die dazu führen, dass der Treiber dieses Flag festgelegt:<br /><ul><li>Der Treiber kann die aktuelle Schutzebene nicht mehr erzwingen.</li><li>Der Treiber hat einen internen Integritätsfehler erkannt.</li><li>Der Connector zwischen dem Computer und dem Anzeigegerät wurde nicht angeschlossen.</li></ul> | 
| <span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt><dt>0x02</dt></dl> | Die Verbindungskonfiguration wurde geändert. Beispielsweise hat der Benutzer den Desktopanzeigemodus geändert.<br /> | 
| <span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt><dt>0x04</dt></dl> | Der Grafikadapter oder der Treiber wurde manipuliert.<br /> Dieses Flag wird im <em>COPP-Emulationsmodus</em>nicht verwendet. Stattdessen legt die Videoausgabe das flag OPM_STATUS_LINK_LOST fest, wenn Manipulationen erkannt werden.<br /> | 
| <span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt><dt>0x08</dt></dl> | An die Videoausgabe wird ein widerrufenes gerät High-Bandwidth Digital Content Protection (HDCP) angefügt.<br /> Dieses Statusflag kann von einer <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> oder <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> Abfrage zurückgegeben werden. <br /> Das gesperrte Gerät kann direkt an die Videoausgabe oder indirekt über einen HDCP-Repeater angefügt werden. Eine Videoausgabe ist erforderlich, um diese Bedingung zu erkennen, während HDCP aktiviert ist, andernfalls jedoch nicht.<br /> Dieses Flag wird im <em>COPP-Emulationsmodus</em>nicht verwendet, da in der Videoausgabe nicht widerrufene Geräte in diesem Modus erkannt werden.<br /> | 




## <a name="remarks"></a>Hinweise

Einige dieser Konstanten entsprechen den Werten der **COPP \_ StatusFlags-Enumeration,** die im Certified Output Protection Protocol (COPP) verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[OPM-Enumerationen](opm-enumerations.md)
</dt> </dl>

 

 




