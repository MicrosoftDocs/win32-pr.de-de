---
title: Sonstige Text Store Konstanten (Textstor.h)
description: Die sonstigen Textspeicherkonst constants legen bestimmte Eigenschaften für Textspeicher fest.
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
ms.openlocfilehash: 55bfa06f7f0ebda1d572a4e637076de25c7a21ef4d273cdc2527ab6481393404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952098"
---
# <a name="miscellaneous-text-store-constants"></a>Sonstige Text Store Konstanten

Die sonstigen Textspeicherkonst constants legen bestimmte Eigenschaften für Textspeicher fest.



| Konstante/Wert                                                                                                                                                                                                                                           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <dt>**TS \_ DEFAULT \_ SELECTION**</dt> <dt>( ( ULONG )-1 )</dt> </dl> | Wenn der *ulIndex-Parameter* [von ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) auf diesen Wert festgelegt ist, wird die Standardauswahl ermittelt.<br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <dt>**TS \_ HIDDEN \_ (**</dt> <dt>0x1 )</dt> </dl>                              | Wenn *der dwFlags-Parameter* von [ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) auf diesen Wert festgelegt ist, kann sich ein eingebettetes Objekt im ausgeblendeten Text befinden.<br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <dt>**TS \_ GTA \_ HIDDEN**</dt> <dt>( 0x1 )</dt> </dl>                              | Wird nicht verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <dt>**TS \_ ST \_ CORRECTION**</dt> <dt>( 0x1 )</dt> </dl>                     | Wenn *der dwFlags-Parameter* von [ITextStoreACP::SetText,](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext) [ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)oder [ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) auf diesen Wert festgelegt ist, ist der Text eine Transformation (Korrektur) vorhandener Inhalte, und alle speziellen Textmarkupinformationen (Metadaten) werden beibehalten, z. B. WAV-Dateidaten oder ein Sprachbezeichner.<br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <dt>**TS \_ TC \_ CORRECTION**</dt> <dt>( 0x1 )</dt> </dl>                     | Wenn *der dwFlags-Parameter* von [ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) auf diesen Wert festgelegt ist, ist der Text eine Transformation (Korrektur) des vorhandenen Inhalts, und alle speziellen Textmarkupinformationen (Metadaten) werden beibehalten, z. B. WAV-Dateidaten oder ein Sprachbezeichner.<br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <dt>**TS \_ VCOOKIE \_ NUL**</dt> <dt>( 0xffffffff )</dt> </dl>                    | Wird intern von TSF verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Verteilbare Komponente<br/>          | TSF 1.0 auf Windows 2000 Professional<br/>                                         |
| Header<br/>                   | <dl> <dt>Textstor.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[Sonstige Frameworkkonst constants](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





