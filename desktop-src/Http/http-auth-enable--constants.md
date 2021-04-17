---
title: HTTP_AUTH_ENABLE_ Konstanten (http. h)
description: Definieren Sie Authentifizierungs Schemas, die für eine URL-Gruppe aktiviert werden können.
ms.assetid: db22645f-c9e4-427e-b3d5-91d568aec7c5
topic_type:
- apiref
api_name:
- HTTP_AUTH_ENABLE_BASIC
- HTTP_AUTH_ENABLE_DIGEST
- HTTP_AUTH_ENABLE_KERBEROS
- HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING
- HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL
- HTTP_AUTH_ENABLE_NTLM
- HTTP_AUTH_ENABLE_NEGOTIATE
- HTTP_AUTH_ENABLE_ALL
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6462a4f9d884244f460c4bf7714b45d3e17600c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478939"
---
# <a name="http_auth_enable_-constants"></a>HTTP-Authentifizierung \_ \_ Aktivieren von \_ Konstanten

Die **http-Authentifizierung \_ \_ enable** -Konstanten definieren Authentifizierungs Schemas, die für eine URL-Gruppe aktiviert werden können.

Diese Konstanten werden in der [**http- \_ Server \_ Authentifizierungs \_ Info**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) -Struktur verwendet.

<dl> <dt>

<span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**HTTP-Authentifizierung ( \_ \_ Basic) aktivieren \_**
</dt> <dd> <dl> <dt>



Das Standard Authentifizierungsschema ist aktiviert.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**HTTP-Authentifizierung \_ \_ enable \_ Digest**
</dt> <dd> <dl> <dt>



Das Digest-Authentifizierungsschema ist aktiviert.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**HTTP-Authentifizierung \_ \_ Aktivieren von \_ Kerberos**
</dt> <dd> <dl> <dt>



Das Kerberos-Authentifizierungsschema ist aktiviert.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**HTTP \_ auth \_ Ex- \_ Flag \_ enable \_ Kerberos \_ Credential \_ Caching**
</dt> <dd> <dl> <dt>



Das Zwischenspeichern der Kerberos-Anmelde Informationen ist aktiviert.

**Windows Server 2003 und früher:** Nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**HTTP \_ auth \_ Ex \_ Flag zum \_ erfassen \_ von Anmelde Informationen**
</dt> <dd> <dl> <dt>



Die HTTP-Server-API erfasst die Identität des Aufrufers und verwendet diese für die Authentifizierung nur für Aushandlungs-und Kerberos-Schemata

**Windows Server 2003 und früher:** Nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**HTTP-Authentifizierung \_ \_ Aktivieren von \_ NTLM**
</dt> <dd> <dl> <dt>



Das NTLM-Authentifizierungsschema ist aktiviert.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**HTTP-Authentifizierung " \_ \_ aushandeln aktivieren" \_**
</dt> <dd> <dl> <dt>



Das Aushandlungs Authentifizierungsschema ist aktiviert.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**HTTP-Authentifizierung \_ \_ \_ Alle aktivieren**
</dt> <dd> <dl> <dt>



Alle Authentifizierungs Schemas sind aktiviert.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[HTTP-Server-API, Version 2,0, Konstanten](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**HTTP- \_ Server \_ Authentifizierungs \_ Informationen**](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[**Httptarturlgroupproperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**Httpsetserversessionproperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**Httpqueryurlgroupproperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**Httpqueryserversessionproperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





