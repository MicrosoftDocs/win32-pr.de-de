---
description: 'Certificates-Objekt: Stellt eine Auflistung von Zertifikatobjekten dar.'
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: Certificates-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8efb9221f39b8544eabe8f6c00d21f6cfdf20c14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098388"
---
# <a name="certificates-object"></a>Certificates-Objekt

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Das **Certificates-Objekt** stellt eine Auflistung von [**Zertifikatobjekten**](certificate.md) dar. Jedes [**Certificate-Objekt**](certificate.md) stellt ein einzelnes [*digitales Zertifikat dar.*](../secgloss/d-gly.md)

Das **Certificates-Objekt** macht die folgenden Schnittstellen verfügbar:

-   **ICertificates2:** Eingeführt in CAPICOM 2.0.
-   **ICertificates:** Eingeführt in CAPICOM 1.0.

## <a name="when-to-use"></a>Verwendung

Das **Certificates-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Hinzufügen oder Entfernen eines [**Certificate-Objekts**](certificate.md) zur oder aus der Auflistung.
-   Generieren Sie eine Teilmenge der Sammlung, indem Sie einen Satz von Zertifikaten suchen oder ein Dialogfeld zum Auswählen der Zertifikate anzeigen.
-   Löschen Sie alle [**Zertifikatobjekte**](certificate.md) aus der Auflistung.
-   Rufen Sie die Anzahl der Zertifikate in der Auflistung ab.
-   Rufen Sie ein [**bestimmtes Certificate-Objekt**](certificate.md) aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **Certificates-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Certificates-Objekt** verfügt über diese Methoden.



| Methode                                | BESCHREIBUNG                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Hinzufügen**](certificates-add.md)       | Fügt der Auflistung ein [**Certificate-Objekt**](certificate.md) hinzu.<br/> (Geerbt von **ZertifikatenICertificates2**)                                        |
| [**Löschen**](certificates-clear.md)   | Entfernt alle [**Certificate-Objekte**](certificate.md) aus der Auflistung.<br/> (Geerbt von **ZertifikatenICertificates2**)                                |
| [**Suchen**](certificates-find.md)     | Gibt ein **Certificates-Objekt** zurück, das alle Zertifikate enthält, die den angegebenen Suchkriterien entsprechen.<br/> (Geerbt von **ZertifikatenICertificates2**) |
| [**Entfernen**](certificates-remove.md) | Entfernt ein einzelnes [**Certificate-Objekt**](certificate.md) aus der Auflistung.<br/> (Geerbt von **ZertifikatenICertificates2**)                            |
| [**Speichern**](certificates-save.md)     | Speichert die Zertifikate in einer angegebenen Datei.<br/> (Geerbt von **ZertifikatenICertificates2**)                                                                |
| [**Select**](certificates-select.md) | Zeigt ein Dialogfeld zum Auswählen von Zertifikaten an und gibt eine Sammlung dieser ausgewählten Zertifikate zurück.<br/> (Geerbt von **ZertifikatenICertificates2**)  |



 

### <a name="properties"></a>Eigenschaften

Das **Certificates-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                             | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificates-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Anzahl**](certificates-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der [**Certificate-Objekte**](certificate.md) in der Auflistung ab.<br/>                                                                                                                                |
| [**Element**](certificates-item.md)<br/>         | Schreibgeschützt<br/> | Ruft ein [**Certificate-Objekt**](certificate.md) ab, das das indizierte Zertifikat der Auflistung darstellt. Dies ist die Standardeigenschaft.<br/> (Geerbt von **ZertifikatenICertificates2ICertificates**)          |



 

## <a name="remarks"></a>Bemerkungen

Das **Certificates-Objekt** kann erstellt werden und ist sicher für Skripts. Die ProgID für das **Certificates-Objekt** ist "CAPICOM. Certificates.2".

**CAPICOM 1. *x*:** Die ProgID für das **Certificates-Objekt** ist "CAPICOM. Certificates.1".

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
