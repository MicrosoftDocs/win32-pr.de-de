---
description: Legt den CAPICOM \_ STORE LOCATION eines Zertifikatspeichers fest oder ruft sie \_ ab.
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: ICertStore::StoreLocation-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreLocation
- ICertStore.get_StoreLocation
- ICertStore.put_StoreLocation
- CertStore.StoreLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea11da4fc908a2a3b665b2491614dbffeaa3034a3127617c562c3365522df835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005608"
---
# <a name="icertstorestorelocation-property"></a>ICertStore::StoreLocation-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **StoreLocation-Eigenschaft** legt den [**CAPICOM STORE LOCATION eines \_ \_**](capicom-store-location.md) Zertifikatspeichers fest oder ruft sie ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Eigenschaftswert

Der Speicherort des Zertifikatspeichers.

## <a name="error-codes"></a>Fehlercodes

Wenn die Eigenschaftenzugriffsmethoden **\_ StoreLocation setzen** und **\_ StoreLocation** erfolgreich abrufen, geben sie S \_ OK zurück.

Jeder andere **HRESULT-Wert** gibt an, dass der Aufruf fehlgeschlagen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




