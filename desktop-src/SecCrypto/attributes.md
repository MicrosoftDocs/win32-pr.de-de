---
description: Stellt eine Auflistung von Attribut Objekten dar.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Attribute-Objekt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2493d4e1bbcbeb2dc7e7b335513beb84c3f28d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364888"
---
# <a name="attributes-object"></a>Attribute-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**cryptographitortributeobjectcollection-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Das **Attribute** -Objekt stellt eine Auflistung von [**Attribut**](attribute.md) Objekten dar. Jedes [**Attribut**](attribute.md) Objekt stellt ein einzelnes Attribut einer Nachricht dar.

## <a name="when-to-use"></a>Verwendung

Das **Attribute** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Fügen Sie ein bestimmtes [**Attribut**](attribute.md) Objekt aus der Auflistung hinzu, oder entfernen Sie es.
-   Löschen Sie die Auflistung.
-   Abrufen der Anzahl von Attributen in der Auflistung.
-   Rufen Sie ein bestimmtes [**Attribut**](attribute.md) Objekt aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **Attribute** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Attribute** -Objekt verfügt über diese Methoden.



| Methode                              | BESCHREIBUNG                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [**Eren**](attributes-add.md)       | Fügt der Auflistung ein [**Attribut**](attribute.md) Objekt hinzu.<br/>       |
| [**Klartext**](attributes-clear.md)   | Löscht alle [**Attribut**](attribute.md) Objekte aus der Auflistung.<br/> |
| [**Aufgeh**](attributes-remove.md) | Entfernt ein [**Attribut**](attribute.md) Objekt aus der Auflistung.<br/>  |



 

### <a name="properties"></a>Eigenschaften

Das **Attribute** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                           | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](attributes-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Countdown**](attributes-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl der [**Attribut**](attribute.md) Objekte in der Auflistung ab.<br/>                                                                                                                                    |
| [**Element**](attributes-item.md)<br/>         | Schreibgeschützt<br/> | Ruft das [**Attribut**](attribute.md) Objekt ab, das das indizierte Attribut darstellt. Dies ist die Standard Eigenschaft.<br/>                                                                                             |



 

## <a name="remarks"></a>Bemerkungen

Das **Attribute** -Objekt kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kryptografieobjekte](cryptography-objects.md)
</dt> </dl>

 

 
