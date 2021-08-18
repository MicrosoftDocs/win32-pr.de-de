---
description: Stellt eine Auflistung von Extension-Objekten dar.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Extensions-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e484de5b4266c5a2458d15365d44a3461a7d1d0589e22391b1afd66e437e02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006838"
---
# <a name="extensions-object"></a>Extensions-Objekt

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ExtensionCollection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Das **Extensions-Objekt** stellt eine Auflistung von [**Extension-Objekten**](extension.md) dar. Jedes [**Extension-Objekt**](extension.md) stellt eine einzelne Zertifikaterweiterung dar.

## <a name="when-to-use"></a>Verwendung

Das **Extensions-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Ruft die Anzahl der Zertifikaterweiterungen in der Auflistung ab.
-   Ruft ein bestimmtes [**Extension-Objekt**](extension.md) aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **Extensions-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Extensions-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                           | Zugriffstyp          | Beschreibung                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extensions-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Anzahl**](extensions-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der [**Extension-Objekte**](extension.md) in der Auflistung ab.<br/>                                                                                                                                    |
| [**Element**](extensions-item.md)<br/>         | Schreibgeschützt<br/> | Ruft das [**Extension-Objekt ab,**](extension.md) das die indizierte Zertifikaterweiterung der Auflistung darstellt. Dies ist die Standardeigenschaft.<br/>                                                               |



 

## <a name="remarks"></a>Hinweise

Das **Extensions-Objekt** wird von der [**Certificate.Extensions-Methode**](certificate-extensions.md) zurückgegeben.

Das **Extensions-Objekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
