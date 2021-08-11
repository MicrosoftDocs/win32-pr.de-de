---
description: Die Konstanten in der folgenden Tabelle geben Fernsehstandards und Formate für Output Protection Manager (OPM) an.
ms.assetid: 8f26aa92-ed40-483e-ac78-c071619f0e12
title: Standardflags für den TV-Schutz (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf739e9ec2fc93f427891e2e841d7dc77049eb5d878028372b2c7757f536169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237579"
---
# <a name="tv-protection-standard-flags"></a>Standardflags für den TV-Schutz

Die Konstanten in der folgenden Tabelle geben Fernsehstandards und Formate für Output Protection Manager (OPM) an.



| Konstante/Wert                                                                                                                                                                                                                                                                                                              | BESCHREIBUNG                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="OPM_PROTECTION_STANDARD_OTHER"></span><span id="opm_protection_standard_other"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ OTHER**</dt> <dt>0x80000000</dt> </dl>                                             | Der Schutzstandard ist unbekannt.<br/>                 |
| <span id="OPM_PROTECTION_STANDARD_NONE"></span><span id="opm_protection_standard_none"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ NONE**</dt> <dt>0x00000000</dt> </dl>                                                | Es gibt keinen Schutzstandard.<br/>                 |
| <span id="OPM_PROTECTION_STANDARD_IEC61880_525I"></span><span id="opm_protection_standard_iec61880_525i"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ IEC61880 \_ 525I**</dt> <dt>0x00000001</dt> </dl>                    | Der Schutzstandard ist IEC 61880, 525i.<br/>         |
| <span id="OPM_PROTECTION_STANDARD_IEC61880_2_525I"></span><span id="opm_protection_standard_iec61880_2_525i"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ IEC61880 \_ 2 \_ 525I**</dt> <dt>0x00000002</dt> </dl>             | Der Schutzstandard ist IEC 61880-2, 525i.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_IEC62375_625P"></span><span id="opm_protection_standard_iec62375_625p"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ IEC62375 \_ 625P**</dt> <dt>0x00000004</dt> </dl>                    | Der Schutzstandard ist IEC 62375, 625p.<br/>         |
| <span id="OPM_PROTECTION_STANDARD_EIA608B_525"></span><span id="opm_protection_standard_eia608b_525"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ EIA608B \_ 525**</dt> <dt>0x00000008</dt> </dl>                          | Der Schutzstandard ist EIA/CEA-608-B, 525i.<br/>     |
| <span id="OPM_PROTECTION_STANDARD_EN300294_625I"></span><span id="opm_protection_standard_en300294_625i"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ EN300294 \_ 625I**</dt> <dt>0x00000010</dt> </dl>                    | Der Schutzstandard ist ETSI EN 300 294, 625i.<br/>   |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_525P"></span><span id="opm_protection_standard_cea805a_typea_525p"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ CEA805A \_ TYPEA \_ 525P**</dt> <dt>0x00000020</dt> </dl>    | Der Schutzstandard ist CEA-805-A Typ A, 525p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_750P"></span><span id="opm_protection_standard_cea805a_typea_750p"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ CEA805A \_ TYPEA \_ 750P**</dt> <dt>0x00000040</dt> </dl>    | Der Schutzstandard ist CEA-805-A Typ A, 750p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_1125I"></span><span id="opm_protection_standard_cea805a_typea_1125i"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ CEA805A \_ TYPEA \_ 1125I**</dt> <dt>0x00000080</dt> </dl> | Der Schutzstandard ist CEA-805-A Typ A, 1125i.<br/> |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_525P"></span><span id="opm_protection_standard_cea805a_typeb_525p"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ CEA805A \_ TYPEB \_ 525P**</dt> <dt>0x00000100</dt> </dl>    | Der Schutzstandard ist CEA-805-A Typ B, 525p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_750P"></span><span id="opm_protection_standard_cea805a_typeb_750p"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ CEA805A \_ TYPEB \_ 750P**</dt> <dt>0x00000200</dt> </dl>    | Der Schutzstandard ist CEA-805-A Typ B, 750p.<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_1125I"></span><span id="opm_protection_standard_cea805a_typeb_1125i"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ CEA805A \_ TYPEB \_ 1125I**</dt> <dt>0x00000400</dt> </dl> | Der Schutzstandard ist CEA-805-A Typ B, 1125i.<br/> |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_525I"></span><span id="opm_protection_standard_aribtrb15_525i"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ ARIBTRB15 \_ 525I**</dt> <dt>0x00000800</dt> </dl>                 | Der Schutzstandard ist ARIB TR-B15, 525i.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_525P"></span><span id="opm_protection_standard_aribtrb15_525p"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ ARIBTRB15 \_ 525P**</dt> <dt>0x00001000</dt> </dl>                 | Der Schutzstandard ist ARIB TR-B15, 525p.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_750P"></span><span id="opm_protection_standard_aribtrb15_750p"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ ARIBTRB15 \_ 750P**</dt> <dt>0x00002000</dt> </dl>                 | Der Schutzstandard ist ARIB TR-B15, 750p.<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_1125I"></span><span id="opm_protection_standard_aribtrb15_1125i"></span><dl> <dt>**OPM \_ PROTECTION \_ STANDARD \_ ARIBTRB15 \_ 1125I**</dt> <dt>0x00004000</dt> </dl>              | Der Schutzstandard ist ARIB TR-B15, 1125i.<br/>      |



## <a name="remarks"></a>Hinweise

Diese Flags entsprechen numerisch der **COPP \_ TVProtectionStandard-Enumeration,** die in Certified Output Protection Protocol (COPP) verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Konstanten](media-foundation-constants.md)
</dt> <dt>

[**OPM \_ SET \_ \_ ACP- UND \_ CGMSA-SIGNALISIERUNG \_**](opm-set-acp-and-cgmsa-signaling.md)
</dt> <dt>

[OPM \_ GET ACP AND CGMSA SIGNALING (OPM GET \_ \_ ACP- UND \_ CGMSA-SIGNALISIERUNG) \_](opm-get-acp-and-cgmsa-signaling.md)
</dt> </dl>

 

 




