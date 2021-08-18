---
description: Die Flags in der folgenden Tabelle geben Ausgabeschutzmechanismen für Output Protection Manager (OPM) an.
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: OPM-Schutztypflags (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ee61b17ee1708f8c2fc7e2f91b33d966b17f8fd2e198e2772c30ccccf837d04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101889"
---
# <a name="opm-protection-type-flags"></a>OPM-Schutztypflags

Die Flags in der folgenden Tabelle geben Ausgabeschutzmechanismen für Output Protection Manager (OPM) an.



| Konstante/Wert                                                                                                                                                                                                                                                                                                     | Beschreibung                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <dt>**OPM \_ SCHUTZTYP \_ \_ ANDERE**</dt> <dt>0X80000000</dt> </dl>                                                | Unbekannter Schutzmechanismus.<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <dt>**OPM \_ SCHUTZTYP \_ \_ NONE**</dt> <dt>0x00000000</dt> </dl>                                                   | Keine Schutzmechanismen.<br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <dt>**OPM \_ \_ \_ COPP-KOMPATIBLE \_ \_ HDCP-0X00000001**</dt> <dt></dt> </dl> | High-Bandwidth Digital Content Protection (HDCP). Dieses Flag wird beim Emulieren von Certified Output Protection Protocol (COPP) verwendet. Weitere Informationen finden Sie in den Hinweisen. Dieses Flag wird für die OPM-Semantik nicht unterstützt.<br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <dt>**OPM \_ SCHUTZTYP \_ \_ ACP 0X00000002**</dt> <dt></dt> </dl>                                                      | Analoger Kopierschutz (ACP).<br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <dt>**OPM \_ SCHUTZTYP \_ \_ CGMSA**</dt> <dt>0x00000004</dt> </dl>                                                | Copy Generation Management System – Analog (CGMS-A).<br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <dt>**OPM \_ SCHUTZTYP \_ \_ HDCP-0x00000008**</dt> <dt></dt> </dl>                                                   | Hdcp. Dieses Flag wird verwendet, wenn das OPM-Objekt über OPM-Semantik verfügt. Dies wird für die COPP-Semantik nicht unterstützt.<br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <dt>**OPM \_ SCHUTZTYP \_ \_ DPCP-0x00000010**</dt> <dt></dt> </dl>                                                   | DisplayPort Content Protection (DPCP).<br/>                                                                                                                                                                           |



## <a name="remarks"></a>Hinweise

Diese Flags werden in den folgenden OPM-Befehlen und Statusanforderungen verwendet.

-   [OPM \_ SET \_ PROTECTION \_ LEVEL](opm-set-protection-level.md)
-   [OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL](opm-get-virtual-protection-level.md)
-   [OPM \_ GET \_ ACTUAL \_ PROTECTION \_ LEVEL](opm-get-actual-protection-level.md)

### <a name="hdcp"></a>Hdcp

Die folgenden beiden Flags sind für HDCP definiert.



| Wert                                         | Beschreibung                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_OPM-SCHUTZTYP \_ \_ HDCP                   | Verwenden Sie dieses Flag, wenn [**der IOPMVideoOutput-Zeiger**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) mit OPM-Semantik erstellt wurde.                                                                        |
| OPM \_ PROTECTION \_ TYPE \_ COPP \_ COMPATIBLE \_ HDCP | Verwenden Sie dieses Flag, wenn [**der IOPMVideoOutput-Zeiger**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) mit COPP-Semantik erstellt wurde. Dieses Flag entspricht dem COPP \_ ProtectionType \_ HDCP-Flag in COPP. |



 

Beide Modi (OPM-Semantik und COPP-Semantik) unterstützen die folgenden Vorgänge für HDCP:

-   Aktivieren oder deaktivieren Sie HDCP mit dem [Befehl OPM \_ SET PROTECTION \_ \_ LEVEL.](opm-set-protection-level.md)
-   Fragen Sie mithilfe der Statusanforderung [OPM \_ GET VIRTUAL PROTECTION \_ \_ \_ LEVEL](opm-get-virtual-protection-level.md) oder [OPM GET ACTUAL PROTECTION \_ \_ \_ \_ LEVEL](opm-get-actual-protection-level.md) ab, ob HDCP aktiviert ist.

Die OPM-Semantik unterstützt außerdem Folgendes:

-   HDCP-Repeater. Ein *HDCP-Repeater* ist ein HDCP-Gerät, das HDCP-Inhalte empfangen sowie den gleichen Inhalt erneut verschlüsseln und übertragen kann.
-   HDCP-Sperrung. Wenn ein gesperrtes HDCP-Gerät an die OPM-Videoausgabe angefügt ist, überträgt die Videoausgabe das Video nicht. Die Anwendung muss weder HDCP-Systemerneuerbarkeitsmeldungen (SRMs) analysieren noch ermitteln, ob das Ausgabegerät widerrufen wurde. Weitere Informationen finden Sie im [**Befehl OPM \_ SET \_ HDCP \_ SRM.**](opm-set-hdcp-srm.md)

Wenn COPP-Semantik verwendet wird, unterstützt die [**IOPMVideoOutput-Schnittstelle**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) keine HDCP-Repeater. Außerdem wird die HDCP-Sperrung nicht verarbeitet. Stattdessen muss die Anwendung den SRM analysieren, um zu ermitteln, ob ein HDCP-Gerät widerrufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[OPM-Enumerationen](opm-enumerations.md)
</dt> </dl>

 

 




