---
title: WINBIO_BIR_DATA_FLAGS Konstanten (Winbio \_ types.h)
description: Geben Sie die Bedingung der Daten an.
ms.assetid: F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C
topic_type:
- apiref
api_name:
- WINBIO_DATA_FLAG_PRIVACY
- WINBIO_DATA_FLAG_INTEGRITY
- WINBIO_DATA_FLAG_SIGNED
- WINBIO_DATA_FLAG_RAW
- WINBIO_DATA_FLAG_INTERMEDIATE
- WINBIO_DATA_FLAG_PROCESSED
- WINBIO_DATA_FLAG_OPTION_MASK_PRESENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87769500de02dedc7247b15e94064a43b7c6d528234c27ad700d4a336f42a092
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622630"
---
# <a name="winbio_bir_data_flags-constants"></a>WINBIO \_ BIR \_ DATA \_ FLAGS-Konstanten

Die folgenden Konstanten werden vom **DataFlags-Member** der [**WINBIO \_ BIR \_ HEADER-Struktur**](winbio-bir-header.md) verwendet.



| Konstante/Wert                                                                                                                                                                                                                                                                                   | Beschreibung                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ \_ \_ DATENSCHUTZ-0x02**</dt> <dt></dt> </dl>                                       | Die Daten sind verschlüsselt.<br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ INTEGRITÄT VON \_ DATENFLAGS \_**</dt> <dt>0x01</dt> </dl>                                 | Die Daten werden digital signiert oder durch einen Nachrichtenauthentifizierungscode (MAC) geschützt.<br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ \_ \_ SIGNIERTES DATENFLAG**</dt> <dt>0x04</dt> </dl>                                          | Wenn dieses Flag und das **WINBIO \_ DATA FLAG \_ \_ INTEGRITY-Flag** festgelegt sind, werden die Daten signiert. Wenn dieses Flag nicht festgelegt ist, aber das **WINBIO \_ DATA FLAG \_ \_ INTEGRITY-Flag** festgelegt ist, wird ein MAC für die Daten berechnet.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ \_ \_ DATA FLAG RAW**</dt> <dt>0x20</dt> </dl>                                                   | Die Daten haben das Format, mit dem sie erfasst wurden.<br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG \_ INTERMEDIATE**</dt> <dt>0x40</dt> </dl>                        | Die Daten sind nicht unformatiert, wurden aber noch nicht vollständig verarbeitet.<br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ \_ \_ VERARBEITETES DATENFLAG**</dt> <dt>0x80</dt> </dl>                                 | Die Daten wurden verarbeitet.<br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG OPTION MASK \_ \_ \_ PRESENT**</dt> <dt>0x08</dt> </dl> | Die Flagmaske. Dieser Wert ist immer ein Wert (1).<br/>                                                                                                                                                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungskonstanten](client-application-constants.md)
</dt> </dl>

 

 





