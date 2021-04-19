---
description: Ruft einen booleschen Wert ab, der angibt, ob die Vorlagen Erweiterung vorhanden ist.
ms.assetid: cc7f9853-8212-470d-b372-43a4bbd517f7
title: Template. istreusent (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23dcd8cc5ee92a689300078d439998e43933af93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369377"
---
# <a name="templateispresent-property"></a>Template. istreusent (Eigenschaft)

\[Die **ispree sent** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und verwenden Sie dann die OID für die Zertifikat Vorlage, um die Zertifikat Erweiterungs Vorlage abzurufen.\]

Die **ispree sent** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob die Vorlagen Erweiterung vorhanden ist.

## <a name="syntax"></a>Syntax


```VB
Template.IsPresent As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

**True** gibt an, dass die Vorlagen Erweiterung vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Vorlage**](template.md)
</dt> </dl>

 

 
