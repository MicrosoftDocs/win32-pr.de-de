---
description: Stellt den einem Zertifikat zugeordneten privaten Schlüssel dar.
ms.assetid: 26ad1d1c-17c5-4191-ac97-b911e62b4119
title: PrivateKey-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e87ca7a5bf12bbaf943bccacaa075a51ae75ed37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364804"
---
# <a name="privatekey-object"></a>PrivateKey-Objekt

\[Das **PrivateKey** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Certificate2. PrivateKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Das **PrivateKey** -Objekt stellt den einem Zertifikat zugeordneten [*privaten Schlüssel*](../secgloss/p-gly.md) dar.

## <a name="when-to-use"></a>Verwendung

Das **PrivateKey** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Abrufen von Informationen zum privaten Schlüssel.
-   Öffnen Sie den Container für den privaten Schlüssel.
-   Löschen Sie den privaten Schlüssel.

## <a name="members"></a>Member

Das **PrivateKey** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **PrivateKey** -Objekt verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                                                                                                                          |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Lösch**](privatekey-delete.md)                     | Löscht den Container für den privaten Schlüssel, auf den vom **PrivateKey** -Objekt verwiesen wird.<br/>                                                                                |
| [**IsAccessible**](privatekey-isaccessible.md)         | Ruft einen booleschen Wert ab, der angibt, ob der Benutzer auf den privaten Schlüssel zugreifen kann. True gibt an, dass der Benutzer auf den privaten Schlüssel zugreifen kann.<br/>                 |
| [**IsExportable**](privatekey-isexportable.md)         | Ruft einen booleschen Wert ab, der angibt, ob der private Schlüssel exportiert werden kann. True gibt an, dass der private Schlüssel exportiert werden kann.<br/>                               |
| [**Ishardwaredevice**](privatekey-ishardwaredevice.md) | Ruft einen booleschen Wert ab, der angibt, ob der private Schlüssel auf einem Hardware Gerät gespeichert ist. True gibt an, dass der private Schlüssel auf einem Hardware Gerät gespeichert wird.<br/> |
| [**Ismachinekeyset**](privatekey-ismachinekeyset.md)   | Ruft einen booleschen Wert ab, der angibt, ob der private Schlüssel ein Computer Schlüssel ist. True gibt an, dass der private Schlüssel ein Computer Schlüssel ist.<br/>                             |
| [**Isprotehiert**](privatekey-isprotected.md)           | Ruft einen booleschen Wert ab, der angibt, ob der private Schlüssel geschützt ist. True gibt an, dass der private Schlüssel geschützt ist.<br/>                                     |
| [**Iswechsel**](privatekey-isremovable.md)           | Ruft einen booleschen Wert ab, der angibt, ob sich der private Schlüssel auf einem Wechselmedium befindet. True gibt an, dass sich der private Schlüssel auf einem Wechsel Datenträger befindet.<br/>             |
| [**Eren**](privatekey-open.md)                         | Greift auf einen vorhandenen Schlüssel Container zu.<br/>                                                                                                                       |



 

### <a name="properties"></a>Eigenschaften

Das **PrivateKey** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                 | Zugriffstyp          | BESCHREIBUNG                                                                                               |
|:-------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------|
| [**Container Name**](privatekey-containername.md)<br/>             | Schreibgeschützt<br/> | Ruft eine Zeichenfolge ab, die den Namen des privaten Schlüssel Containers enthält. Dies ist die Standard Eigenschaft.<br/> |
| [**KeySpec**](privatekey-keyspec.md)<br/>                         | Schreibgeschützt<br/> | Ruft die Schlüssel Spezifikation ab.<br/>                                                               |
| [**ProviderName**](privatekey-providername.md)<br/>               | Schreibgeschützt<br/> | Ruft eine Zeichenfolge ab, die den Namen des CSP enthält.<br/>                                          |
| [**ProviderType**](privatekey-providertype.md)<br/>               | Schreibgeschützt<br/> | Ruft einen Enumerationswert ab, der den Typ des Anbieters angibt.<br/>                            |
| [**Uniquecontainername**](privatekey-uniquecontainername.md)<br/> | Schreibgeschützt<br/> | Ruft eine Zeichenfolge ab, die den eindeutigen Container Namen des privaten Schlüssels enthält.<br/>                        |



 

## <a name="remarks"></a>Bemerkungen

Das **PrivateKey** -Objekt kann erstellt werden und ist für die Skripterstellung sicher. Die ProgID für das **PrivateKey** -Objekt ist CAPICOM. PrivateKey. 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
