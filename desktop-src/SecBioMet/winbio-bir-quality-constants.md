---
title: WINBIO_BIR_QUALITY Konstanten (Winbio \_ types.h)
description: Geben Sie die relative Qualität biometrischer Daten in der BIR an, wenn kein ganzzahliger Wert zwischen 0 und 100 angegeben wurde.
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
ms.openlocfilehash: 5bbb5139b1420ea3dbfbc9e37a9dc07421788bb051acb40449e9c0117031320e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911052"
---
# <a name="winbio_bir_quality-constants"></a>WINBIO \_ BIR \_ QUALITY-Konstanten

Die folgenden Flags werden vom **DataQuality-Member** der [**WINBIO \_ BIR \_ HEADER-Struktur**](winbio-bir-header.md) verwendet, um die relative Qualität biometrischer Daten in der BIR anzugeben, wenn kein ganzzahliger Wert von 0 bis 100 angegeben wurde.



| Konstante/Wert                                                                                                                                                                                                                                                                       | BESCHREIBUNG                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ DATA \_ QUALITY \_ NOT \_ SET**</dt> <dt> 1</dt> </dl>                   | Qualitätsmessungen werden vom BIR-Ersteller unterstützt, aber in der BIR ist kein Wert festgelegt.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ DATA \_ QUALITY WIRD NICHT \_ \_ UNTERSTÜTZT**</dt> <dt> 2</dt> </dl> | Qualitätsmessungen werden vom BIR-Ersteller nicht unterstützt.<br/>                             |



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

 

 





