---
description: Erstellt eine Zertifikatüberprüfungskette von einem Endzertifikat zum vertrauenswürdigen Stammzertifikat und gibt einen booleschen Wert zurück, der die Gesamtgültigkeit der Kette angibt.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: IChain2::Build-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.Build
- IChain2.Build
- IChain.Build
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5001fe6855a02ad487b16b56d01eb83d28c25c8ef5ba52e6249c9de1bd2fc8a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769749"
---
# <a name="ichain2build-method"></a>IChain2::Build-Methode

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Build-Methode** erstellt eine Zertifikatüberprüfungskette von einem Endzertifikat zum vertrauenswürdigen [*Stammzertifikat*](../secgloss/r-gly.md) und gibt einen booleschen Wert zurück, der die Gesamtgültigkeit der Kette angibt.

## <a name="syntax"></a>Syntax


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zertifikat* \[ In\]
</dt> <dd>

Ein [**Certificate-Objekt,**](certificate.md) das das Endzertifikat darstellt, auf dem die Überprüfungskette erstellt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein boolescher Wert, der die Gesamtgültigkeit der Kette angibt. Die allgemeine Gültigkeit basiert auf der gültigkeitsprüfungsrichtlinie.

## <a name="remarks"></a>Hinweise

Die Kette wird mithilfe der [**CertificateStatus.CheckFlag-Eigenschaft**](certificatestatus-checkflag.md) sowie anwendungs- und zertifikatrichtlinien erstellt, die von einem [**CertificateStatus-Objekt**](certificatestatus.md) angegeben werden. Die zurückgegebene Auflistung wird sortiert. Das erste Zertifikat in der Sammlung **Certificates.Item**(1) ist das Endzertifikat der Kette. Das letzte Zertifikat in der Sammlung, **Certificates.Item**(**Certificates.Count**), ist das [*Stammzertifikat*](../secgloss/r-gly.md) der Kette. **Certificates.Item**(0) stellt die gesamte Kette dar.

Jedes Mal, wenn die **Chain.Build-Methode** aufgerufen wird, wird der [*Zustand*](../secgloss/s-gly.md) des [**Chain-Objekts**](chain.md) zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**Kette**](chain.md)
</dt> </dl>

 

 
