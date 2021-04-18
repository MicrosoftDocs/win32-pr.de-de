---
description: Stellt eine Auflistung von Oid-Objekten dar.
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: OIDs-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 894689c214d8b7d352a2453d2d62c847866b9bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365941"
---
# <a name="oids-object"></a>OIDs-Objekt

\[Das **OIDs** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**OidCollection-Klasse**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Das **OIDs** -Objekt stellt eine Auflistung von [**OID**](oid.md) -Objekten dar. Jedes [**OID**](oid.md) -Objekt stellt einen einzelnen Objekt Bezeichner dar.

## <a name="when-to-use"></a>Verwendung

Das **OIDs** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Fügen Sie der Auflistung ein [**OID**](oid.md) -Objekt hinzu, oder entfernen Sie es.
-   Löschen Sie alle [**OID**](oid.md) -Objekte aus der Auflistung.
-   Ruft die Anzahl der Objekt Bezeichner in der Auflistung ab.
-   Ruft ein bestimmtes [**OID**](oid.md) -Objekt aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **OIDs** -Objekt verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **OIDs** -Objekt verfügt über diese Methoden.



| Methode                        | BESCHREIBUNG                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [**Eren**](oids-add.md)       | Fügt der Auflistung ein [**OID**](oid.md) -Objekt hinzu.<br/>              |
| [**Klartext**](oids-clear.md)   | Löscht alle [**OID**](oid.md) -Objekte aus der Auflistung.<br/>        |
| [**Aufgeh**](oids-remove.md) | Entfernt ein indiziertes [**OID**](oid.md) -Objekt aus der Auflistung.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **OIDs** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                     | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](oids-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Countdown**](oids-count.md)<br/>       | Schreibgeschützt<br/> | Ruft die Anzahl von [**OID**](oid.md) -Objekten in der Auflistung ab.<br/>                                                                                                                                                |
| [**Element**](oids-item.md)<br/>         | Schreibgeschützt<br/> | Ruft ein indiziertes [**OID**](oid.md) -Objekt aus der Auflistung ab. Dies ist die Standard Eigenschaft.<br/>                                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Das **OIDs** -Objekt kann nicht erstellt werden.

Das **OIDs** -Objekt wird von den folgenden Eigenschaften verwendet:

-   [**CertificateStatus. applicationpolicies**](certificatestatus-applicationpolicies.md)
-   [**CertificateStatus. certificatepolicies**](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
