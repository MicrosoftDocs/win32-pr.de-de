---
description: Stellt eine Auflistung von EKU-Objekten dar.
ms.assetid: 04b9f0bf-e1d4-4a2c-be5d-bae7c1090bdb
title: EKUs-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5258a37ac32e663b45bb2a82f8b0691cca3e1e76c303e8d4f9b7156e4f5a423e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767083"
---
# <a name="ekus-object"></a>EKUs-Objekt

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ExtensionCollection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Das **EKUs-Objekt** stellt eine Auflistung von [**EKU-Objekten**](eku.md) dar. Jedes [**EKU-Objekt**](eku.md) stellt eine einzelne EKU-Eigenschaft (Extended Key Usage) eines Zertifikats dar.

## <a name="when-to-use"></a>Verwendung

Die **EKUs-Sammlung** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Ruft die Anzahl der EKU-Eigenschaften in der Auflistung ab.
-   Rufen Sie ein bestimmtes [**EKU-Objekt**](eku.md) aus der Auflistung ab.
-   Durchlaufen sie die Auflistung.

## <a name="members"></a>Member

Das **EKUs-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **EKUs-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                     | Zugriffstyp          | Beschreibung                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ekus-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Anzahl**](ekus-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der [**EKU-Objekte**](eku.md) in der Auflistung ab.<br/>                                                                                                                                                |
| [**Element**](ekus-item.md)<br/>         | Schreibgeschützt<br/> | Ruft das [**EKU-Objekt**](eku.md) ab, das die indizierte EKU-Eigenschaft darstellt. Dies ist die Standardeigenschaft.<br/>                                                                                                      |



 

## <a name="remarks"></a>Hinweise

Diese Auflistung wird von der [**ExtendedKeyUsage.EKUs-Eigenschaft**](extendedkeyusage-ekus.md) abgerufen.

Das **EKUs-Objekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
