---
title: WINBIO_BIR_QUALITY Konstanten (winbio \_ types. h)
description: Geben Sie die relative Qualität der biometrischen Daten im Bir an, wenn kein ganzzahliger Wert zwischen 0 und 100 angegeben wurde.
ms.assetid: A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C
topic_type:
- apiref
api_name:
- WINBIO_DATA_QUALITY_NOT_SET
- WINBIO_DATA_QUALITY_NOT_SUPPORTED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1eb0881672c9e3bf51214cff93cb3f68d802b04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106191"
---
# <a name="winbio_bir_quality-constants"></a>Winbio \_ Bir- \_ Qualitäts Konstanten

Die folgenden Flags werden vom **dataquality** -Member der [**winbio- \_ \_ Header**](winbio-bir-header.md) -Struktur verwendet, um die relative Qualität der biometrischen Daten im Bir anzugeben, wenn kein ganzzahliger Wert zwischen 0 und 100 angegeben wurde.



| Konstante/Wert                                                                                                                                                                                                                                                                       | BESCHREIBUNG                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**Winbio \_ Data \_ Quality \_ nicht \_ festgelegt**</dt> <dt> 1</dt> </dl>                   | Qualitätsmessungen werden vom BIR-Ersteller unterstützt, aber im Bir ist kein Wert festgelegt.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**Winbio \_ Data \_ Quality \_ nicht \_ unterstützt**</dt> <dt> 2</dt> </dl> | Qualitätsmessungen werden vom BIR-Ersteller nicht unterstützt.<br/>                             |



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

 

 





