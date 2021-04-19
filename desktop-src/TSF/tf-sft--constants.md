---
title: TF_SFT_ Konstanten (ctfutb. h)
description: Die TF \_ SFT \_ \ Konstanten geben die Anzeigeeinstellungen einer gleitenden sprach Leiste an.
ms.assetid: 628e1d85-9614-4327-b89b-723f6eeb0718
topic_type:
- apiref
api_name:
- TF_SFT_SHOWNORMAL
- TF_SFT_DOCK
- TF_SFT_MINIMIZED
- TF_SFT_HIDDEN
- TF_SFT_NOTRANSPARENCY
- TF_SFT_LOWTRANSPARENCY
- TF_SFT_HIGHTRANSPARENCY
- TF_SFT_LABELS
- TF_SFT_NOLABELS
- TF_SFT_EXTRAICONSONMINIMIZED
- TF_SFT_NOEXTRAICONSONMINIMIZED
- TF_SFT_DESKBAND
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a947960bfbe67585dc02a37de2da3dc6737540
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341805"
---
# <a name="tf_sft_-constants"></a>TF- \_ SFT- \_ \* Konstanten

Die **tf- \_ SFT \_ \** _-Konstanten geben die Anzeigeeinstellungen einer gleitenden sprach Leiste an.



| Konstante/Wert                                                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_SFT_SHOWNORMAL"></span><span id="tf_sft_shownormal"></span><dl> <dt>_ * TF \_ SFT \_ shownormal * *</dt> <dt>0x00000001</dt> </dl>                                        | Zeigen Sie die sprach Leiste als unverankertes Fenster an. Diese Konstante kann nicht mit den TF \_ SFT \_ Dock, TF \_ SFT \_ minimi, TF \_ SFT \_ Hidden oder TF \_ SFT \_ Deskband Konstanten kombiniert werden.<br/>                                                                                                 |
| <span id="TF_SFT_DOCK"></span><span id="tf_sft_dock"></span><dl> <dt>**Tf \_ SFT- \_ Dock**</dt> <dt>0x00000002</dt> </dl>                                                          | Docken Sie die sprach Leiste in einem eigenen Aufgabenbereich an. Diese Konstante kann nicht mit den TF \_ SFT \_ shownormal, TF \_ SFT \_ minimi, TF SFT \_ \_ Hidden oder TF \_ SFT \_ Deskband Konstanten kombiniert werden. Nur unter Windows XP verfügbar.<br/>                                                                |
| <span id="TF_SFT_MINIMIZED"></span><span id="tf_sft_minimized"></span><dl> <dt>**Tf \_ SFT \_ minimierte**</dt> <dt>0x00000004</dt> </dl>                                           | Zeigen Sie die sprach Leiste als einzelnes Symbol in der Taskleiste an. Diese Konstante kann nicht mit der TF \_ SFT \_ shownormal, TF \_ SFT \_ Dock, TF \_ SFT \_ Hidden oder TF \_ SFT \_ Deskband Konstanten kombiniert werden. Verwenden Sie unter Windows XP \_ stattdessen TF SFT \_ deskband.<br/>                                   |
| <span id="TF_SFT_HIDDEN"></span><span id="tf_sft_hidden"></span><dl> <dt>**Tf \_ SFT \_ ausgeblendet**</dt> <dt>0x00000008</dt> </dl>                                                    | Blenden Sie die sprach Leiste aus. Diese Konstante kann nicht mit den TF \_ SFT \_ shownormal, TF \_ SFT \_ Dock, TF \_ SFT \_ minimierten oder TF \_ SFT \_ Deskband-Konstanten kombiniert werden.<br/>                                                                                                                     |
| <span id="TF_SFT_NOTRANSPARENCY"></span><span id="tf_sft_notransparency"></span><dl> <dt>**Tf \_ SFT \_ notransparenz**</dt> <dt>0x00000010</dt> </dl>                            | Machen Sie die sprach Leiste nicht transparent.<br/>                                                                                                                                                                                                                                                |
| <span id="TF_SFT_LOWTRANSPARENCY"></span><span id="tf_sft_lowtransparency"></span><dl> <dt>**Tf \_ SFT \_ lowtransparenz**</dt> <dt>0x00000020</dt> </dl>                         | Legen Sie die sprach Leiste teilweise transparent. Nur unter Windows 2000 oder höher verfügbar.<br/>                                                                                                                                                                                        |
| <span id="TF_SFT_HIGHTRANSPARENCY"></span><span id="tf_sft_hightransparency"></span><dl> <dt>**Tf \_ SFT \_ hightransparenz**</dt> <dt>0x00000040</dt> </dl>                      | Machen Sie die sprach Leiste äußerst transparent. Nur unter Windows 2000 oder höher verfügbar.<br/>                                                                                                                                                                                           |
| <span id="TF_SFT_LABELS"></span><span id="tf_sft_labels"></span><dl> <dt>**Tf \_ SFT- \_ Bezeichnungen**</dt> <dt>0x00000080</dt> </dl>                                                    | Zeigen Sie Text Bezeichnungen neben sprach leisten Symbolen an.<br/>                                                                                                                                                                                                                              |
| <span id="TF_SFT_NOLABELS"></span><span id="tf_sft_nolabels"></span><dl> <dt>**Tf \_ SFT \_ nolabels**</dt> <dt>0x00000100</dt> </dl>                                              | Text Beschriftungen für sprach leisten Symbol ausblenden.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_SFT_EXTRAICONSONMINIMIZED"></span><span id="tf_sft_extraiconsonminimized"></span><dl> <dt>**Tf \_ SFT \_ extraiconsonminimi0x00000200**</dt> <dt></dt> </dl>       | Zeigt Text Dienst Symbole auf der Taskleiste an, wenn die sprach Leiste minimiert wird.<br/>                                                                                                                                                                                                |
| <span id="TF_SFT_NOEXTRAICONSONMINIMIZED"></span><span id="tf_sft_noextraiconsonminimized"></span><dl> <dt>**Tf \_ SFT \_ noextraiconsonminimi0x00000400**</dt> <dt></dt> </dl> | Blenden Sie Text Dienst Symbole auf der Taskleiste aus, wenn die sprach Leiste minimiert ist.<br/>                                                                                                                                                                                                   |
| <span id="TF_SFT_DESKBAND"></span><span id="tf_sft_deskband"></span><dl> <dt>**Tf \_ SFT \_ Deskband**</dt> <dt>0x00000800</dt> </dl>                                              | Andocken Sie die sprach Leiste am rechten und Ende der Taskleiste des Systems (unmittelbar links neben der Taskleiste/Uhr). Diese Konstante kann nicht mit den "TF \_ SFT \_ shownormal", "TF \_ SFT \_ Dock", "TF \_ SFT \_ minimiminimiert" oder "TF \_ SFT \_ Hidden Konstanten" kombiniert werden. Nur unter Windows XP verfügbar.<br/> |



## <a name="remarks"></a>Bemerkungen

Die [itflangbarmgr:: showfloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating) -Methode legt das Ergebnis einer logischen **or** -Operation für eine oder mehrere dieser Konstanten fest, um die Attribute des sprach leisten Elements anzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                       |
| Header<br/>                   | <dl> <dt>Ctfutb. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctfutb. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ITF langbarmgr:: showfloating](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbarmgr-showfloating)
</dt> </dl>

 

 





