---
title: WINBIO_ENG_CAP Konstanten (Winbio \_ types.h)
description: Geben Sie generische Engine-Funktionen an.
ms.assetid: 31C4E8AF-6EF8-43FF-A944-D7363A26BB1A
topic_type:
- apiref
api_name:
- WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT
- WINBIO_ENG_CAP_SPOOF_DETECTION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5be1099b6ad555b0547dc975c1446740f43359792c1643d155322095ad26dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867950"
---
# <a name="winbio_eng_cap-constants"></a>WINBIO \_ ENG \_ CAP-Konstanten

Die folgenden Konstanten sind **WINBIO \_ CAPABILITIES-Werte,** die verwendet werden können, um generische Funktionen der Engine-Komponente anzugeben, die mit einer bestimmten biometrischen Einheit verbunden ist. Sie geben diese Funktionen im **GenericEngineCapabilities-Member** der [**WINBIO \_ EXTENDED ENGINE \_ \_ INFO-Struktur**](winbio-extended-engine-info.md) an.



| Konstante/Wert                                                                                                                                                                                                                                                                                        | BESCHREIBUNG                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span id="WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT"></span><span id="winbio_eng_cap_iterative_improvement"></span><dl> <dt>**WINBIO \_ ENG \_ CAP \_ ITERATIVE \_ IMPROVEMENT**</dt> <dt>0X00000001</dt> </dl> | Die Biometrische Engine-Komponente kann iterative Verbesserungen durchführen.<br/> |
| <span id="WINBIO_ENG_CAP_SPOOF_DETECTION"></span><span id="winbio_eng_cap_spoof_detection"></span><dl> <dt>**WINBIO \_ ENG \_ CAP \_ SPOOF DETECTION \_ 0X00000002**</dt> <dt></dt> </dl>                   | Die Biometrische Engine-Komponente kann Spooferkennung durchführen.<br/>       |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (einschließlich Winbio.h)</dt> </dl> |



 

 





