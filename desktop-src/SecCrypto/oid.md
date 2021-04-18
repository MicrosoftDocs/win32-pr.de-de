---
description: Stellt einen Objekt Bezeichner (OID) dar, der von mehreren CAPICOM-Eigenschaften verwendet wird.
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: Oid-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a524bfd8d2eb2edcf3c97919129dd694414d5ace
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364489"
---
# <a name="oid-object"></a>Oid-Objekt

\[Das **OID** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**OID-Klasse**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Das **OID** -Objekt stellt einen [*Objekt Bezeichner*](../secgloss/o-gly.md) (OID) dar, der von mehreren CAPICOM-Eigenschaften verwendet wird.

## <a name="when-to-use"></a>Verwendung

Das **OID** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Festlegen oder Abrufen eines CAPICOM-namens und eines anzeigen Amens für die OID.
-   Festlegen oder Abrufen der gepunkteten Nummer für die OID.

## <a name="members"></a>Member

Das **OID** -Objekt verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **OID** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp           | BESCHREIBUNG                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**FriendlyName**](oid-friendlyname.md)<br/> | Lesen/Schreiben<br/> | Legt den anzeigen Amen für die OID fest oder ruft ihn ab.<br/>                                       |
| [**Name**](oid-name.md)<br/>                 | Lesen/Schreiben<br/> | Legt den von CAPICOM definierten Namen für die OID fest oder ruft ihn ab. Dies ist die Standard Eigenschaft.<br/> |
| [**Wert**](oid-value.md)<br/>               | Lesen/Schreiben<br/> | Legt den Wert der OID-gepunkteten Zahl der OID fest oder ruft ihn ab.<br/>                      |



 

## <a name="remarks"></a>Bemerkungen

Das **OID** -Objekt kann erstellt werden und ist für die Skripterstellung sicher. Die ProgID für das **OID** -Objekt ist CAPICOM. OID. 1.

Die folgenden CAPICOM-Objekteigenschaften geben ein **OID** -Objekt zurück:

-   [**Policyinformation. Oid**](policyinformation-oid.md)
-   [**Qualifizierer. Oid**](qualifier-oid.md)
-   [**Erweiterung. Oid**](extension-oid.md)
-   [**Template. Oid**](template-oid.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
