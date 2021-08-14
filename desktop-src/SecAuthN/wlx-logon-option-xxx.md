---
description: Werte werden vom dwOptions-Parameter von WlxLoggedOutSAS verwendet.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (Winwlx.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae482fa7af757a18fc3a38f809befbee94e4d59753cde8e35e01d172bcc065d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914759"
---
# <a name="wlx_logon_option_xxx"></a>\_WLX-ANMELDEOPTION \_ \_ XXX

\[Die WLX \_ LOGON \_ OPTION \_ XXX-Konstante ist ab Windows Server 2008 und Windows Vista nicht mehr für die Verwendung verfügbar.\]

Die **WLX \_ LOGON \_ OPTION \_ XXX-Werte** werden vom *dwOptions-Parameter* von [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas)verwendet.

> [!Note]  
> GINA-DLLs werden in Windows Vista ignoriert.

 

Nach erfolgreicher Anmeldung kann Ihre GINA-DLL diesen Wert verwenden, um die folgende Option anzugeben.



| Konstante                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <dt>**WLX \_ LOGON \_ OPT \_ NO \_ PROFILE**</dt> </dl> | Gibt an, dass Winlogon kein Profil für den angemeldeten Benutzer laden darf. In diesem Fall lädt entweder Ihre GINA-DLL das Profil, oder der Benutzer benötigt kein Profil.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                               |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winwlx.h</dt> </dl> |



 

 




