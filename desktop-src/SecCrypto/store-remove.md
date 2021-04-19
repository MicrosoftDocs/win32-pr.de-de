---
description: Die Remove-Methode entfernt ein Zertifikat aus einem geöffneten Zertifikat Speicher. Diese Methode kann nur mit einem Speicher verwendet werden, der mit Lese-/Schreibberechtigung geöffnet wurde.
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Store. Remove-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 188553d6091314e1a872145219ea321d581b35c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368384"
---
# <a name="storeremove-method"></a>Store. Remove-Methode

\[Die **Remove** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Remove** -Methode entfernt ein [*Zertifikat*](../secgloss/c-gly.md) aus einem geöffneten [*Zertifikat Speicher*](../secgloss/c-gly.md). Diese Methode kann nur mit einem Speicher verwendet werden, der mit Lese-/Schreibberechtigung geöffnet wurde.

## <a name="syntax"></a>Syntax


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zertifikat* \[ in\]
</dt> <dd>

Ein Ausdruck, der zu einer Instanz eines [**Zertifikat**](certificate.md) Objekts aufgelöst wird, das aus dem Speicher entfernt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

> [!IMPORTANT]
> Wenn diese Methode von einem Webskript aufgerufen wird, muss das Skript digitale Zertifikate vom lokalen Computer löschen. Das Löschen digitaler Zertifikate durch nicht vertrauenswürdige Websites ist ein Sicherheitsrisiko. Ein Dialogfeld, in dem Sie gefragt werden, ob die Website Zertifikate löschen kann, wenn diese Methode zum ersten Mal aufgerufen wird. Wenn Sie der Anwendung das Löschen von Zertifikaten gestatten und dieses Dialogfeld nicht mehr anzeigen auswählen, wird das Dialogfeld nicht mehr für Skripts angezeigt, die Zertifikate innerhalb dieser Domäne löschen. Skripts außerhalb dieser Domäne, die versuchen, Zertifikate zu löschen, werden jedoch dennoch dazu führen, dass dieses Dialogfeld angezeigt wird. Wenn Sie das Skript nicht für das Löschen von Zertifikaten zulassen und das Kontrollkästchen Dieses Dialogfeld nicht mehr anzeigen aktivieren, wird das Löschen von Zertifikaten automatisch verweigert.

 

Wenn Sie ein Zertifikat aus einem Speicher löschen, sollten Sie zuerst den dem Zertifikat zugeordneten privaten Schlüssel löschen.

Wenn der Speicher nicht mit Lese-/Schreibberechtigungen geöffnet ist, schlägt diese Methode fehl. Obwohl diese Methode mit Speicher speichern verwendet werden kann, werden alle Änderungen, die an einem Speicher Speicher vorgenommen werden, beim Schließen des Speichers nicht beibehalten.

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

 

 
