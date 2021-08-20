---
description: Gibt den Zertifikatspeicher an, der zum Signieren eines Dokuments verwendet wird.
ms.assetid: aabad010-6fa3-4677-bd73-b8c52d68dbc8
title: SIGNER_CERT_STORE_INFO-Struktur
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
ms.openlocfilehash: 93524f631f9a9a761880eec5ebba5c97c66dcd8a67f85c6260d4598eba1a9764
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973640"
---
# <a name="signer_cert_store_info-structure"></a>SIGNER \_ CERT \_ STORE \_ INFO-Struktur

Die **SIGNER \_ CERT \_ STORE \_ INFO-Struktur** gibt den Zertifikatspeicher an, der zum Signieren eines Dokuments verwendet wird.

> [!Note]  
> Diese Struktur ist in einer Headerdatei nicht definiert. Um diese Struktur zu verwenden, müssen Sie sie selbst definieren, wie in diesem Thema gezeigt.

 

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

**cbSize**
</dt> <dd>

Die Größe der -Struktur in Bytes.

</dd> <dt>

**pSigningCert**
</dt> <dd>

Ein Zeiger auf eine [**CERT \_ CONTEXT-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) für das Signaturzertifikat.

</dd> <dt>

**dwCertPolicy**
</dt> <dd>

Gibt an, wie Zertifikate zur Signatur hinzugefügt werden. Um die Zertifikatkette zu finden, werden die My-, CA-, ROOT- und SPC-Speicher zusätzlich zu dem vom **hCertStore-Mitglied** angegebenen Speicher überprüft. Dieser Member kann mindestens einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <dt>**SIGNER \_ CERT \_ POLICY \_ CHAIN**</dt> <dt>2 (0x2)</dt> </dl>                           | Fügen Sie der Zertifikatkette nur Zertifikate hinzu.<br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <dt>**SIGNER \_ \_ \_ ZERTIFIKATRICHTLINIENKETTE \_ KEIN \_ STAMM**</dt> <dt>8 (0X8)</dt> </dl> | Fügen Sie der Zertifikatkette nur Zertifikate hinzu, mit Ausnahme des Stammzertifikats.<br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <dt>**SIGNER \_ CERT \_ POLICY \_ STORE**</dt> <dt>1 (0x1)</dt> </dl>                           | Fügen Sie alle Zertifikate in dem vom **hCertStore-Mitglied angegebenen Speicher** hinzu. Dieses Flag kann eine bitweise **OR-Kombination** mit einem der anderen möglichen Werte für diesen Member sein.<br/> |



 

</dd> <dt>

**hCertStore**
</dt> <dd>

Optional. Ein Handle für einen zusätzlichen Zertifikatspeicher.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_SIGNER-ZERTIFIKAT**](signer-cert.md)
</dt> </dl>

 

 




