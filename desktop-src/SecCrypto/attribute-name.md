---
description: Legt den CAPICOM-Namen des Attributs fest oder ruft diese ab. Dies ist die Standardeigenschaft.
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Attribute.Name-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3234d02e5e0f68817896f2d0c9d05be25b55bbe97f49fea4d34bafbab627b2c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773654"
---
# <a name="attributename-property"></a>Attribute.Name-Eigenschaft

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**CryptographicAttributeObject-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography-Namespace.**](/previous-versions/windows/)\]

Die **Name-Eigenschaft** legt den CAPICOM-Namen des Attributs fest oder ruft sie ab. Dies ist die Standardeigenschaft.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**CAPICOM \_ ATTRIBUTE-Enumeration,**](capicom-attribute.md) der den CAPICOM-Namen des Attributs angibt. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                                                                 | Bedeutung                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <dt>**SIGNIERUNGSZEIT FÜR \_ CAPICOM-AUTHENTIFIZIERTE \_ \_ \_ ATTRIBUTE**</dt> </dl>                         | Das -Attribut enthält den Zeitpunkt, zu dem die Signatur erstellt wurde.<br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <dt>**DOKUMENTNAME DES \_ AUTHENTIFIZIERTEN CAPICOM-ATTRIBUTS \_ \_ \_**</dt> </dl>                      | Das Attribut enthält den Namen des signierten Dokuments.<br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <dt>**DOKUMENTBESCHREIBUNG DES AUTHENTIFIZIERTEN \_ \_ CAPICOM-ATTRIBUTS \_ \_**</dt> </dl> | Das -Attribut enthält eine Beschreibung des signierten Dokuments.<br/>    |



 

## <a name="remarks"></a>Hinweise

Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte Zustand des Objekts zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**attribute**](attribute.md)
</dt> </dl>

 

 
