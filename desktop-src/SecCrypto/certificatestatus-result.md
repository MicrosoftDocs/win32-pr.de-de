---
description: Die Result-Eigenschaft ruft einen Wert ab, der angibt, ob das Zertifikat gültig ist. Dies ist die Standard Eigenschaft.
ms.assetid: b1edfbde-9d54-4e9c-ba9b-33e4c354c23f
title: CertificateStatus. Result (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Result
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df13e9a9fb0454d30ce855b3d272fa521e96e0f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352016"
---
# <a name="certificatestatusresult-property"></a>CertificateStatus. Result (Eigenschaft)

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Result** -Eigenschaft ruft einen Wert ab, der angibt, ob das Zertifikat gültig ist. Dies ist die Standard Eigenschaft.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.Result As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

**True** gibt an, dass das Zertifikat gültig ist. Die Gültigkeit des Zertifikats wird mithilfe der aktuellen Einstellung der [**checkflag**](certificatestatus-checkflag.md) -Eigenschaft und der verschiedenen Richtlinien Einstellungen überprüft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
