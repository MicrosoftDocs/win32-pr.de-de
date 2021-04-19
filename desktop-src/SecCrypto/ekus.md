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
ms.openlocfilehash: 56fd6eaeb5a00549cbb4ee659b99ece391e0ebed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371696"
---
# <a name="ekus-object"></a>EKUs-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ExtensionCollection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Das **EKUs** -Objekt stellt eine Auflistung von [**EKU**](eku.md) -Objekten dar. Jedes [**EKU**](eku.md) -Objekt stellt eine einzelne EKU (Extended Key Usage)-Eigenschaft eines Zertifikats dar.

## <a name="when-to-use"></a>Verwendung

Die **EKUs** -Sammlung wird verwendet, um die folgenden Aufgaben auszuführen:

-   Ruft die Anzahl der EKU-Eigenschaften in der Auflistung ab.
-   Rufen Sie ein bestimmtes [**EKU**](eku.md) -Objekt aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **EKUs** -Objekt verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **EKUs** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                     | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](ekus-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Countdown**](ekus-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der [**EKU**](eku.md) -Objekte in der Auflistung ab.<br/>                                                                                                                                                |
| [**Element**](ekus-item.md)<br/>         | Schreibgeschützt<br/> | Ruft das [**EKU**](eku.md) -Objekt ab, das die indizierte EKU-Eigenschaft darstellt. Dies ist die Standard Eigenschaft.<br/>                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Diese Auflistung wird von der [**extendedkeyusage. EKUs**](extendedkeyusage-ekus.md) -Eigenschaft abgerufen.

Das **EKUs** -Objekt kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
