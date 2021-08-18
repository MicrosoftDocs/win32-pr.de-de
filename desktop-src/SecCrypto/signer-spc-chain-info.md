---
description: Gibt ein Software Publisher Certificate (SPC) und eine Zertifikatkette an, die zum Signieren eines Dokuments verwendet werden.
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
ms.openlocfilehash: ff646da815604082024f7a811f21e786abaece7b8e34944d9bd229c4624ed511
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898633"
---
# <a name="signer_spc_chain_info-structure"></a>SIGNER \_ SPC \_ CHAIN \_ INFO-Struktur

Die **SIGNER \_ SPC \_ CHAIN \_ INFO-Struktur** gibt ein [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) und eine Zertifikatkette an, die zum Signieren eines Dokuments verwendet werden.

> [!Note]  
> Diese Struktur ist in einer Headerdatei nicht definiert. Um diese Struktur zu verwenden, müssen Sie sie selbst definieren, wie in diesem Thema gezeigt.

 

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

**cbSize**
</dt> <dd>

Die Größe der -Struktur in Bytes.

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

Der Name der SPC-Datei, die zum Signieren eines Dokuments verwendet werden soll.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_SIGNER-ZERTIFIKAT**](signer-cert.md)
</dt> </dl>

 

 
