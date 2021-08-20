---
description: Werte definieren einen bestimmten SAS-Typ.
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: WLX_SAS_TYPE_XXX (Winwlx.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 568308d064b576f036d18aaa2d150cb1c6b7f0a2d89ee60d9410fcad123351d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785713"
---
# <a name="wlx_sas_type_xxx"></a>WLX \_ SAS \_ TYPE \_ XXX

\[Die WLX \_ SAS \_ TYPE \_ XXX-Konstante ist ab Windows Server 2008 und Windows Vista nicht mehr für die Verwendung verfügbar.\]

Die **WLX \_ SAS TYPE \_ \_ XXX-Werte** definieren einen bestimmten SAS-Typ.

> [!Note]  
> GINA-DLLs werden in Windows Vista ignoriert.

 

Alle Werte von 0 bis 127 sind für von Microsoft definierte Typen reserviert. Werte über 127 sind für kundendefinierte Typen verfügbar. Die folgenden Typen werden an Funktionen übergeben, die über einen *dwSasType-Parameter* verfügen.



| Konstante                                                                                                                                                                                                         | Beschreibung                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <dt>**WLX \_ SAS \_ TYPE \_ STRG ALT \_ \_ DEL**</dt> </dl>            | Gibt an, dass ein Benutzer die Standard-SAS STRG+ALT+ENTF eingegeben hat.<br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <dt>**WLX \_ SAS \_ TYPE \_ SC \_ INSERT**</dt> </dl>                      | Gibt an, dass eine [*Smartcard*](../secgloss/s-gly.md) in ein kompatibles Gerät eingefügt wurde.<br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <dt>**WLX \_ SAS \_ TYPE \_ SC \_ REMOVE**</dt> </dl>                      | Gibt an, dass eine Smartcard von einem kompatiblen Gerät entfernt wurde.<br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <dt>**WLX \_ SAS \_ TYPE \_ SCRNSVR \_ ACTIVITY**</dt> </dl> | Gibt an, dass eine Tastatur- oder Mausaktivität aufgetreten ist, während ein sicherer Bildschirmschoner aktiv war.<br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <dt>**WLX \_ SAS \_ TYPE \_ SCRNSVR \_ TIMEOUT**</dt> </dl>    | Gibt an, dass die Bildschirmschoneraktivierung aufgrund von Tastatur- und Mausinaktivität erfolgt ist.<br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <dt>**TIMEOUT FÜR \_ WLX-SAS-TYP \_ \_**</dt> </dl>                             | Gibt an, dass innerhalb des angegebenen Time out-Zeitraums keine Benutzereingabe empfangen wurde.<br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <dt>**WLX \_ SAS \_ TYPE \_ USER \_ LOGOFF**</dt> </dl>                | Gibt an, dass der Benutzer vom System abgemeldet wird.<br/>                                                                                            |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                               |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winwlx.h</dt> </dl> |



 

 
