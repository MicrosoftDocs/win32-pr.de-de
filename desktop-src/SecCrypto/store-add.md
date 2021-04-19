---
description: Fügt einem geöffneten Zertifikat Speicher ein Zertifikat Objekt hinzu.
ms.assetid: 787b8a41-dcdb-4b5b-a1fd-f5424300361b
title: Store. Add-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d217c784fa5f994e88ee2de78f2e1944091d724
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365682"
---
# <a name="storeadd-method"></a>Store. Add-Methode

\[Die **Add** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Store-Klasse**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Mit der **Add** -Methode wird einem geöffneten [*Zertifikat Speicher*](../secgloss/c-gly.md)ein [**Zertifikat**](certificate.md) Objekt hinzugefügt. Diese Methode kann nur mit einem Speicher verwendet werden, der mit Lese-/Schreibberechtigung geöffnet wurde.

## <a name="syntax"></a>Syntax


```VB
Store.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zertifikat* \[ in\]
</dt> <dd>

Ein Ausdruck, der zu einem [**Zertifikat**](certificate.md) Objekt aufgelöst wird, das dem Speicher hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

> [!IMPORTANT]
> Wenn diese Methode von einem Webskript in einem Systemspeicher aufgerufen wird, muss das Skript auf die digitalen Zertifikate auf dem lokalen Computer zugreifen. Wenn Sie zulassen, dass das Skript auf Ihre digitalen Zertifikate zugreift, erhält die Website, von der aus das Skript ausgeführt wird, auch Zugriff auf alle persönlichen Informationen, die in den Zertifikaten gespeichert sind. Wenn diese Methode zum ersten Mal von einer bestimmten Domäne aufgerufen wird, wird ein Dialogfeld generiert, in dem der Benutzer angeben muss, ob der Zugriff auf die Zertifikate zulässig sein soll.

 

Wenn der Speicher nicht im Lese-/Schreibmodus geöffnet ist, schlägt diese Methode fehl. Obwohl diese Methode mit Speicher speichern verwendet werden kann, werden alle Änderungen, die an einem Speicher Speicher vorgenommen werden, beim Schließen des Speichers nicht beibehalten.

Wenn das Zertifikat, das dem Speicher hinzugefügt wird, identisch mit dem Zertifikat ist, das bereits vorhanden ist, löscht die **Add** -Methode das vorhandene Zertifikat aus dem Speicher und fügt dann das neue Zertifikat hinzu. Das neue Zertifikat erbt die Eigenschaften des vorhandenen Zertifikats.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Speicher**](store.md)
</dt> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
