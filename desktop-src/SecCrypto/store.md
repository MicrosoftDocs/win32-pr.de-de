---
description: Stellt Eigenschaften und Methoden zur Auswahl, Verwaltung und Verwendung von Zertifikatspeichern und Zertifikaten in diesen Speichern zur Auswahl, Verwaltung und Verwendung von Zertifikaten zur Auswahl.
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: Store-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1de500d10d6bd5493492b62a2abb618be3cdb19d48a89beaf7ab83d55a86ac28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972297"
---
# <a name="store-object"></a>Store-Objekt

\[Das **Store** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Das **Store-Objekt** enthält Eigenschaften und Methoden, mit denen Sie [](../secgloss/c-gly.md) Zertifikatspeicher und die Zertifikate in diesen Speichern auswählen, verwalten und verwenden können. CAPICOM kann Current-User-, Local-Machine-, Memory- und Active Directory-Speicher verwenden. Darüber hinaus unterstützen Speicher Smartcard-basierte Zertifikatspeicher. Entwickler sollten beachten, dass einige Methoden bei einigen Speichern fehlschlagen können, wenn Vorgänge versucht werden, für die der Benutzer nicht über Rechte verfügt.

## <a name="members"></a>Member

Das **Store-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Store-Objekt** verfügt über diese Methoden.



| Methode                         | Beschreibung                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Hinzufügen**](store-add.md)       | Fügt dem [**geöffneten**](certificate.md) Zertifikatspeicher ein Zertifikatobjekt hinzu.<br/>                                                                                                                       |
| [**Schließen**](store-close.md)   | Schließt einen geöffneten Zertifikatspeicher.<br/> **CAPICOM 2.0.0.3 und früher:** Die [**Close-Methode**](store-close.md) wird nicht unterstützt.<br/>                                                               |
| [**Löschen**](store-delete.md) | Löscht den Zertifikatspeicher, der durch das aktuelle Store [**dargestellt**](certificate.md) wird.<br/> **CAPICOM 2.0.0.3 und früher:** Die [**Delete-Methode**](store-delete.md) wird nicht unterstützt.<br/> |
| [**Exportieren**](store-export.md) | Exportiert den Speicher eines codierten [*BLOB.*](../secgloss/b-gly.md)<br/>                                                                                                       |
| [**Importieren**](store-import.md) | Importiert einen zuvor exportierten Speicher.<br/>                                                                                                                                                                  |
| [**Laden**](store-load.md)     | Importiert [**Zertifikatobjekte**](certificate.md) aus einer Datei in den Speicher.<br/>                                                                                                                        |
| [**Öffnen**](store-open.md)     | Öffnet einen Zertifikatspeicher.<br/>                                                                                                                                                                            |
| [**Entfernen**](store-remove.md) | Entfernt ein [**Certificate-Objekt**](certificate.md) aus einem geöffneten Speicher.<br/>                                                                                                                               |



 

### <a name="properties"></a>Eigenschaften

Das **Store-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                              | Zugriffstyp          | Beschreibung                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Zertifikate**](store-certificates.md)<br/> | Schreibgeschützt<br/> | Ruft die [**Zertifikatsammlung des Speichers**](certificates.md) ab. Dies ist die Standardeigenschaft.<br/>                                                                                  |
| [**Location**](store-location.md)<br/>         | Schreibgeschützt<br/> | Ruft den Speicherort des Zertifikatspeichers ab, den dieses -Objekt darstellt.<br/> **CAPICOM 2.0.0.3 und früher:** Die [**Location-Eigenschaft**](store-location.md) wird nicht unterstützt.<br/> |
| [**Name**](store-name.md)<br/>                 | Schreibgeschützt<br/> | Ruft den Namen des Zertifikatspeichers ab, den dieses -Objekt darstellt.<br/> **CAPICOM 2.0.0.3 und früher:** Die [**Name-Eigenschaft**](store-name.md) wird nicht unterstützt.<br/>             |



 

## <a name="remarks"></a>Hinweise

Das **Store** kann erstellt werden und ist sicher für Skripts. Die ProgID für **das** Store ist CAPICOM. Store.2.

**CAPICOM 1. *x*:** Die ProgID für **das** Store ist CAPICOM. Store.1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
