---
description: Gibt den Zertifikat Speicher an, der zum Signieren eines Dokuments verwendet wird.
ms.assetid: aabad010-6fa3-4677-bd73-b8c52d68dbc8
title: SIGNER_CERT_STORE_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT_STORE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 197bd4855a7d2afec4c0b23662365e5f9197e302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348220"
---
# <a name="signer_cert_store_info-structure"></a>Signatur Geber- \_ Zertifikat \_ Speicher Info- \_ Struktur

Die Signatur Geber-Zertifikat **\_ \_ \_ Informations** Struktur gibt den Zertifikat Speicher an, der zum Signieren eines Dokuments verwendet wird.

> [!Note]  
> Diese Struktur ist nicht in einer Header Datei definiert. Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct _SIGNER_CERT_STORE_INFO {
  DWORD          cbSize;
  PCCERT_CONTEXT pSigningCert;
  DWORD          dwCertPolicy;
  HCERTSTORE     hCertStore;
} SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**CBSIZE**
</dt> <dd>

Die Größe der-Struktur in Bytes.

</dd> <dt>

**psigningcert**
</dt> <dd>

Ein Zeiger auf eine [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) Struktur für das Signaturzertifikat.

</dd> <dt>

**dwcertpolicy**
</dt> <dd>

Gibt an, wie der Signatur Zertifikate hinzugefügt werden. Zum Ermitteln der Zertifikat Kette werden die Speicher "My", "ca", "root" und "SPC" zusätzlich zu dem vom **HCERTSTORE** -Member angegebenen Speicher geprüft. Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <dt>**Signatur \_ Geber Zertifikat \_ Richtlinien \_ Kette**</dt> <dt>2 (0x2)</dt> </dl>                           | Fügen Sie nur Zertifikate in der Zertifikat Kette hinzu.<br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <dt>**Signatur \_ Geber Zertifikat \_ Richtlinien \_ Kette \_ ohne \_**</dt> Stamm <dt>8 (0x8)</dt> </dl> | Fügen Sie nur Zertifikate in der Zertifikat Kette mit Ausnahme des Stamm Zertifikats hinzu.<br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <dt>**Signatur \_ Geber Zertifikat \_ Richtlinien \_ Speicher**</dt> <dt>1 (0x1)</dt> </dl>                           | Fügen Sie alle Zertifikate in dem Speicher hinzu, der vom **HCERTSTORE** -Member angegeben wird. Dieses Flag kann eine bitweise **or** -Kombination mit einem der anderen möglichen Werte für diesen Member sein.<br/> |



 

</dd> <dt>

**HCERTSTORE**
</dt> <dd>

Dies ist optional. Ein Handle für einen zusätzlichen Zertifikat Speicher.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signatur Geber \_ Zertifikat**](signer-cert.md)
</dt> </dl>

 

 




