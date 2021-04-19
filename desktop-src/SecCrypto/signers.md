---
description: Stellt eine Auflistung von Signatur Geber Objekten dar.
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: Signer-Objekt
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
ms.openlocfilehash: 75eba0ecb2592bf7efc27ecdd63288179e306651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373634"
---
# <a name="signers-object"></a>Signer-Objekt

\[Das **Signatur** Geber Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen eine Auflistung von CmsSigner-Objekten. Weitere Informationen finden Sie unter der [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Das **Signatur** Geber-Objekt stellt eine Auflistung von [**Signatur**](signer.md) Geber Objekten dar.

## <a name="when-to-use"></a>Verwendung

Das **Signatur** Geber-Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Ruft die Anzahl der Zertifikate in der Sammlung ab.
-   Ruft ein bestimmtes **Signatur** Geber Objekt aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **Signatur** Geber-Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Signatur** Geber-Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                        | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](signers-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Countdown**](signers-count.md)<br/>       | Schreibgeschützt<br/> | Anzahl der [**Signatur**](signer.md) Geber Objekte in der Auflistung.<br/>                                                                                                                                                        |
| [**Element**](signers-item.md)<br/>         | Schreibgeschützt<br/> | Ruft das [**Signatur**](signer.md) Geber Objekt ab, das den indizierten Signatur Geber darstellt. Dies ist die Standard Eigenschaft.<br/>                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Das **Signatur** Geber Objekt kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
