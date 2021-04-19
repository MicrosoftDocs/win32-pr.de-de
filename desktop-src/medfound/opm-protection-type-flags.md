---
description: Mit den Flags in der folgenden Tabelle werden die Ausgabe Schutzmechanismen für den Output Protection Manager (OPM) angegeben.
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: OPM-Schutztyp Flags (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc8b30a18f5c7bf68fb01775751aa56e1e619f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356578"
---
# <a name="opm-protection-type-flags"></a>OPM-Schutztyp Flags

Mit den Flags in der folgenden Tabelle werden die Ausgabe Schutzmechanismen für den Output Protection Manager (OPM) angegeben.



| Konstante/Wert                                                                                                                                                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <dt>**OPM \_ \_ \_ Anderer Schutztyp**</dt> <dt>0x80000000</dt> </dl>                                                | Unbekannter Schutzmechanismus.<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <dt>**OPM \_ \_Schutztyp \_ None**</dt> <dt>0x00000000</dt> </dl>                                                   | Keine Schutzmechanismen.<br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <dt>**OPM \_ \_Schutztyp \_ COPP- \_ kompatibler \_ HDCP**</dt> <dt>0x00000001</dt> </dl> | High-Bandwidth Digital Content Protection (HDCP). Dieses Flag wird verwendet, wenn das Certified Output Protection Protocol (COPP) emuliiert wird. Weitere Informationen finden Sie in den Hinweisen. Dieses Flag wird für die OPM-Semantik nicht unterstützt.<br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <dt>**OPM \_ \_Schutztyp \_ ACP**</dt> <dt>0x00000002</dt> </dl>                                                      | Der Schutz von analogen Kopien (ACP).<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <dt>**OPM \_ \_Schutztyp \_ cgmsa**</dt> <dt>0x00000004</dt> </dl>                                                | Copy Generation Management System – Analog (CGMS-A).<br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <dt>**OPM \_ \_Schutztyp \_ HDCP**</dt> <dt>0x00000008</dt> </dl>                                                   | HDCP. Dieses Flag wird verwendet, wenn das OPM-Objekt über eine OPM-Semantik verfügt. Es wird nicht für die COPP-Semantik unterstützt.<br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <dt>**OPM \_ \_Schutztyp \_ dpcp**</dt> <dt>0x00000010</dt> </dl>                                                   | DisplayPort Content Protection (dpcp).<br/>                                                                                                                                                                           |



## <a name="remarks"></a>Bemerkungen

Diese Flags werden in den folgenden OPM-Befehlen und-Status Anforderungen verwendet.

-   [OPM \_ - \_ Schutz \_ Ebene festlegen](opm-set-protection-level.md)
-   [OPM \_ - \_ Ebene zum virtuellen \_ Schutz \_](opm-get-virtual-protection-level.md)
-   [OPM \_ get \_ Actual \_ Protection \_ Level](opm-get-actual-protection-level.md)

### <a name="hdcp"></a>HDCP

Die folgenden zwei Flags sind für HDCP definiert.



| Wert                                         | BESCHREIBUNG                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| OPM \_ - \_ Schutztyp \_ HDCP                   | Verwenden Sie dieses Flag, wenn der [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Zeiger mit OPM-Semantik erstellt wurde.                                                                        |
| OPM \_ - \_ Schutztyp mit \_ COPP- \_ kompatiblem \_ HDCP | Verwenden Sie dieses Flag, wenn der [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Zeiger mit der COPP-Semantik erstellt wurde. Dieses Flag entspricht dem "COPP \_ schutztype \_ HDCP"-Flag in COPP. |



 

Beide Modi (OPM-Semantik und COPP-Semantik) unterstützen die folgenden Vorgänge für HDCP:

-   Aktivieren oder deaktivieren Sie HDCP mithilfe des Befehls [OPM- \_ \_ Schutz \_ Ebene festlegen](opm-set-protection-level.md) .
-   Fragen Sie ab, ob HDCP mithilfe der Status Anforderung zum Aktivieren des [ \_ \_ virtuellen \_ \_ Schutzes von OPM](opm-get-virtual-protection-level.md) oder der [ \_ \_ aktuellen \_ Schutz \_ Ebene für den OPM](opm-get-actual-protection-level.md) -Status aktiviert ist.

OPM-Semantik unterstützt auch Folgendes:

-   HDCP-Repeater. Ein *HDCP-Repeater* ist ein HDCP-Gerät, das HDCP-Inhalte empfangen und denselben Inhalt erneut verschlüsseln und übertragen kann.
-   HDCP-Sperrung. Wenn ein gesperrtes HDCP-Gerät an die OPM-Videoausgabe angefügt wird, wird das Video in der Videoausgabe nicht übertragen. Die Anwendung muss keine HDCP-System erneubarkeits Nachrichten (SRMs) analysieren oder ermitteln, ob das Ausgabegerät gesperrt wurde. Weitere Informationen finden Sie unter der [**OPM \_ Set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) -Befehl.

Wenn die COPP-Semantik verwendet wird, unterstützt die [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Schnittstelle keine HDCP-Repeater. Außerdem wird die HDCP-Sperrung nicht behandelt. Die Anwendung muss stattdessen den SRM analysieren, um zu bestimmen, ob ein HDCP-Gerät gesperrt wurde.

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

 

 




