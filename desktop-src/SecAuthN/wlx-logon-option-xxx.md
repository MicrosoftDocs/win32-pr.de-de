---
description: Werte werden vom dwOptions-Parameter von wlxloggedoutsas verwendet.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8909f562b87eb3a8147b0684d9676b9ac55d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347138"
---
# <a name="wlx_logon_option_xxx"></a>wlx- \_ Anmelde \_ Option \_ xxx

\[Die Konstante der wlx- \_ Anmelde \_ Option \_ xxx ist nicht mehr für die Verwendung ab Windows Server 2008 und Windows Vista verfügbar.\]

Die **wlx- \_ Anmelde \_ Option \_ xxx** -Werte werden vom *dwOptions* -Parameter von [**wlxloggedoutsas**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas)verwendet.

> [!Note]  
> Gina-DLLs werden in Windows Vista ignoriert.

 

Bei erfolgreicher Anmeldung kann die Gina-DLL diesen Wert verwenden, um die folgende Option anzugeben.



| Konstante                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <dt>**wlx \_ - \_ Anmeldung \_ ohne \_ Profil**</dt> </dl> | Gibt an, dass Winlogon kein Profil für den angemeldeten Benutzer laden darf. In diesem Fall lädt entweder Ihre GINA-DLL das Profil, oder der Benutzer benötigt kein Profil.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                               |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winwlx. h</dt> </dl> |



 

 




