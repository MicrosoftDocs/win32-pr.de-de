---
description: Die Import Methode kopiert den Inhalt eines zuvor exportierten Zertifikat Speicher in einen geöffneten Zertifikat Speicher. Diese Methode kann nur mit einem Speicher verwendet werden, der mit Lese-/Schreibberechtigung geöffnet wurde.
ms.assetid: 22db8f1c-469b-4baf-9039-4da35c9c6aa0
title: Store. Import-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4eb16cc341eb6e5dcee87216a52e9e3de94d1b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359712"
---
# <a name="storeimport-method"></a>Store. Import-Methode

\[Die **Import** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Store-Klasse**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Import** Methode kopiert den Inhalt eines zuvor exportierten Zertifikat Speicher in einen geöffneten [*Zertifikat Speicher*](../secgloss/c-gly.md) . Diese Methode kann nur mit einem Speicher verwendet werden, der mit Lese-/Schreibberechtigung geöffnet wurde.

## <a name="syntax"></a>Syntax


```VB
Store.Import( _
  ByVal EncodedStore _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Encodstore* \[ in\]
</dt> <dd>

Die Zeichenfolge, die die zu importierenden codierten Zertifikate enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

> [!IMPORTANT]
> Wenn diese Methode von einem Webskript aufgerufen wird, muss das Skript auf die digitalen Zertifikate auf dem lokalen Computer zugreifen. Wenn Sie zulassen, dass das Skript auf Ihre digitalen Zertifikate zugreift, erhält die Website, von der aus das Skript ausgeführt wird, auch Zugriff auf alle persönlichen Informationen, die in den Zertifikaten gespeichert sind. Wenn diese Methode zum ersten Mal von einer bestimmten Domäne aufgerufen wird, wird ein Dialogfeld generiert, in dem der Benutzer angeben muss, ob der Zugriff auf die Zertifikate zulässig sein soll.

 

Wenn der Speicher nicht mit Lese-/Schreibberechtigungen geöffnet wird, schlägt diese Methode fehl. Obwohl diese Methode mit Speicher speichern verwendet werden kann, werden alle Änderungen, die an einem Speicher Speicher vorgenommen werden, beim Schließen des Speichers nicht beibehalten.

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

 

 
