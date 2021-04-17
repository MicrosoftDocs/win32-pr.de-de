---
description: Die Flags in der folgenden Tabelle geben den Status einer OPM-Sitzung (Output Protection Manager) an.
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: OPM-Statusflags (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cbf9d299d6d53a26a61d19372e56e42bd2cdf99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527872"
---
# <a name="opm-status-flags"></a>OPM-Statusflags

Die Flags in der folgenden Tabelle geben den Status einer OPM-Sitzung (Output Protection Manager) an.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl> <dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </dl></td>
<td style="text-align: left;">Normaler Status.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl> <dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </dl></td>
<td style="text-align: left;">Die Integrität der Verbindung wurde beeinträchtigt. Beispiele für Ereignisse, die bewirken, dass der Treiber dieses Flag festgelegt hat, sind:<br/>
<ul>
<li>Der Treiber kann die aktuelle Schutz Ebene nicht mehr erzwingen.</li>
<li>Der Treiber hat einen internen Integritäts Fehler festgestellt.</li>
<li>Der Connector zwischen dem Computer und dem Anzeigegerät wurde getrennt.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl> <dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </dl></td>
<td style="text-align: left;">Die Verbindungs Konfiguration wurde geändert. Der Benutzer hat z. b. den Anzeigemodus für den Desktop geändert.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl> <dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </dl></td>
<td style="text-align: left;">Der Grafikadapter oder der Treiber wurde manipuliert.<br/> Dieses Flag wird im <em>COPP-Emulations Modus</em>nicht verwendet. Stattdessen wird bei der Videoausgabe das OPM_STATUS_LINK_LOST-Flag festgelegt, wenn Manipulationen erkannt werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl> <dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </dl></td>
<td style="text-align: left;">Ein gesperrtes High-Bandwidth Digital Content Protection-Gerät (HDCP) ist an die Videoausgabe angefügt.<br/> Dieses Statusflag kann von einer <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> oder <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> Abfrage zurückgegeben werden. <br/> Das widerrufene Gerät kann direkt an die Videoausgabe oder indirekt über einen HDCP-Repeater angefügt werden. Eine Videoausgabe ist erforderlich, um diese Bedingung zu erkennen, während HDCP aktiviert ist, aber nicht anders.<br/> Dieses Flag wird im <em>COPP-Emulations Modus</em>nicht verwendet, da die Videoausgabe keine gesperrten Geräte in diesem Modus erkennt.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Einige dieser Konstanten entsprechen den Werten aus der **COPP \_** -Enumeration "Enumeration", die im Certified Output Protection Protocol (COPP) verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[OPM-Enumerationen](opm-enumerations.md)
</dt> </dl>

 

 




