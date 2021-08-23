---
description: Ermöglicht den Zugriff auf den Kontext eines CAPICOM-Store Objekts. Dieser Kontext ermöglicht die Verwendung des CAPICOM-Zertifikatspeichers in anderen Ableitungen von CryptoAPI.
ms.assetid: dc108e2d-d6ec-4972-9c8e-e6e738c25756
title: ICertStore-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a48913b4bfb1fc28b612437a8f3b6934941c19b22683913f68d59f3f11d9e1c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005578"
---
# <a name="icertstore-interface"></a>ICertStore-Schnittstelle

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **ICertStore-Schnittstelle** ermöglicht den Zugriff auf den Kontext eines CAPICOM-Store Objekts. [](store.md) Dieser Kontext ermöglicht die Verwendung des CAPICOM-Zertifikatspeichers in anderen Ableitungen von CryptoAPI.

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Schnittstelle, wenn Sie [](store.md) ein CAPICOM-Store in einer anderen Ableitung von CryptoAPI verwenden müssen.

## <a name="members"></a>Member

Die **ICertStore-Schnittstelle** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ICertStore-Schnittstelle** verfügt über diese Methoden.



| Methode                                        | Beschreibung                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**Closehandle**](icertstore-closehandle.md) | Schließt ein HCERTSTORE-Handle, das über die [**StoreHandle-Eigenschaft erworben**](icertstore-storehandle.md) wurde.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **ICertStore-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                     | Zugriffstyp           | Beschreibung                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**Storehandle**](icertstore-storehandle.md)<br/>     | Lesen/Schreiben<br/> | Legt das HCERTSTORE-Handle eines Zertifikatspeichers fest oder ruft es ab.<br/>                                          |
| [**Storelocation**](icertstore-storelocation.md)<br/> | Lesen/Schreiben<br/> | Legt den [**CAPICOM \_ STORE \_ LOCATION eines Zertifikatspeichers**](capicom-store-location.md) fest oder ruft diese ab.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




