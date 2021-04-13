---
title: Diverse sprach Balken Konstanten (ctfutb. h)
description: Die verschiedenen sprach leisten Konstanten legen bestimmte Eigenschaften von sprach leisten fest.
ms.assetid: c1740636-7ba3-4748-9005-ee94d04dbb15
topic_type:
- apiref
api_name:
- TF_DTLBI_USEPROFILEICON
- TF_INVALIDMENUITEM
- TF_LBI_BMPF_VERTICAL
- TF_LBI_DESC_MAXLEN
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fd1a371581dea02226ba6539ca25a06ef98e75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392138"
---
# <a name="miscellaneous-language-bar-constants"></a>Diverse sprach Balken Konstanten

Die verschiedenen sprach leisten Konstanten legen bestimmte Eigenschaften von sprach leisten fest.



| Konstante/Wert                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DTLBI_USEPROFILEICON"></span><span id="tf_dtlbi_useprofileicon"></span><dl> <dt>**Tf \_ Dtlbi \_ useprofileicon**</dt> <dt>0x00000001</dt> </dl> | Das Element System Language Bar sollte das Symbol anzeigen, das für das Sprachprofil angegeben ist. Wird in den Methoden [ITF systemdevicetypelangbaritem:: getianmode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) und [ITF systemdevicetypelangbaritem::](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) -Methode verwendet.<br/> |
| <span id="TF_INVALIDMENUITEM"></span><span id="tf_invalidmenuitem"></span><dl> <dt>**Tf \_ Invalidmenuitem**</dt> <dt>(uint) (-1)</dt> </dl>                 | Nicht verwendet.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_BMPF_VERTICAL"></span><span id="tf_lbi_bmpf_vertical"></span><dl> <dt>**Tf \_ LBI \_ BMPF \_ vertikal**</dt> <dt>0x00000001</dt> </dl>         | Nicht verwendet.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_DESC_MAXLEN"></span><span id="tf_lbi_desc_maxlen"></span><dl> <dt>**Tf \_ LBI-zu-Ende- \_ \_ maxlen**</dt> <dt>32</dt> </dl>                       | Länge in WCHAR-Zeichen des Strukturmembers [tf \_ langbariteminfo. szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).<br/>                                                                                                                                                                                                 |



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

[ITF systemdevicetypelangbaritem:: getidesystemmode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode)
</dt> <dt>

[ITF systemdevicetypelangbaritem:: Settings-Modus](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode)
</dt> <dt>

[TF \_ langbariteminfo](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> </dl>

 

 





