---
title: WINBIO_BIR_FIELD Konstanten (winbio \_ types. h)
description: Geben Sie eine Bitmaske an.
ms.assetid: D8D12BCF-FEB3-4E02-B751-9F3AE5048BC1
topic_type:
- apiref
api_name:
- WINBIO_BIR_FIELD_SUBHEAD_COUNT
- WINBIO_BIR_FIELD_PRODUCT_ID
- WINBIO_BIR_FIELD_PATRON_ID
- WINBIO_BIR_FIELD_INDEX
- WINBIO_BIR_FIELD_CREATION_DATE
- WINBIO_BIR_FIELD_VALIDITY_PERIOD
- WINBIO_BIR_FIELD_BIOMETRIC_TYPE
- WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE
- WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION
- WINBIO_BIR_FIELD_PATRON_HEADER_VERSION
- WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE
- WINBIO_BIR_FIELD_BIOMETRIC_CONDITION
- WINBIO_BIR_FIELD_QUALITY
- WINBIO_BIR_FIELD_CREATOR
- WINBIO_BIR_FIELD_CHALLENGE
- WINBIO_BIR_FIELD_PAYLOAD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104710f1686f13227fbe65782c2baf9c13149650
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340728"
---
# <a name="winbio_bir_field-constants"></a>Winbio \_ Bir- \_ Feld Konstanten

Die folgenden Konstanten werden verwendet, um eine Bitmaske für den **validfields** -Member der [**winbio- \_ \_ Header**](winbio-bir-header.md) Struktur zu erstellen.



| Konstante/Wert                                                                                                                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <dt>**Winbio \_ Bir \_ - \_ feldsubkopfanzahl \_**</dt> <dt>0x0001</dt> </dl>                          | Wird für die Konformität mit nistir 6529-a bereitgestellt, das allgemeine Framework für biometrische Austauschformate (CBEFF) a, aber nicht verwendet.<br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <dt>**Winbio \_ Bir \_ - \_ feldprodukt- \_ ID**</dt> <dt>0x0002</dt> </dl>                                   | Der **ProductID-** Member ist gültig.<br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <dt>**Winbio \_ Bir- \_ Feld- \_ Patron- \_ ID**</dt> <dt>0x0004</dt> </dl>                                      | Wird für die Konformität mit nistir 6529-a bereitgestellt, das CBEFF-patronenformat A, aber nicht verwendet.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <dt>**Winbio \_ Bir \_ - \_ Feldindex**</dt> <dt>0x0008</dt> </dl>                                                   | Wird für die Konformität mit nistir 6529-a bereitgestellt, das CBEFF-patronenformat A, aber nicht verwendet.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <dt>**Winbio \_ Bir \_ - \_ felderstellungs \_ Datum**</dt> <dt>0x0010</dt> </dl>                          | Der Member " **kreationdate** " ist gültig.<br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <dt>**Winbio \_ \_ \_ Gültigkeits \_ Dauer des BIR-Felds**</dt> <dt>0x0020</dt> </dl>                    | Der **ValidityPeriod** -Member ist gültig.<br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <dt>**Winbio \_ \_ \_ Biometrischer \_ Typ des BIR-Felds**</dt> <dt>0x0040</dt> </dl>                       | Der **Typmember** ist gültig.<br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <dt>**Winbio \_ \_ \_ Biometrischer \_ Untertyp "Bir Field**</dt> " <dt>0x0080</dt> </dl>              | Der **Untertyp** Member ist gültig.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <dt>**Winbio \_ Bir \_ Field \_ CBEFF- \_ Header \_ Version**</dt> <dt>0x0100</dt> </dl>    | Der **Header Version** -Member ist gültig.<br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <dt>**Winbio \_ Bir- \_ Feld- \_ \_ patronieheader \_ Version**</dt> <dt>0x0200</dt> </dl> | Der **patronheaderversion** -Member ist gültig.<br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <dt>**Winbio \_ \_ \_ \_ Biometriezweck des biometrischen Felds**</dt> <dt>0x0400</dt> </dl>              | Der **Purpose** -Member ist gültig.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <dt>**Winbio \_ \_ \_ Biometrische \_ Bedingung "Bir Field**</dt> " <dt>0x0800</dt> </dl>        | Wird für die Konformität mit nistir 6529-a bereitgestellt, das CBEFF-patronenformat A, aber nicht verwendet.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <dt>**Winbio \_ Bir- \_ Feld \_ Qualität**</dt> <dt>0x1000</dt> </dl>                                             | Der **dataquality** -Member ist gültig.<br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <dt>**Winbio \_ Bir \_ Field \_ Creator**</dt> <dt>0x2000</dt> </dl>                                             | Wird für die Konformität mit nistir 6529-a bereitgestellt, das CBEFF-patronenformat A, aber nicht verwendet.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <dt>**Winbio \_ Bir \_ Field \_ Challenge**</dt> <dt>0x4000</dt> </dl>                                       | Wird für die Konformität mit nistir 6529-a bereitgestellt, das CBEFF-patronenformat A, aber nicht verwendet.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <dt>**Winbio \_ Bir \_ - \_ feldnutzlast**</dt> <dt>0X8000</dt> </dl>                                             | Wird für die Konformität mit nistir 6529-a bereitgestellt, das CBEFF-patronenformat A, aber nicht verwendet.<br/>                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Konstanten](client-application-constants.md)
</dt> </dl>

 

 





