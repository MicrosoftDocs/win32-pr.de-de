---
description: Ruft den Namen der dem Qualifizierer zugeordneten Organisation ab.
ms.assetid: 4ceb2c0f-903d-4fcd-8446-abf3175fe8e0
title: Qualifizierer. OrganizationName-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OrganizationName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1e1ebb2b948d5a933b59e86c8753b6b68a3a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368465"
---
# <a name="qualifierorganizationname-property"></a>Qualifizierer. OrganizationName-Eigenschaft

\[Die Eigenschaft " **OrganizationName** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]

Die **OrganizationName** -Eigenschaft ruft den Namen der Organisation ab, die dem Qualifizierer zugeordnet ist. Diese Eigenschaft ist möglicherweise leer.

## <a name="syntax"></a>Syntax


```VB
Qualifier.OrganizationName As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Name der Organisation, die dem Qualifizierer zugeordnet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Qualifizierer**](qualifier.md)
</dt> </dl>

 

 
