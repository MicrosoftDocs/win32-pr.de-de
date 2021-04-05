---
description: Die Konstanten in der folgenden Tabelle geben die Fernsehstandards und-Formate für den Output Protection Manager (OPM) an.
ms.assetid: 8f26aa92-ed40-483e-ac78-c071619f0e12
title: TV-schutzstandardflags (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28fc4db73bb68fd1aeb0749134d8d6cf998cec40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042041"
---
# <a name="tv-protection-standard-flags"></a>TV-Schutz Standardflags

Die Konstanten in der folgenden Tabelle geben die Fernsehstandards und-Formate für den Output Protection Manager (OPM) an.



| Konstante/Wert                                                                                                                                                                                                                                                                                                              | BESCHREIBUNG                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="OPM_PROTECTION_STANDARD_OTHER"></span><span id="opm_protection_standard_other"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ anderer**</dt> <dt>0x80000000</dt> </dl>                                             | Der Schutzstandard ist unbekannt.<br/>                 |
| <span id="OPM_PROTECTION_STANDARD_NONE"></span><span id="opm_protection_standard_none"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ None**</dt> <dt>0x00000000</dt> </dl>                                                | Es ist kein Schutzstandard vorhanden.<br/>                 |
| <span id="OPM_PROTECTION_STANDARD_IEC61880_525I"></span><span id="opm_protection_standard_iec61880_525i"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ IEC61880 \_ 525i**</dt> <dt>0x00000001</dt> </dl>                    | Der Schutzstandard ist IEC 61880, 525i.<br/>         |
| <span id="OPM_PROTECTION_STANDARD_IEC61880_2_525I"></span><span id="opm_protection_standard_iec61880_2_525i"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ IEC61880 \_ 2 \_ 525i**</dt> <dt>0x00000002</dt> </dl>             | Der Schutzstandard ist IEC 61880-2, 525i.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_IEC62375_625P"></span><span id="opm_protection_standard_iec62375_625p"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ IEC62375 \_ 625p**</dt> <dt>0x00000004</dt> </dl>                    | Der Schutzstandard ist IEC 62375, 625p.<br/>         |
| <span id="OPM_PROTECTION_STANDARD_EIA608B_525"></span><span id="opm_protection_standard_eia608b_525"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ EIA608B \_ 525**</dt> <dt>0x00000008</dt> </dl>                          | Der Schutzstandard ist "EIA/CEA-608-B, 525i".<br/>     |
| <span id="OPM_PROTECTION_STANDARD_EN300294_625I"></span><span id="opm_protection_standard_en300294_625i"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ EN300294 \_ 625i**</dt> <dt>0x00000010</dt> </dl>                    | Der Schutzstandard lautet ETSI EN 300 294, 625i.<br/>   |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_525P"></span><span id="opm_protection_standard_cea805a_typea_525p"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ CEA805A \_ TypeA \_ 525p**</dt> <dt>0x00000020</dt> </dl>    | Der Schutzstandard ist CEA-805-a type a, 525p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_750P"></span><span id="opm_protection_standard_cea805a_typea_750p"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ CEA805A \_ TypeA \_ 750 p**</dt> <dt>0x00000040</dt> </dl>    | Der Schutzstandard ist CEA-805-a, 750 p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_1125I"></span><span id="opm_protection_standard_cea805a_typea_1125i"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ CEA805A \_ TypeA \_ 1125i**</dt> <dt>0x00000080</dt> </dl> | Der Schutzstandard ist CEA-805-a type a, 1125i.<br/> |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_525P"></span><span id="opm_protection_standard_cea805a_typeb_525p"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ CEA805A \_ TypeB \_ 525p**</dt> <dt>0x00000100</dt> </dl>    | Der Schutzstandard ist CEA-805-A Type B, 525p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_750P"></span><span id="opm_protection_standard_cea805a_typeb_750p"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ CEA805A \_ TypeB \_ 750 p**</dt> <dt>0x00000200</dt> </dl>    | Der Schutzstandard ist CEA-805-A Typ B, 750 p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_1125I"></span><span id="opm_protection_standard_cea805a_typeb_1125i"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ CEA805A \_ TypeB \_ 1125i**</dt> <dt>0x00000400</dt> </dl> | Der Schutzstandard ist CEA-805-A Type B, 1125i.<br/> |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_525I"></span><span id="opm_protection_standard_aribtrb15_525i"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ ARIBTRB15 \_ 525i**</dt> <dt>0x00000800</dt> </dl>                 | Der Schutzstandard ist ARIB TR-B15, 525i.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_525P"></span><span id="opm_protection_standard_aribtrb15_525p"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ ARIBTRB15 \_ 525p**</dt> <dt>0x00001000</dt> </dl>                 | Der Schutzstandard ist ARIB TR-B15, 525p.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_750P"></span><span id="opm_protection_standard_aribtrb15_750p"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ ARIBTRB15 \_ 750 p**</dt> <dt>0x00002000</dt> </dl>                 | Der Schutzstandard ist ARIB TR-B15, 750 p.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_1125I"></span><span id="opm_protection_standard_aribtrb15_1125i"></span><dl> <dt>**OPM \_ Schutz \_ Standard \_ ARIBTRB15 \_ 1125i**</dt> <dt>0x00004000</dt> </dl>              | Der Schutzstandard ist ARIB TR-B15, 1125i.<br/>      |



## <a name="remarks"></a>Bemerkungen

Diese Flags sind numerisch äquivalent zur **COPP \_ tvschutzstandard** -Enumeration, die im Certified Output Protection Protocol (COPP) verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Konstanten](media-foundation-constants.md)
</dt> <dt>

[**OPM \_ Set \_ ACP \_ und \_ cgmsa \_ Signalisierung**](opm-set-acp-and-cgmsa-signaling.md)
</dt> <dt>

[OPM \_ get \_ ACP \_ und \_ cgmsa- \_ Signalisierung](opm-get-acp-and-cgmsa-signaling.md)
</dt> </dl>

 

 




