---
description: Stellt eine Auflistung von Signer-Objekten dar.
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: Signiererobjekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 62c5f59fc90d0d34226b4442b8fa443ad734d474e8077bf210df8bfdf752b1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898333"
---
# <a name="signers-object"></a>Signiererobjekt

\[Das **Signers-Objekt** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen eine Auflistung von CmsSigner-Objekten. Weitere Informationen finden Sie in der [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Das **Signers-Objekt** stellt eine Auflistung von [**Signer-Objekten**](signer.md) dar.

## <a name="when-to-use"></a>Verwendung

Das **Signers-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Ruft die Anzahl der Zertifikate in der Auflistung ab.
-   Rufen Sie ein bestimmtes **Signers-Objekt** aus der Auflistung ab.
-   Durchlaufen sie die Auflistung.

## <a name="members"></a>Member

Das **Signers-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Signers-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                        | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](signers-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Anzahl**](signers-count.md)<br/>       | Schreibgeschützt<br/> | Anzahl der [**Signer-Objekte**](signer.md) in der Auflistung.<br/>                                                                                                                                                        |
| [**Element**](signers-item.md)<br/>         | Schreibgeschützt<br/> | Ruft das [**Signer-Objekt**](signer.md) ab, das den indizierten Signierer darstellt. Dies ist die Standardeigenschaft.<br/>                                                                                                      |



 

## <a name="remarks"></a>Hinweise

Das **Signers-Objekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
