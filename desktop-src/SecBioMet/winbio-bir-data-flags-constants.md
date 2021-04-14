---
title: WINBIO_BIR_DATA_FLAGS Konstanten (winbio \_ types. h)
description: Geben Sie die Bedingung für die Daten an.
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
ms.openlocfilehash: a8195cf17040c35b9e42f8977b36c5ddc6f2ea33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392214"
---
# <a name="winbio_bir_data_flags-constants"></a>Winbio \_ - \_ \_ datenflags-Konstanten

Die folgenden Konstanten werden vom **dataflags** -Member der [**winbio- \_ \_ Header**](winbio-bir-header.md) Struktur verwendet.



| Konstante/Wert                                                                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**Winbio \_ Data \_ Flag \_ Privacy**</dt> <dt>0x02</dt> </dl>                                       | Die Daten sind verschlüsselt.<br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**Winbio \_ Datenflag- \_ \_ Integrität**</dt> <dt>0x01</dt> </dl>                                 | Die Daten sind digital signiert oder durch einen Nachrichten Authentifizierungscode (Message Authentication Code, Mac) geschützt.<br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**Winbio \_ \_Datenflag \_ signiert**</dt> <dt>0x04</dt> </dl>                                          | Wenn dieses Flag und das **integritätsflag für die winbio- \_ \_ datenflag \_** festgelegt sind, werden die Daten signiert. Wenn dieses Flag nicht festgelegt ist, aber das integritätsflag für die **winbio- \_ \_ \_ datenflag** festgelegt ist, wird ein Mac für die Daten berechnet.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**Winbio \_ Data \_ Flag \_ RAW**</dt> <dt>0x20</dt> </dl>                                                   | Die Daten haben das Format, in dem Sie aufgezeichnet wurden.<br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**Winbio \_ \_Datenflag \_ zwischen**</dt> <dt>0x40</dt> </dl>                        | Die Daten sind nicht RAW, aber wurden nicht vollständig verarbeitet.<br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**Winbio \_ \_Datenflag \_ verarbeitet**</dt> <dt>0x80</dt> </dl>                                 | Die Daten wurden verarbeitet.<br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**Winbio \_ Datenflag- \_ \_ options \_ Maske \_ vorhanden**</dt> <dt>0x08</dt> </dl> | Die flagmaske. Dieser Wert ist immer eins (1).<br/>                                                                                                                                                           |



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

 

 





