---
title: Sonstige Text Speicher Konstanten (textstor. h)
description: Die verschiedenen Text Speicher Konstanten legen bestimmte Eigenschaften für Text Speicher fest.
ms.assetid: 6e05ed74-fff3-4bc4-a21e-9af9492af23b
topic_type:
- apiref
api_name:
- TS_DEFAULT_SELECTION
- TS_GEA_HIDDEN
- TS_GTA_HIDDEN
- TS_ST_CORRECTION
- TS_TC_CORRECTION
- TS_VCOOKIE_NUL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead33c21bb78035dd9fda443a53de575ffa64d9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105399"
---
# <a name="miscellaneous-text-store-constants"></a>Sonstige Text Speicher Konstanten

Die verschiedenen Text Speicher Konstanten legen bestimmte Eigenschaften für Text Speicher fest.



| Konstante/Wert                                                                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <dt>**TS \_ Standard \_ Auswahl**</dt> <dt>((ULONG)-1)</dt> </dl> | Wenn der *ulindex* -Parameter von [ITfContext:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) auf diesen Wert festgelegt ist, wird die Standardauswahl abgerufen.<br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <dt>**TS \_ GEA \_ ausgeblendet**</dt> <dt>(0x1)</dt> </dl>                              | Wenn der *dwFlags* -Parameter von [itextstoreanchor:: getemembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) auf diesen Wert festgelegt ist, kann ein eingebettetes Objekt in ausgeblendetem Text gefunden werden.<br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <dt>**TS \_ GTA \_ ausgeblendet**</dt> <dt>(0x1)</dt> </dl>                              | Nicht verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <dt>**TS \_ St- \_ Korrektur**</dt> <dt>(0x1)</dt> </dl>                     | Wenn der *dwFlags* -Parameter von [ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [itextstoreanchor:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)oder [ITextStoreACPSink:: ontextchange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) auf diesen Wert festgelegt ist, ist der Text eine Transformation (Korrektur) vorhandener Inhalte, und alle speziellen Text Markup Informationen (Metadaten) werden aufbewahrt, wie z. b<br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <dt>**TS \_ TC- \_ Korrektur**</dt> <dt>(0x1)</dt> </dl>                     | Wenn der *dwFlags* -Parameter von [itextstoreanchorsink:: ontextchange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) auf diesen Wert festgelegt ist, ist der Text eine Transformation (Korrektur) vorhandener Inhalte, und alle speziellen Text Markup Informationen (Metadaten) werden beibehalten, wie z. b. WAV-Datei Daten oder ein sprach Bezeichner.<br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <dt>**TS \_ VCookie- \_ NUL**</dt> <dt>(0xFFFFFFFF)</dt> </dl>                    | Wird intern von TSF verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                         |
| Header<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ITF context:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[Itextstoreanchor:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[Itextstoreanchor:: getembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[ITextStoreACPSink:: ontextchange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[Itextstoreanchorsink:: ontextchange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[Sonstige frameworkkonstanten](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





