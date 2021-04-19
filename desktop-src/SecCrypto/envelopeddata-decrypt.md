---
description: Entschlüsselt den eingeschlossenen Inhalt.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: EnvelopedData. entschlpt-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c4c71ba0e3e0c2d421ad7bcbc9b1a61bb71d284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352979"
---
# <a name="envelopeddatadecrypt-method"></a>EnvelopedData. entschlpt-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**EnvelopedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Mit  der Entschlüsselungsmethode werden eingeschlossene Inhalte entschlüsselt. Die Entschlüsselung erfolgt, wenn der Empfänger der Nachricht Zugriff auf den [*privaten Schlüssel*](../secgloss/p-gly.md) hat, der mit einem der [*öffentlichen*](../secgloss/p-gly.md) Schlüssel gekoppelt ist, die zum Umhüllen der Nachricht verwendet werden. Durch Aufrufen der **Entschlüsselungsmethode** wird der [*Zustand*](../secgloss/s-gly.md) des-Objekts zurückgesetzt. Wenn die **Entschlüsselungsmethode** erfolgreich ist, wird die [**Content**](envelopeddata-content.md) -Eigenschaft des [**EnvelopedData**](envelopeddata.md) -Objekts auf die Klartext-Nachricht festgelegt.

## <a name="syntax"></a>Syntax


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Envelopedmessage* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die die zu entschlüsselnden Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die entschlüsselten Daten werden zu dem [**Content**](envelopeddata-content.md) -Eigenschafts Wert für das [**EnvelopedData**](envelopeddata.md) -Objekt.

Wenn der Benutzer dieser Methode keinen Zugriff auf einen privaten Schlüssel hat, der mit einem der öffentlichen Schlüssel übereinstimmt, die zum Umhüllen der Nachricht verwendet werden, schlägt die Methode fehl. Bei dieser Methode tritt ein Fehler auf, wenn sich das Zertifikat für den zugeordneten privaten Schlüssel weder auf dem lokalen Computer als auch auf dem Speicher des aktuellen Benutzers befindet.

> [!IMPORTANT]
> Wenn diese Methode von einem Webskript aufgerufen wird, muss das Skript den [*privaten Schlüssel*](../secgloss/p-gly.md) verwenden, um die Daten zu entschlüsseln. Es ist ein Sicherheitsrisiko, nicht vertrauenswürdige Websites den privaten Schlüssel zu verwenden. Wenn diese Methode erstmals aufgerufen wird, wird ein Dialogfeld angezeigt, in dem Sie gefragt werden, ob die Website den privaten Schlüssel verwenden kann. Wenn Sie zulassen, dass das Skript den privaten Schlüssel verwendet, und wählen Sie "nicht mehr nachfragen", wird das Dialogfeld nicht mehr für Skripts angezeigt, die Ihren privaten Schlüssel zum Entschlüsseln von Daten in dieser Domäne verwenden. Skripts außerhalb dieser Domäne, die versuchen, den privaten Schlüssel zum Entschlüsseln von Daten zu verwenden, werden jedoch dennoch dazu führen, dass dieses Dialogfeld angezeigt wird. Wenn Sie dem Skript nicht gestatten, Ihren privaten Schlüssel zu verwenden, und die Option "Diese Meldung nicht mehr anzeigen" auswählen, wird die Möglichkeit der Verwendung Ihres privaten Schlüssels für das Entschlüsseln von Daten automatisch verweigert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
