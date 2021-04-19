---
description: Stellt eine Auflistung von Zertifikat Objekten dar.
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: Zertifikate-Objekt
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
ms.openlocfilehash: 2e8c12c16820342c5687720a35ce81aa7b94f180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357303"
---
# <a name="certificates-object"></a>Zertifikate-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Das **Zertifikate** -Objekt stellt eine Sammlung von [**Zertifikat**](certificate.md) Objekten dar. Jedes [**Zertifikat**](certificate.md) Objekt stellt ein einzelnes [*digitales Zertifikat*](../secgloss/d-gly.md)dar.

Das **Zertifikate** -Objekt macht die folgenden Schnittstellen verfügbar:

-   **ICertificates2**: wurde in CAPICOM 2,0 eingeführt.
-   **Izertifikate**: eingeführt in CAPICOM 1,0.

## <a name="when-to-use"></a>Verwendung

Das **Zertifikat** Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Fügen Sie ein [**Zertifikat**](certificate.md) Objekt zu oder aus der Auflistung hinzu, oder entfernen Sie es.
-   Generieren Sie eine Teilmenge der Sammlung, indem Sie eine Gruppe von Zertifikaten suchen oder ein Dialogfeld zum Auswählen der Zertifikate anzeigen.
-   Löschen Sie alle [**Zertifikat**](certificate.md) Objekte aus der Sammlung.
-   Ruft die Anzahl der Zertifikate in der Sammlung ab.
-   Rufen Sie ein bestimmtes [**Zertifikat**](certificate.md) Objekt aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das Objekt " **Zertifikate** " verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Zertifikate** -Objekt verfügt über diese Methoden.



| Methode                                | BESCHREIBUNG                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eren**](certificates-add.md)       | Fügt der Auflistung ein [**Zertifikat**](certificate.md) Objekt hinzu.<br/> (Geerbt von **CertificatesICertificates2**)                                        |
| [**Klartext**](certificates-clear.md)   | Entfernt alle [**Zertifikat**](certificate.md) Objekte aus der Auflistung.<br/> (Geerbt von **CertificatesICertificates2**)                                |
| [**Sich**](certificates-find.md)     | Gibt ein **Zertifikate** -Objekt zurück, das alle Zertifikate enthält, die den angegebenen Suchkriterien entsprechen.<br/> (Geerbt von **CertificatesICertificates2**) |
| [**Aufgeh**](certificates-remove.md) | Entfernt ein einzelnes [**Zertifikat**](certificate.md) Objekt aus der Auflistung.<br/> (Geerbt von **CertificatesICertificates2**)                            |
| [**Speichern**](certificates-save.md)     | Speichert die Zertifikate in einer angegebenen Datei.<br/> (Geerbt von **CertificatesICertificates2**)                                                                |
| [**Select**](certificates-select.md) | Zeigt ein Dialogfeld für die Auswahl von Zertifikaten an und gibt eine Sammlung der ausgewählten Zertifikate zurück.<br/> (Geerbt von **CertificatesICertificates2**)  |



 

### <a name="properties"></a>Eigenschaften

Das Objekt " **Zertifikate** " verfügt über diese Eigenschaften.



| Eigenschaft                                             | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](certificates-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Countdown**](certificates-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der [**Zertifikat**](certificate.md) Objekte in der Auflistung ab.<br/>                                                                                                                                |
| [**Element**](certificates-item.md)<br/>         | Schreibgeschützt<br/> | Ruft ein [**Zertifikat**](certificate.md) Objekt ab, das das indizierte Zertifikat der Auflistung darstellt. Dies ist die Standard Eigenschaft.<br/> (Geerbt von **CertificatesICertificates2ICertificates**)          |



 

## <a name="remarks"></a>Bemerkungen

Das Objekt " **Zertifikate** " kann erstellt und ist für die Skripterstellung sicher. Die ProgID für das **Zertifikat** Objekt ist "CAPICOM". Zertifikate. 2 ".

**CAPICOM 1. *x*:** die ProgID für das **Zertifikat** Objekt ist "CAPICOM". Zertifikate. 1 ".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
