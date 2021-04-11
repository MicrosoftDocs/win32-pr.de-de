---
title: TS_IE_ Konstanten (textstor. h)
description: Die TS- \_ IE \_ \-Konstanten beschreiben, wie Text eingefügt wird, der eingebettete Objekte enthalten kann, die von Text Diensten verwendet werden.
ms.assetid: a455d712-42d5-472e-862d-85ae3ba9149f
topic_type:
- apiref
api_name:
- TS_IE_CORRECTION
- TS_IE_COMPOSITION
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9abdb05ba065ed9bf41b5379060c0643053884e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103282"
---
# <a name="ts_ie_-constants"></a>TS- \_ IE- \_ \* Konstanten

Die TS- \_ IE- \_ \* Konstanten beschreiben, wie Text eingefügt wird, der eingebettete Objekte enthalten kann, die von Text Diensten verwendet werden.



| Konstante/Wert                                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IE_CORRECTION"></span><span id="ts_ie_correction"></span><dl> <dt>**TS \_ IE- \_ Korrektur**</dt> <dt>(0x1)</dt> </dl>    | Bei dem Text handelt es sich um eine Transformation (Korrektur) vorhandener Inhalte, und alle speziellen Text Markup Informationen (Metadaten) werden aufbewahrt, wie z. b. WAV-Datei Daten oder eine Sprach-ID.<br/> |
| <span id="TS_IE_COMPOSITION"></span><span id="ts_ie_composition"></span><dl> <dt>**TS \_ IE- \_ Komposition**</dt> <dt>(0x2)</dt> </dl> | Nicht verwendet.<br/>                                                                                                                                                                  |



## <a name="remarks"></a>Bemerkungen

Diese Konstanten werden im *dwFlags* -Parameter von [ITextStoreACP:: insertembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) und [itextstoreanchor:: insertemeingebettet](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)verwendet.

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

[ITextStoreACP:: insertemeingebettet](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> <dt>

[Itextstoreanchor:: insertembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)
</dt> </dl>

 

 





