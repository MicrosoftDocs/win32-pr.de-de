---
description: Ruft den Namen der Vorlage ab.
ms.assetid: f92346bc-89b6-4063-aa66-85e2fb88d67d
title: Template.Name-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 005a9cc961b1d7be0ebda0b8e76307b95d92a6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369169"
---
# <a name="templatename-property"></a>Template.Name-Eigenschaft

\[Die **Name** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und verwenden Sie dann die OID für die Zertifikat Vorlage, um die Zertifikat Erweiterungs Vorlage abzurufen.\]

Die **Name** -Eigenschaft ruft den Namen der Vorlage ab.

## <a name="syntax"></a>Syntax


```VB
Template.Name As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Name der Vorlage.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Vorlage**](template.md)
</dt> </dl>

 

 
