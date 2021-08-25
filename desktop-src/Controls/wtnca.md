---
title: WTNCA-Werte (Uxtheme.h)
description: Gibt Flags an, die visuelle Stilattribute von Fenstern ändern. Verwenden Sie eine oder eine bitweise Kombination der folgenden Werte.
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
ms.openlocfilehash: 3b5528e26b7dc24a744affad84c8fd1fe74607ed1af56e20651fd43723cdbbff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059290"
---
# <a name="wtnca-values"></a>WTNCA-Werte

Gibt Flags an, die visuelle Stilattribute von Fenstern ändern. Verwenden Sie eine oder eine bitweise Kombination der folgenden Werte.



| Konstante/Wert                                                                                                                                                                                                                                  | BESCHREIBUNG                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="WTNCA_NODRAWCAPTION"></span><span id="wtnca_nodrawcaption"></span><dl> <dt>**WTNCA \_ NODRAWCAPTION-0x00000001**</dt> <dt></dt> </dl> | Verhindert, dass die Fensterbeschriftung gezeichnet wird.<br/>                                |
| <span id="WTNCA_NODRAWICON"></span><span id="wtnca_nodrawicon"></span><dl> <dt>**WTNCA \_ NODRAWICON**</dt> <dt>0x00000002</dt> </dl>          | Verhindert, dass das Systemsymbol gezeichnet wird.<br/>                                   |
| <span id="WTNCA_NOSYSMENU"></span><span id="wtnca_nosysmenu"></span><dl> <dt>**WTNCA \_ NOSYSMENU**</dt> <dt>0x00000004</dt> </dl>             | Verhindert, dass das Systemsymbolmenü angezeigt wird.<br/>                                |
| <span id="WTNCA_NOMIRRORHELP"></span><span id="wtnca_nomirrorhelp"></span><dl> <dt>**WTNCA \_ NOMIRRORHELP**</dt> <dt>0x00000008</dt> </dl>    | Verhindert die Spiegelung des Fragezeichens, selbst im Layout von rechts nach links (RTL).<br/> |
| <span id="WTNCA_VALIDBITS"></span><span id="wtnca_validbits"></span><dl> <dt>**WTNCA \_ VALIDBITS**</dt> </dl>                                                                             | Eine Maske, die alle gültigen Bits enthält.<br/>                                     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Uxtheme.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**\_WTA-OPTIONEN**](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)
</dt> <dt>

[**SetWindowThemeNonClientAttributes**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)
</dt> </dl>

 

 





