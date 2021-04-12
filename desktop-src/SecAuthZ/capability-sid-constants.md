---
description: Definieren Sie für Anwendungen bekannte Funktionen mithilfe der Funktion "Zuordnungs-initializesid".
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Funktionsid-Konstanten (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55809cbb341bcbe60578043778bc824e09b8a295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218829"
---
# <a name="capability-sid-constants"></a>Funktionsid-Konstanten

Die funktionsid-Konstanten definieren für Anwendungen bekannte Funktionen mithilfe der Funktion " [**Zuordnungs-initializesid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) ".

<dl> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**Sicherheits \_ Funktion \_ Internet \_ Client**
</dt> <dd> <dl> <dt>

(0x00000001l)
</dt> <dt>



Ein Konto hat Zugriff auf das Internet über einen Client Computer.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**Sicherheits \_ Funktion \_ Internet \_ Client \_ Server**
</dt> <dd> <dl> <dt>

(0x00000002l)
</dt> <dt>



Ein Konto hat Zugriff auf das Internet über die Client-und Server Computer.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**Sicherheits \_ Funktion \_ privater \_ Netzwerk \_ Client \_ Server**
</dt> <dd> <dl> <dt>

(0x00000003l)
</dt> <dt>



Ein Konto hat Zugriff auf das Internet über ein privates Netzwerk.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**\_ \_ Bild \_ Bibliothek für Sicherheitsfunktionen**
</dt> <dd> <dl> <dt>

(0x00000004l)
</dt> <dt>



Ein Konto hat Zugriff auf die Bilderbibliothek.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**\_ \_ Video \_ Bibliothek zu Sicherheitsfunktionen**
</dt> <dd> <dl> <dt>

(0x00000005l)
</dt> <dt>



Ein Konto hat Zugriff auf die Video Bibliothek.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**\_ \_ Musik \_ Bibliothek für Sicherheitsfunktionen**
</dt> <dd> <dl> <dt>

(0x00000006l)
</dt> <dt>



Ein Konto hat Zugriff auf die Musikbibliothek.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**Bibliothek für Sicherheits \_ Funktionen- \_ Dokumente \_**
</dt> <dd> <dl> <dt>

(0x00000007l)
</dt> <dt>



Ein Konto hat Zugriff auf die Dokumentationsbibliothek.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**Sicherheits \_ Funktion \_ Enterprise- \_ Authentifizierung**
</dt> <dd> <dl> <dt>

(0x00000008l)
</dt> <dt>



Ein Konto hat Zugriff auf die standardmäßigen Windows-Anmelde Informationen.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**Sicherheits \_ Funktionen für frei \_ gegebene \_ Benutzer \_ Zertifikate**
</dt> <dd> <dl> <dt>

(0x00000009l)
</dt> <dt>



Ein Konto hat Zugriff auf die freigegebenen Benutzerzertifikate.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**Wechselmedien für Sicherheits \_ Funktionen \_ \_**
</dt> <dd> <dl> <dt>

(0x0000000al)
</dt> <dt>



Ein Konto hat Zugriff auf den Wechsel Datenträger.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beim Erstellen einer Funktions-sid müssen Sie die Paket Zertifizierungsstelle, die Sicherheits- \_ App- \_ Paket- \_ Autorität {0,0,0,0,0,15} , in den Aufrufen der Funktion "" der Funktion " [**Zuweisung**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) " einschließen. Darüber hinaus benötigen Sie die grundlegende RID-und RID-Anzahl für die integrierten Funktionen, die Sicherheits \_ Funktion " \_ \_ RID (0x00000003l)" und "Security \_ BuiltIn \_ Capability \_ RID \_ count (2L)".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



 

