---
description: Ruft die Auflistung der Benutzer Hinweis Nummern ab.
ms.assetid: 5db38a53-e71b-4e80-9374-69b0c044fbc5
title: Qualifizierer. noticenumschlag (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ef9b2c4c70e011cc33f0aa9d9f2bbcc9f530bec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370744"
---
# <a name="qualifiernoticenumbers-property"></a>Qualifizierer. noticenumschlag (Eigenschaft)

\[Die **noticenumschlag** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]

Die **noticenumbers** -Eigenschaft ruft die Auflistung der Benutzer Hinweis Nummern ab. Diese Eigenschaft ist möglicherweise leer.

## <a name="syntax"></a>Syntax


```VB
Qualifier.NoticeNumbers As NoticeNumbers
```



## <a name="property-value"></a>Eigenschaftswert

Die Auflistung von Benutzer Hinweis Nummern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Qualifizierer**](qualifier.md)
</dt> </dl>

 

 
