---
description: Legt den CAPICOM- \_ \_ Speicherort eines Zertifikat Speicher fest oder ruft ihn ab.
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: 'Icertstore:: storelokation-Eigenschaft'
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
ms.openlocfilehash: 97bca7ed9dae20c129d202910b40f7c26d54a576
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359397"
---
# <a name="icertstorestorelocation-property"></a>Icertstore:: storelokation-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **storelokation** -Eigenschaft legt den [**CAPICOM- \_ \_ Speicherort**](capicom-store-location.md) eines Zertifikat Speicher fest oder ruft ihn ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Eigenschaftswert

Der Speicherort des Zertifikatspeichers.

## <a name="error-codes"></a>Fehlercodes

Wenn die Eigenschaften Zugriffsmethoden **\_ storeloation ablegen** und **\_ storelokation** erfolgreich abrufen, geben Sie S \_ OK zurück.

Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icertstore**](icertstore.md)
</dt> </dl>

 

 




