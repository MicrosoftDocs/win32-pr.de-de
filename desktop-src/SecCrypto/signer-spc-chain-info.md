---
description: Gibt ein Software Herausgeber Zertifikat (SPC) und eine Zertifikat Kette zum Signieren eines Dokuments an.
ms.assetid: b65b4129-df92-410c-b372-b0c004f8bb03
title: SIGNER_SPC_CHAIN_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SPC_CHAIN_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60279a60e6cdfbf43a1e2d9c45735b885d97a055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131649"
---
# <a name="signer_spc_chain_info-structure"></a>Info Struktur der Signatur Geber- \_ SPC- \_ Kette \_

Die Informationen Struktur der Signatur Geber- **\_ SPC- \_ Kette \_** gibt ein [*Software Herausgeber Zertifikat*](../secgloss/s-gly.md) (SPC) und eine Zertifikat Kette zum Signieren eines Dokuments an.

> [!Note]  
> Diese Struktur ist nicht in einer Header Datei definiert. Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct _SIGNER_SPC_CHAIN_INFO {
  DWORD      cbSize;
  LPCWSTR    pwszSpcFile;
  DWORD      dwCertPolicy;
  HCERTSTORE hCertStore;
} SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**CBSIZE**
</dt> <dd>

Die Größe der-Struktur in Bytes.

</dd> <dt>

**pwszspcfile**
</dt> <dd>

Der Name der SPC-Datei, die zum Signieren eines Dokuments verwendet werden soll.

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

 

 
