---
description: 'Empfängerobjekt: Stellt eine Auflistung von Certificate-Objekten dar.'
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: Empfängerobjekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0f0f6474c6ed8883eb591591eff387fe387f7d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103738"
---
# <a name="recipients-object"></a>Empfängerobjekt

\[Das **Empfängerobjekt** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen die [**CmsRecipientCollection-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Das **Recipients-Objekt** stellt eine Auflistung von [**Certificate-Objekten**](certificate.md) dar. Jedes -Objekt stellt einen beabsichtigten Empfänger der umschlageten Nachricht dar. Daten in einem [**EnvelopedData-Objekt**](envelopeddata.md) werden mit einem [*symmetrischen*](../secgloss/s-gly.md) Sitzungsschlüssel verschlüsselt, und dieser symmetrische Sitzungsschlüssel wird dann selbst für jeden Empfänger verschlüsselt, indem der öffentliche Schlüssel aus dem Zertifikat des gewünschten Empfängers verwendet wird. Ein Empfänger mit Zugriff auf den [*privaten Schlüssel,*](../secgloss/p-gly.md) der dem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) eines Zertifikats zugeordnet ist, kann den [*Sitzungsschlüssel*](../secgloss/s-gly.md) entschlüsseln und den entschlüsselten Sitzungsschlüssel verwenden, um die tatsächlichen Daten zu entschlüsseln.

## <a name="when-to-use"></a>Verwendung

Das **Recipients-Objekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Hinzufügen oder Entfernen eines [**Certificate-Objekts**](certificate.md) aus der Auflistung.
-   Ruft die Anzahl der Zertifikate in der Auflistung ab.
-   Rufen Sie ein bestimmtes **Empfängerobjekt** aus der Auflistung ab.
-   Durchlaufen sie die Auflistung.

## <a name="members"></a>Member

Das **Recipients-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Recipients-Objekt** verfügt über diese Methoden.



| Methode                              | BESCHREIBUNG                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [**Hinzufügen**](recipients-add.md)       | Fügt der Auflistung ein [**Certificate-Objekt**](certificate.md) hinzu.<br/>         |
| [**Löschen**](recipients-clear.md)   | Entfernt alle [**Certificate-Objekte**](certificate.md) aus der Auflistung.<br/> |
| [**Entfernen**](recipients-remove.md) | Entfernt ein [**Certificate-Objekt**](certificate.md) aus der Auflistung.<br/>    |



 

### <a name="properties"></a>Eigenschaften

Das **Recipients-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                           | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](recipients-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für ein Objekt ab, das zum Aufzählen der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Anzahl**](recipients-count.md)<br/>       |                      | Die Anzahl der Objekte in der **Recipients-Auflistung.**<br/>                                                                                                                                                              |
| [**Element**](recipients-item.md)<br/>         |                      | Ein indiziertes Objekt in der Auflistung. Dies ist die Standardeigenschaft.<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Das **Recipients-Objekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
