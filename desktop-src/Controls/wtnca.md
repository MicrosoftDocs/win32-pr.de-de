---
title: Wtnca-Werte (uxtheme. h)
description: Gibt Flags an, die visuelle Fenster Stil Attribute ändern. Verwenden Sie eine oder eine bitweise Kombination der folgenden Werte.
ms.assetid: C71D1957-6572-4242-B715-C54BDFBBD6B7
topic_type:
- apiref
api_name:
- WTNCA_NODRAWCAPTION
- WTNCA_NODRAWICON
- WTNCA_NOSYSMENU
- WTNCA_NOMIRRORHELP
- WTNCA_VALIDBITS
api_location:
- Uxtheme.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaf543b688d0b403962da43029ac9aa85422bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105939"
---
# <a name="wtnca-values"></a>Wtnca-Werte

Gibt Flags an, die visuelle Fenster Stil Attribute ändern. Verwenden Sie eine oder eine bitweise Kombination der folgenden Werte.



| Konstante/Wert                                                                                                                                                                                                                                  | BESCHREIBUNG                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="WTNCA_NODRAWCAPTION"></span><span id="wtnca_nodrawcaption"></span><dl> <dt>**Wtnca \_ Nodrawcaption**</dt> <dt>0x00000001</dt> </dl> | Verhindert, dass die Beschriftung des Fensters gezeichnet wird.<br/>                                |
| <span id="WTNCA_NODRAWICON"></span><span id="wtnca_nodrawicon"></span><dl> <dt>**Wtnca \_ Nodrawicon**</dt> <dt>0x00000002</dt> </dl>          | Verhindert, dass das System Symbol gezeichnet wird.<br/>                                   |
| <span id="WTNCA_NOSYSMENU"></span><span id="wtnca_nosysmenu"></span><dl> <dt>**Wtnca \_ Nosysmenu**</dt> <dt>0x00000004</dt> </dl>             | Verhindert, dass das System Symbolmenü angezeigt wird.<br/>                                |
| <span id="WTNCA_NOMIRRORHELP"></span><span id="wtnca_nomirrorhelp"></span><dl> <dt>**Wtnca \_ Nomirrorhelp**</dt> <dt>0x00000008</dt> </dl>    | Verhindert die Spiegelung des Fragezeichens, auch in einem Layout von rechts nach links (RTL).<br/> |
| <span id="WTNCA_VALIDBITS"></span><span id="wtnca_validbits"></span><dl> <dt>**wtnca- \_ validbits**</dt> </dl>                                                                             | Eine Maske, die alle gültigen Bits enthält.<br/>                                     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Uxtheme. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**WTA- \_ Optionen**](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)
</dt> <dt>

[**Setwindowthemumonclientattribute**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)
</dt> </dl>

 

 





