---
description: Stellt eine Auflistung von Erweiterungs Objekten dar.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Extensions-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3af518d6f1918c82d5819b04a086195c06b79740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368466"
---
# <a name="extensions-object"></a>Extensions-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ExtensionCollection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Das **Extensions** -Objekt stellt eine Auflistung von [**Erweiterungs**](extension.md) Objekten dar. Jedes [**Erweiterungs**](extension.md) Objekt stellt eine einzelne Zertifikat Erweiterung dar.

## <a name="when-to-use"></a>Verwendung

Das **Erweiterungs** Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Abrufen der Anzahl der Zertifikat Erweiterungen in der Sammlung.
-   Ruft ein bestimmtes [**Erweiterungs**](extension.md) Objekt aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **Erweiterungs** Objekt verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Erweiterungs** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                           | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](extensions-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Countdown**](extensions-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der [**Erweiterungs**](extension.md) Objekte in der Auflistung ab.<br/>                                                                                                                                    |
| [**Element**](extensions-item.md)<br/>         | Schreibgeschützt<br/> | Ruft das [**Erweiterungs**](extension.md) Objekt ab, das die indizierte Zertifikats Erweiterung der Auflistung darstellt. Dies ist die Standard Eigenschaft.<br/>                                                               |



 

## <a name="remarks"></a>Bemerkungen

Das **Erweiterungs** Objekt wird von der [**Certificate. Extensions**](certificate-extensions.md) -Methode zurückgegeben.

Das **Erweiterungs** Objekt kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
