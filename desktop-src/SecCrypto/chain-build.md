---
description: Erstellt eine Zertifikat Überprüfungs Kette von einem Endzertifikat zum vertrauenswürdigen Stamm Zertifikat und gibt einen booleschen Wert zurück, der die Gesamt Gültigkeit der Kette angibt.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: 'IChain2:: Build-Methode'
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
ms.openlocfilehash: 66ad51d94fdbd361a34e25b4b76289139abb87f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353784"
---
# <a name="ichain2build-method"></a>IChain2:: Build-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Build** -Methode erstellt eine Zertifikat Überprüfungs Kette von einem Endzertifikat zum vertrauenswürdigen Stamm [*Zertifikat*](../secgloss/r-gly.md) und gibt einen booleschen Wert zurück, der die Gesamt Gültigkeit der Kette angibt.

## <a name="syntax"></a>Syntax


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zertifikat* \[ in\]
</dt> <dd>

Ein [**Zertifikat**](certificate.md) Objekt, das das Endzertifikat darstellt, auf dem die Überprüfungs Kette erstellt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein boolescher Wert, der die Gesamt Gültigkeit der Kette angibt. Die Gesamt Gültigkeit basiert auf der Richtlinie für die Gültigkeitsprüfung.

## <a name="remarks"></a>Bemerkungen

Die Kette wird mit der Eigenschaft [**CertificateStatus. checkflag**](certificatestatus-checkflag.md) sowie mit den von einem [**CertificateStatus**](certificatestatus.md) -Objekt angegebenen Anwendungs-und Zertifikat Richtlinien erstellt. Die zurückgegebene Auflistung ist geordnet. das erste Zertifikat in der Sammlung, "Certificate **. Item**(1)", ist das Endzertifikat der Kette. Das letzte Zertifikat in der Sammlung, "Certificate **. Item**" ("**Zertifikate. count**"), ist das Stamm [*Zertifikat*](../secgloss/r-gly.md) der Kette. " **Zertifikate. Item**(0)" stellt die gesamte Kette dar.

Jedes Mal, wenn die **Chain. Build** -Methode aufgerufen wird, wird der [*Zustand*](../secgloss/s-gly.md) des [**Kette**](chain.md) -Objekts zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**Ketten**](chain.md)
</dt> </dl>

 

 
