---
description: Ruft die Hauptversionsnummer der Vorlage ab.
ms.assetid: efde3a7c-48e0-4bfe-9118-3098c7ef8771
title: Template. MajorVersion (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MajorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a193a36ed7e914d1ed45d26c21008a7e59a5b8a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358663"
---
# <a name="templatemajorversion-property"></a>Template. MajorVersion (Eigenschaft)

\[Die **MajorVersion** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und verwenden Sie dann die OID für die Zertifikat Vorlage, um die Zertifikat Erweiterungs Vorlage abzurufen.\]

Die **MajorVersion** -Eigenschaft ruft die Hauptversionsnummer der Vorlage ab.

## <a name="syntax"></a>Syntax


```VB
Template.MajorVersion As Long
```



## <a name="property-value"></a>Eigenschaftswert

Die Hauptversionsnummer der Vorlage.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Vorlage**](template.md)
</dt> </dl>

 

 
