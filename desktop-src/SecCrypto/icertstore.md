---
description: Bietet Zugriff auf den Kontext eines CAPICOM-Speicher Objekts. In diesem Kontext kann der CAPICOM-Zertifikat Speicher in anderen Ableitungen von CryptoAPI verwendet werden.
ms.assetid: dc108e2d-d6ec-4972-9c8e-e6e738c25756
title: Icertstore-Schnittstelle
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
ms.openlocfilehash: 119609399709340049bc43693ac51f6259021416
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351338"
---
# <a name="icertstore-interface"></a>Icertstore-Schnittstelle

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **icertstore** -Schnittstelle bietet Zugriff auf den Kontext eines CAPICOM- [**Speicher**](store.md) Objekts. In diesem Kontext kann der CAPICOM-Zertifikat Speicher in anderen Ableitungen von CryptoAPI verwendet werden.

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Schnittstelle, wenn Sie ein CAPICOM- [**Speicher**](store.md) Objekt in einer anderen Ableitung von CryptoAPI verwenden müssen.

## <a name="members"></a>Member

Die **icertstore** -Schnittstelle verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **icertstore** -Schnittstelle verfügt über diese Methoden.



| Methode                                        | BESCHREIBUNG                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**CloseHandle**](icertstore-closehandle.md) | Schließt ein HCERTSTORE-handle, das über die [**storeHandle**](icertstore-storehandle.md) -Eigenschaft abgerufen wurde.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **icertstore** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                     | Zugriffstyp           | BESCHREIBUNG                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**StoreHandle**](icertstore-storehandle.md)<br/>     | Lesen/Schreiben<br/> | Legt das HCERTSTORE-Handle eines Zertifikat Speicher fest oder ruft es ab.<br/>                                          |
| [**StoreLocation**](icertstore-storelocation.md)<br/> | Lesen/Schreiben<br/> | Legt den [**CAPICOM- \_ \_ Speicherort**](capicom-store-location.md) eines Zertifikat Speicher fest oder ruft ihn ab.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




