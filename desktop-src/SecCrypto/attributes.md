---
description: Stellt eine Auflistung von Attribute-Objekten dar.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Attributes-Objekt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61936fff0421c43a07483fb8489cca755154a8cfbdd524da5837b12f90add969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773181"
---
# <a name="attributes-object"></a>Attributes-Objekt

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**CryptographicAttributeObjectCollection-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography-Namespace.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Das **Attributes-Objekt** stellt eine Auflistung von [**Attribute-Objekten**](attribute.md) dar. Jedes [**Attribute-Objekt**](attribute.md) stellt ein einzelnes Attribut einer Nachricht dar.

## <a name="when-to-use"></a>Verwendung

Das **Attributes-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Hinzufügen oder Entfernen eines bestimmten [**Attribute-Objekts**](attribute.md) aus der Auflistung.
-   Löschen Sie die Auflistung.
-   Ruft die Anzahl der Attribute in der Auflistung ab.
-   Ruft ein bestimmtes [**Attribute-Objekt**](attribute.md) aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **Attributes-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Attributes-Objekt** verfügt über diese Methoden.



| Methode                              | Beschreibung                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [**Hinzufügen**](attributes-add.md)       | Fügt der Auflistung ein [**Attribute-Objekt**](attribute.md) hinzu.<br/>       |
| [**Klar**](attributes-clear.md)   | Entfernt alle [**Attribute-Objekte**](attribute.md) aus der Auflistung.<br/> |
| [**Entfernen**](attributes-remove.md) | Entfernt ein [**Attribute-Objekt**](attribute.md) aus der Auflistung.<br/>  |



 

### <a name="properties"></a>Eigenschaften

Das **Attributes-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                           | Zugriffstyp          | Beschreibung                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](attributes-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Anzahl**](attributes-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der [**Attribute-Objekte**](attribute.md) in der Auflistung ab.<br/>                                                                                                                                    |
| [**Element**](attributes-item.md)<br/>         | Schreibgeschützt<br/> | Ruft das [**Attribute-Objekt**](attribute.md) ab, das das indizierte Attribut darstellt. Dies ist die Standardeigenschaft.<br/>                                                                                             |



 

## <a name="remarks"></a>Hinweise

Das **Attributes-Objekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Kryptografieobjekte](cryptography-objects.md)
</dt> </dl>

 

 
