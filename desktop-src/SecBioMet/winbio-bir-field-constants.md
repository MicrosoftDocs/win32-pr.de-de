---
title: WINBIO_BIR_FIELD Konstanten (Winbio \_ types.h)
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
ms.openlocfilehash: a354f3119fcef6da3ff204f833616eeb2ac9570cdad0712a87686904ad528958
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035090"
---
# <a name="winbio_bir_field-constants"></a>WINBIO \_ BIR \_ FIELD-Konstanten

Die folgenden Konstanten werden verwendet, um eine Bitmaske für den **ValidFields-Member** der [**WINBIO \_ BIR \_ HEADER-Struktur zu**](winbio-bir-header.md) erstellen.



| Konstante/Wert                                                                                                                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ SUBHEAD COUNT \_ 0x0001**</dt> <dt></dt> </dl>                          | Für die Konformität mit NISTIR 6529-A, dem Common Biometric Exchange Formats Framework (CBEFF) Und Format A bereitgestellt, aber nicht verwendet.<br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD PRODUCT ID \_ \_ 0x0002**</dt> <dt></dt> </dl>                                   | Das **ProductId-Member** ist gültig.<br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ ID \_ 0x0004**</dt> <dt></dt> </dl>                                      | Wird für die Konformität mit NISTIR 6529-A, CBEFF Format A bereitgestellt, aber nicht verwendet.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ INDEX**</dt> <dt>0x0008</dt> </dl>                                                   | Wird für die Konformität mit NISTIR 6529-A, CBEFF Format A bereitgestellt, aber nicht verwendet.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <dt>**WINBIO \_ DATUM \_ DER \_ ERSTELLUNG \_ DES BIR-0X0010**</dt> <dt></dt> </dl>                          | Das **CreationDate-Member** ist gültig.<br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ VALIDITY PERIOD \_ 0X0020**</dt> <dt></dt> </dl>                    | Das **ValidityPeriod-Member** ist gültig.<br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD BIOMETRIC TYPE \_ \_ 0X0040**</dt> <dt></dt> </dl>                       | Der **Type-Member** ist gültig.<br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ BIOMETRIC \_ SUBTYPE**</dt> <dt>0X0080</dt> </dl>              | Der **Member Subtype** ist gültig.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ CBEFF \_ HEADER VERSION \_ 0X0100**</dt> <dt></dt> </dl>    | Der **HeaderVersion-Member** ist gültig.<br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD HEADER VERSION \_ \_ \_ 0X0200**</dt> <dt></dt> </dl> | **DerHeaderVersion-Member** ist gültig.<br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ BIOMETRIC \_ PURPOSE**</dt> <dt>0X0400</dt> </dl>              | Das **Purpose-Member** ist gültig.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD BIOMETRIC CONDITION \_ \_ 0X0800**</dt> <dt></dt> </dl>        | Wird für die Konformität mit NISTIR 6529-A, CBEFF Format A bereitgestellt, aber nicht verwendet.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ QUALITY**</dt> <dt>0x1000</dt> </dl>                                             | Das **DataQuality-Member** ist gültig.<br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ CREATOR**</dt> <dt>0x2000</dt> </dl>                                             | Wird für die Konformität mit NISTIR 6529-A, CBEFF Format A bereitgestellt, aber nicht verwendet.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ CHALLENGE**</dt> <dt>0x4000</dt> </dl>                                       | Wird für die Konformität mit NISTIR 6529-A, CBEFF Format A bereitgestellt, aber nicht verwendet.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ PAYLOAD**</dt> <dt>0x8000</dt> </dl>                                             | Wird für die Konformität mit NISTIR 6529-A, CBEFF Format A bereitgestellt, aber nicht verwendet.<br/>                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (einschließlich Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientanwendungskonst constants](client-application-constants.md)
</dt> </dl>

 

 





