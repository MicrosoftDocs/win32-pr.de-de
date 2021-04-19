---
description: Stellt eine Zertifikats Vertrauenskette dar.
ms.assetid: 45ed686f-4a7f-4df9-8366-98b825c3c657
title: Chain-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fa3432767ccfdb60a2e3bc0a50ddbbcf565e0aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373712"
---
# <a name="chain-object"></a>Chain-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Das **Chain** -Objekt stellt eine Zertifikats Vertrauenskette dar.

Dieses Objekt stellt Eigenschaften und Methoden zum Erstellen einer Zertifikats Vertrauenskette zum Überprüfen der Gültigkeit von Zertifikaten bereit. Die Kette wird mit dem Eigenschafts Wert [**CertificateStatus. checkflag**](certificatestatus-checkflag.md) und den Richtlinien Einstellungen eines [**CertificateStatus**](certificatestatus.md) -Objekts erstellt.

Das **Chain** -Objekt macht die folgenden Schnittstellen verfügbar:

-   **IChain2**: wurde in CAPICOM 2,0 eingeführt.
-   **IChain**: wurde in CAPICOM 1,0 eingeführt.

## <a name="when-to-use"></a>Verwendung

Das **Chain** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Erstellen Sie eine Zertifikat Vertrauenskette.
-   Abrufen der OIDs aller Zertifikat-und Anwendungsrichtlinien, die für die Kette gültig sind.
-   Überprüfen Sie den Status der Zertifikate in der Kette.
-   Abrufen erweiterter Fehlerinformationen.
-   Ruft die Auflistung der Zertifikate in der Kette ab.

## <a name="members"></a>Member

Das **Chain** -Objekt verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Chain** -Objekt verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Applicationpolicies**](chain-applicationpolicies.md) | Gibt eine [**OIDs**](oids.md) -Auflistung zurück, die die Anwendungs Richtlinie für die Kette darstellt.<br/> (Geerbt von **ChainIChain2**)                                                                                                                                                          |
| [**Entwickeln**](chain-build.md)                             | Erstellt eine Zertifikat Überprüfungs Kette von einem Endzertifikat zum vertrauenswürdigen Stamm [*Zertifikat*](../secgloss/r-gly.md)und gibt einen booleschen Wert zurück, der die Gesamt Gültigkeit der Kette angibt.<br/> (Geerbt von **ChainIChain2IChain**) |
| [**Certificatepolicies**](chain-certificatepolicies.md) | Gibt eine [**OIDs**](oids.md) -Auflistung zurück, die die für die Kette gültigen Zertifikat Richtlinie-OIDs darstellt.<br/> (Geerbt von **ChainIChain2**)                                                                                                                                                          |
| [**ExtendedErrorInfo**](chain-extendederrorinfo.md)     | Gibt eine Zeichenfolge zurück, die zusätzliche Fehlerinformationen zum indizierten Eintrag enthält.<br/> (Geerbt von **ChainIChain2**)                                                                                                                                                                                 |



 

### <a name="properties"></a>Eigenschaften

Das **Chain** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                              | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                 |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Zertifikate**](chain-certificates.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**Zertifikat**](certificates.md) Sammlung ab, die die Zertifikate in der Kette darstellt. Dies ist die Standard Eigenschaft.<br/> (Geerbt von **ChainIChain2IChain**) |
| [**Status**](chain-status.md)<br/>             | Schreibgeschützt<br/> | Ruft den Gültigkeits Status der Kette oder eines bestimmten Zertifikats in der Kette ab.<br/> (Geerbt von **ChainIChain2IChain**)                                                       |



 

## <a name="remarks"></a>Bemerkungen

Das **Ketten** Objekt kann erstellt werden und ist für die Skripterstellung sicher. Die ProgID für das **Ketten** Objekt ist "CAPICOM". Kette. 2 ".

**CAPICOM 1. *x*:** die ProgID für das **Ketten** Objekt ist CAPICOM. Kette. 1.

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
</dt> </dl>

 

 
