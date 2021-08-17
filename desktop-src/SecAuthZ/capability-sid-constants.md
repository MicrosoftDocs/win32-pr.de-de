---
description: Definieren Sie bekannte Funktionen für Anwendungen mithilfe der AllocateAndInitializeSid-Funktion.
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Capability SID Constants (Winnt.h) (Funktions-SID-Konstanten (Winnt.h))
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37a06c0bd0115c4f7d05753825477b5de4948d1ddb9576aea46933a63cbf409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783214"
---
# <a name="capability-sid-constants"></a>Funktions-SID-Konstanten

Die Funktions-SID-Konstanten definieren für Anwendungen bekannte Funktionen mithilfe der [**AllocateAndInitializeSid-Funktion.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)

<dl> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**\_SICHERHEITSFUNKTION \_ \_ INTERNETCLIENT**
</dt> <dd> <dl> <dt>

(0x00000001L)
</dt> <dt>



Ein Konto hat von einem Clientcomputer aus Zugriff auf das Internet.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**\_SICHERHEITSFUNKTION \_ \_ \_ INTERNETCLIENTSERVER**
</dt> <dd> <dl> <dt>

(0x00000002L)
</dt> <dt>



Ein Konto hat zugriff auf das Internet von den Client- und Servercomputern.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**\_SICHERHEITSFUNKTION \_ CLIENTSERVER FÜR PRIVATE \_ \_ \_ NETZWERKE**
</dt> <dd> <dl> <dt>

(0x00000003L)
</dt> <dt>



Ein Konto hat über ein privates Netzwerk Zugriff auf das Internet.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**BILDBIBLIOTHEK \_ FÜR \_ \_ SICHERHEITSFUNKTIONEN**
</dt> <dd> <dl> <dt>

(0x000000004L)
</dt> <dt>



Ein Konto hat Zugriff auf die Bildbibliothek.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**VIDEOBIBLIOTHEK \_ ZUR \_ \_ SICHERHEITSFUNKTION**
</dt> <dd> <dl> <dt>

(0x00000005L)
</dt> <dt>



Ein Konto hat Zugriff auf die Videobibliothek.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**SECURITY \_ CAPABILITY \_ MUSIC \_ LIBRARY**
</dt> <dd> <dl> <dt>

(0x00000006L)
</dt> <dt>



Ein Konto hat Zugriff auf die Musikbibliothek.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**BIBLIOTHEK \_ ZU \_ SICHERHEITSFUNKTIONENDOKUMENTEN \_**
</dt> <dd> <dl> <dt>

(0x000000007L)
</dt> <dt>



Ein Konto hat Zugriff auf die Dokumentationsbibliothek.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**\_SICHERHEITSFUNKTION \_ \_ UNTERNEHMENSAUTHENTIFIZIERUNG**
</dt> <dd> <dl> <dt>

(0x000000008L)
</dt> <dt>



Ein Konto hat Zugriff auf die Windows Anmeldeinformationen.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**\_SICHERHEITSFUNKTION: \_ \_ FREIGEGEBENE \_ BENUTZERZERTIFIKATE**
</dt> <dd> <dl> <dt>

(0x000000009L)
</dt> <dt>



Ein Konto hat Zugriff auf die freigegebenen Benutzerzertifikate.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**WECHSELMEDIEN \_ FÜR \_ \_ SICHERHEITSFUNKTIONEN**
</dt> <dd> <dl> <dt>

(0x0000000AL)
</dt> <dt>



Ein Konto hat Zugriff auf Wechselmedien.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Beim Erstellen einer Funktions-SID müssen Sie die Paketstelle SECURITY APP PACKAGE AUTHORITY in den Aufruf der \_ \_ \_ {0,0,0,0,0,15} [**AllocateAndInitializeSid-Funktion**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) einteilen. Darüber hinaus benötigen Sie die RID- und RID-Basisanzahl für die integrierten Funktionen SECURITY \_ CAPABILITY \_ BASE RID \_ (0x00000003L) und SECURITY \_ BUILTIN \_ CAPABILITY RID COUNT \_ \_ (2L).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Winnt.h</dt> </dl> |



 

