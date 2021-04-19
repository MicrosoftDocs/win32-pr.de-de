---
description: Ruft den URI ab, der auf eine von der Zertifizierungsstelle (Certification Authority, ca) veröffentlichte Zertifizierungs Praxis Erklärung (Certification Practice Statement, CPS) verweist.
ms.assetid: fd030c1c-137c-4036-bf13-ae989a9703cc
title: Qualifizierer. cpspointer (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.CPSPointer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db16e8faa25fc929e884358fcd885943adc17e32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366838"
---
# <a name="qualifiercpspointer-property"></a>Qualifizierer. cpspointer (Eigenschaft)

\[Die Eigenschaft " **cpspointer** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]

Die **cpspointer** -Eigenschaft ruft den URI ab, der auf eine von der Zertifizierungsstelle (Certification Authority, ca) veröffentlichte Zertifizierungs Praxis Erklärung (Certification Practice Statement, CPS) verweist.

## <a name="syntax"></a>Syntax


```VB
Qualifier.CPSPointer As String
```



## <a name="property-value"></a>Eigenschaftswert

Der URI, der auf ein von der Zertifizierungsstelle veröffentlichtes CPS zeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Qualifizierer**](qualifier.md)
</dt> </dl>

 

 
