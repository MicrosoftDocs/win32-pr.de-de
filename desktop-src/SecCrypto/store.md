---
description: Stellt Eigenschaften und Methoden bereit, die Sie verwenden können, um Zertifikat Speicher und die Zertifikate in diesen speichern auszuwählen, zu verwalten und zu verwenden.
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
ms.openlocfilehash: 4e8a14fcecf0ded2e4e1a56e2b98e4ac4838b776
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355962"
---
# <a name="store-object"></a>Store-Objekt

\[Das **Store** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Das **Store** -Objekt stellt Eigenschaften und Methoden bereit, die Sie verwenden können, um [*Zertifikat Speicher*](../secgloss/c-gly.md) und die Zertifikate in diesen speichern auszuwählen, zu verwalten und zu verwenden. CAPICOM kann aktuelle Benutzer-, lokale Computer-, Speicher-und Active Directory Speicher verwenden. Speichert auch Smartcard – basierte Zertifikat Speicher. Entwickler sollten sich bewusst sein, dass einige Methoden möglicherweise mit einigen speichern fehlschlagen, wenn versucht wird, einen Vorgang auszuführen, für den der Benutzer keine Rechte hat.

## <a name="members"></a>Member

Das **Store** -Objekt verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Store** -Objekt verfügt über diese Methoden.



| Methode                         | BESCHREIBUNG                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eren**](store-add.md)       | Fügt dem geöffneten Zertifikat Speicher ein [**Zertifikat**](certificate.md) Objekt hinzu.<br/>                                                                                                                       |
| [**Schließen**](store-close.md)   | Schließt einen geöffneten Zertifikat Speicher.<br/> **CAPICOM 2.0.0.3 und früher:** Die [**Close**](store-close.md) -Methode wird nicht unterstützt.<br/>                                                               |
| [**Lösch**](store-delete.md) | Löscht den Zertifikat Speicher, der durch das aktuelle [**Speicher**](certificate.md) Objekt dargestellt wird.<br/> **CAPICOM 2.0.0.3 und früher:** Die [**Delete**](store-delete.md) -Methode wird nicht unterstützt.<br/> |
| [**Exportieren**](store-export.md) | Exportiert den Speicher eines codierten [*BLOBs*](../secgloss/b-gly.md).<br/>                                                                                                       |
| [**Importieren**](store-import.md) | Importiert einen zuvor exportierten Speicher.<br/>                                                                                                                                                                  |
| [**Laden**](store-load.md)     | Importiert [**Zertifikat**](certificate.md) Objekte aus einer Datei in den Speicher.<br/>                                                                                                                        |
| [**Eren**](store-open.md)     | Öffnet einen Zertifikat Speicher.<br/>                                                                                                                                                                            |
| [**Aufgeh**](store-remove.md) | Entfernt ein [**Zertifikat**](certificate.md) Objekt aus einem geöffneten Speicher.<br/>                                                                                                                               |



 

### <a name="properties"></a>Eigenschaften

Das **Store** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                              | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Zertifikate**](store-certificates.md)<br/> | Schreibgeschützt<br/> | Ruft die [**Zertifikats**](certificates.md) Sammlung des Stores ab. Dies ist die Standard Eigenschaft.<br/>                                                                                  |
| [**Hotels**](store-location.md)<br/>         | Schreibgeschützt<br/> | Ruft den Speicherort des Zertifikat Speicher ab, der von diesem-Objekt dargestellt wird.<br/> **CAPICOM 2.0.0.3 und früher:** Die [**Location**](store-location.md) -Eigenschaft wird nicht unterstützt.<br/> |
| [**Name**](store-name.md)<br/>                 | Schreibgeschützt<br/> | Ruft den Namen des Zertifikat Speicher ab, der von diesem-Objekt dargestellt wird.<br/> **CAPICOM 2.0.0.3 und früher:** Die [**Name**](store-name.md) -Eigenschaft wird nicht unterstützt.<br/>             |



 

## <a name="remarks"></a>Bemerkungen

Das **Store** -Objekt kann erstellt werden und ist für die Skripterstellung sicher. Die ProgID für das **Speicher** Objekt ist CAPICOM. Store. 2.

**CAPICOM 1. *x*:** die ProgID für das **Speicher** Objekt ist CAPICOM. Store. 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
