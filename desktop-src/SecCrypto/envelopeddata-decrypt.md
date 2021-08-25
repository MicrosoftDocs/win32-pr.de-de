---
description: Entschlüsselt umschlageten Inhalt.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: EnvelopedData.Decrypt-Methode
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
ms.openlocfilehash: 5f1c754e23977ac9c7af7f4fd3feaade13c928e9522a2285102a095fff4740b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874260"
---
# <a name="envelopeddatadecrypt-method"></a>EnvelopedData.Decrypt-Methode

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**EnvelopedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Decrypt-Methode** entschlüsselt umschlageten Inhalt. Die Entschlüsselung erfolgt, wenn der Empfänger der Nachricht Zugriff auf den [*privaten Schlüssel*](../secgloss/p-gly.md) hat, der mit einem der [*öffentlichen Schlüssel*](../secgloss/p-gly.md) gekoppelt ist, die zum Umschwenden der Nachricht verwendet werden. Durch Aufrufen der **Decrypt-Methode** wird der [*Zustand*](../secgloss/s-gly.md) des Objekts zurückgesetzt. Wenn die **Decrypt-Methode** erfolgreich ist, wird die [**Content-Eigenschaft**](envelopeddata-content.md) des [**EnvelopedData-Objekts**](envelopeddata.md) auf die Klartextnachricht festgelegt.

## <a name="syntax"></a>Syntax


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EnvelopedMessage* \[ In\]
</dt> <dd>

Zeichenfolge, die die zu entschlüsselnden Umschlagdaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die entschlüsselten Daten werden zum [**Content-Eigenschaftswert**](envelopeddata-content.md) für das [**EnvelopedData-Objekt.**](envelopeddata.md)

Wenn der Benutzer dieser Methode keinen Zugriff auf einen privaten Schlüssel hat, der mit einem der öffentlichen Schlüssel übereinstimmt, die zum Umgestalten der Nachricht verwendet werden, schlägt die -Methode fehl. Bei dieser Methode tritt ein Fehler auf, wenn sich das Zertifikat für den zugeordneten privaten Schlüssel weder im MY Store des lokalen Computers noch im MY-Speicher des aktuellen Benutzers befindet.

> [!IMPORTANT]
> Wenn diese Methode von einem Webskript aufgerufen wird, muss das Skript Ihren [*privaten Schlüssel*](../secgloss/p-gly.md) verwenden, um die Daten zu entschlüsseln. Das Zulassen der Verwendung Ihres privaten Schlüssels durch nicht vertrauenswürdige Websites ist ein Sicherheitsrisiko. Ein Dialogfeld mit der Frage, ob die Website Ihren privaten Schlüssel verwenden kann, wird angezeigt, wenn diese Methode zum ersten Mal aufgerufen wird. Wenn Sie zulassen, dass das Skript Ihren privaten Schlüssel verwendet, und wählen Sie "Nicht mehr fragen" aus, wird das Dialogfeld nicht mehr für Skripts angezeigt, die Ihren privaten Schlüssel zum Entschlüsseln von Daten in dieser Domäne verwenden. Skripts außerhalb dieser Domäne, die versuchen, Ihren privaten Schlüssel zum Entschlüsseln von Daten zu verwenden, führen jedoch weiterhin dazu, dass dieses Dialogfeld angezeigt wird. Wenn Sie dem Skript die Verwendung Ihres privaten Schlüssels nicht gestatten und "Nicht mehr fragen" auswählen, wird Skripts in dieser Domäne automatisch die Möglichkeit verweigert, Ihren privaten Schlüssel zum Entschlüsseln von Daten zu verwenden.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
