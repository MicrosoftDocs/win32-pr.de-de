---
description: Werte definieren einen bestimmten SAS-Typ.
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: WLX_SAS_TYPE_XXX (winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a75c7d7a71855700c4c8c233db3cfc18e06b9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369731"
---
# <a name="wlx_sas_type_xxx"></a>wlx \_ SAS- \_ Typ \_ xxx

\[Die Konstante "wlx \_ SAS \_ Type \_ xxx" ist nicht mehr für die Verwendung ab Windows Server 2008 und Windows Vista verfügbar.\]

Die Werte für den **wlx- \_ SAS- \_ Typ \_ xxx** definieren einen bestimmten SAS-Typ.

> [!Note]  
> Gina-DLLs werden in Windows Vista ignoriert.

 

Alle Werte von 0 bis 127 sind für von Microsoft definierte Typen reserviert. Werte oberhalb von 127 sind für Kunden definierte Typen verfügbar. Die folgenden Typen werden an Funktionen übergeben, die einen *dwsastype* -Parameter aufweisen.



| Konstante                                                                                                                                                                                                         | BESCHREIBUNG                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <dt>**wlx \_ SAS \_ Type \_ STRG \_ alt \_ del**</dt> </dl>            | Gibt an, dass ein Benutzer die standardmäßige STRG + ALT + ENTF-SAS eingegeben hat.<br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <dt>**wlx \_ SAS \_ Type \_ SC \_ Insert**</dt> </dl>                      | Gibt an, dass eine [*Smartcard*](../secgloss/s-gly.md) in ein kompatibles Gerät eingefügt wurde.<br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <dt>**wlx \_ SAS \_ Type \_ SC \_ Remove**</dt> </dl>                      | Gibt an, dass eine Smartcard von einem kompatiblen Gerät entfernt wurde.<br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <dt>**\_ \_ \_ scrnsvr-Aktivität für wlx-SAS-Typ \_**</dt> </dl> | Gibt an, dass die Tastatur-oder Maus Aktivität aufgetreten ist, während ein sicherer Bildschirmschoner aktiv war.<br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <dt>**\_ \_ \_ scrnsvr-Timeout für wlx-SAS-Typ \_**</dt> </dl>    | Gibt an, dass die Bildschirmschoner-Aktivierung aufgrund von Tastatur-und Maus Inaktivität aufgetreten ist.<br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <dt>**Timeout für wlx- \_ SAS- \_ Typ \_**</dt> </dl>                             | Gibt an, dass innerhalb des angegebenen Timeout Zeitraums keine Benutzereingaben empfangen wurden.<br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <dt>**Benutzer Abmeldung zum wlx- \_ SAS- \_ Typ \_ \_**</dt> </dl>                | Gibt an, dass der Benutzer vom System abgemeldet wird.<br/>                                                                                            |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                               |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winwlx. h</dt> </dl> |



 

 
