---
title: Verschiedene Sprachleistenkonst constants (Ctfutb.h)
description: Die verschiedenen Sprachleistenkonst constants legen bestimmte Eigenschaften von Sprachleisten fest.
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
ms.openlocfilehash: 681477018ad9afbfd42de3a1756cf68c4efe4f20405a7e3d566078927e75817b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118876488"
---
# <a name="miscellaneous-language-bar-constants"></a>Verschiedene Sprachleistenkonst constants

Die verschiedenen Sprachleistenkonst constants legen bestimmte Eigenschaften von Sprachleisten fest.



| Konstante/Wert                                                                                                                                                                                                                                               | Beschreibung                                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DTLBI_USEPROFILEICON"></span><span id="tf_dtlbi_useprofileicon"></span><dl> <dt>**TF \_ DTLBI \_ USEPROFILEICON**</dt> <dt>0x00000001</dt> </dl> | Das Systemsprachleistenelement sollte das für das Sprachprofil angegebene Symbol anzeigen. Wird in den [Methoden ITfSystemDeviceTypeLangBarItem::GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) und [ITfSystemDeviceTypeLangBarItem::SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) verwendet.<br/> |
| <span id="TF_INVALIDMENUITEM"></span><span id="tf_invalidmenuitem"></span><dl> <dt>**TF \_ INVALIDMENUITEM**</dt> <dt>(UINT)(-1)</dt> </dl>                 | Wird nicht verwendet.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_BMPF_VERTICAL"></span><span id="tf_lbi_bmpf_vertical"></span><dl> <dt>**TF \_ LBI \_ BMPF \_ VERTICAL**</dt> <dt>0x00000001</dt> </dl>         | Wird nicht verwendet.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_DESC_MAXLEN"></span><span id="tf_lbi_desc_maxlen"></span><dl> <dt>**TF \_ LBI \_ DESC \_ MAXLEN**</dt> <dt>32</dt> </dl>                       | Länge des Strukturmitglieds TF [ \_ LANGBARITEMINFO.szDescription in WCHAR-Zeichen.](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)<br/>                                                                                                                                                                                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | TSF 1.0 auf Windows 2000 Professional<br/>                                       |
| Header<br/>                   | <dl> <dt>Ctfutb.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctfutb.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ITfSystemDeviceTypeLangBarItem::GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode)
</dt> <dt>

[ITfSystemDeviceTypeLangBarItem::SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode)
</dt> <dt>

[TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> </dl>

 

 





