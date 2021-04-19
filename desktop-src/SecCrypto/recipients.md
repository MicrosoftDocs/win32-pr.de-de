---
description: Stellt eine Auflistung von Zertifikat Objekten dar.
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: Empfänger Objekt
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
ms.openlocfilehash: c68ca0217631970f35680160b71841f758b13fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355269"
---
# <a name="recipients-object"></a>Empfänger Objekt

\[Das Objekt " **Empfänger** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**cmsrecepentcollection-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Das **Empfängers** -Objekt stellt eine Auflistung von [**Zertifikat**](certificate.md) Objekten dar. Jedes-Objekt stellt einen beabsichtigten Empfänger der eingeschlossenen Nachricht dar. Daten in einem [**EnvelopedData**](envelopeddata.md) -Objekt werden mit einem [*symmetrischen*](../secgloss/s-gly.md) Sitzungsschlüssel verschlüsselt, und dieser symmetrische Sitzungsschlüssel wird dann selbst für jeden Empfänger verschlüsselt, indem der öffentliche Schlüssel aus dem Zertifikat dieses gewünschten Empfängers verwendet wird. Ein Empfänger mit Zugriff auf den [*privaten Schlüssel*](../secgloss/p-gly.md) , der dem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) eines Zertifikats zugeordnet ist, kann den [*Sitzungsschlüssel*](../secgloss/s-gly.md) entschlüsseln und den entschlüsselten Sitzungsschlüssel verwenden, um die eigentlichen Daten zu entschlüsseln.

## <a name="when-to-use"></a>Verwendung

Das Objekt " **Empfänger** " wird verwendet, um die folgenden Aufgaben auszuführen:

-   Fügen Sie ein [**Zertifikat**](certificate.md) Objekt der Auflistung hinzu, oder entfernen Sie es.
-   Ruft die Anzahl der Zertifikate in der Sammlung ab.
-   Rufen Sie ein bestimmtes **Empfänger** Objekt aus der Auflistung ab.
-   Iterieren Sie die Auflistung.

## <a name="members"></a>Member

Das **Empfänger** Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Empfänger** Objekt verfügt über diese Methoden.



| Methode                              | BESCHREIBUNG                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [**Eren**](recipients-add.md)       | Fügt der Auflistung ein [**Zertifikat**](certificate.md) Objekt hinzu.<br/>         |
| [**Klartext**](recipients-clear.md)   | Entfernt alle [**Zertifikat**](certificate.md) Objekte aus der Auflistung.<br/> |
| [**Aufgeh**](recipients-remove.md) | Entfernt ein [**Zertifikat**](certificate.md) Objekt aus der Auflistung.<br/>    |



 

### <a name="properties"></a>Eigenschaften

Das **Empfänger** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                           | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](recipients-newenum.md)<br/> | Schreibgeschützt<br/> | Ruft eine [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle für ein Objekt ab, das zum Auflisten der Auflistung verwendet werden kann. Diese Eigenschaft wird in Visual Basic Scripting Edition (VBScript) ausgeblendet.<br/> |
| [**Countdown**](recipients-count.md)<br/>       |                      | Die Anzahl der-Objekte in der **Empfänger** Auflistung.<br/>                                                                                                                                                              |
| [**Element**](recipients-item.md)<br/>         |                      | Ein indiziertes Objekt in der Auflistung. Dies ist die Standard Eigenschaft.<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Das **Empfänger** Objekt kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
