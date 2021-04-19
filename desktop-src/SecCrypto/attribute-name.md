---
description: Legt den CAPICOM-Namen des Attributs fest oder ruft ihn ab. Dies ist die Standard Eigenschaft.
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
ms.openlocfilehash: f71bb231941765dd073d44abd11c56152ea2d975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352849"
---
# <a name="attributename-property"></a>Attribute.Name-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**cryptographiertributeobject-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography**](/previous-versions/windows/) -Namespace.\]

Die **Name** -Eigenschaft legt den CAPICOM-Namen des Attributs fest oder ruft ihn ab. Dies ist die Standard Eigenschaft.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**CAPICOM- \_ Attribut**](capicom-attribute.md) Enumeration, der den CAPICOM-Namen des Attributs angibt. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                                                                 | Bedeutung                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <dt>**\_Signatur Zeit des authentifizierten CAPICOM- \_ Attributs \_ \_**</dt> </dl>                         | Das-Attribut enthält den Zeitpunkt, zu dem die Signatur erstellt wurde.<br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <dt>**Name des von CAPICOM \_ authentifizierten \_ Attribut \_ Dokuments \_**</dt> </dl>                      | Das-Attribut enthält den Namen des signierten Dokuments.<br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <dt>**Beschreibung des \_ authentifizierten CAPICOM- \_ Attribut \_ Dokuments \_**</dt> </dl> | Das-Attribut enthält eine Beschreibung des signierten Dokuments.<br/>    |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte Status des Objekts zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Versehen**](attribute.md)
</dt> </dl>

 

 
