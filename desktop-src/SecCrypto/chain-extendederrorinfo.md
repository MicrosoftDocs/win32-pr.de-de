---
description: Gibt eine Zeichenfolge zurück, die zusätzliche Fehlerinformationen zum indizierten Eintrag enthält.
ms.assetid: 4f0d5289-c414-4e2b-b612-be8ce1d98b12
title: 'IChain2:: ExtendedErrorInfo-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ExtendedErrorInfo
- IChain2.ExtendedErrorInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f8a7840d0f54ea7e93ad9998d5e8772a2ae411f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371617"
---
# <a name="ichain2extendederrorinfo-method"></a>IChain2:: ExtendedErrorInfo-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **ExtendedErrorInfo** -Methode gibt eine Zeichenfolge zurück, die zusätzliche Fehlerinformationen zum indizierten Eintrag enthält.

Diese Methode wird in CAPICOM 2,0 eingeführt.

## <a name="syntax"></a>Syntax


```VB
Chain.ExtendedErrorInfo( _
  [ ByVal Index ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in, optional\]
</dt> <dd>

Ein **Long** -Wert, der den Index des Eintrags darstellt. Der Standardwert ist 1, wodurch Fehlerinformationen für das Endzertifikat in der Kette zurückgegeben werden. " **Zertifikate. count** " gibt Informationen zum Stamm Zertifikat der Kette zurück. 0 gibt erweiterte Fehlerinformationen für die gesamte Kette zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Zeichenfolge, die die erweiterten Fehlerinformationen enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ketten**](chain.md)
</dt> </dl>

 

 
