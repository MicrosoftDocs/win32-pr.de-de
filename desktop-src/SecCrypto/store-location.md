---
description: Ruft den Speicherort des Zertifikat Speicher ab, der von diesem-Objekt dargestellt wird.
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Store. Location (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Location
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42afe40dffde5a0375928d355508ec75a4076f17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371780"
---
# <a name="storelocation-property"></a>Store. Location (Eigenschaft)

\[Die **Location** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Location** -Eigenschaft ruft den Speicherort des Zertifikat Speicher ab, der von diesem-Objekt dargestellt wird.

## <a name="syntax"></a>Syntax


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Eigenschaftswert

Der Wert des [**CAPICOM- \_ Speicher \_ Orts**](capicom-store-location.md) , der den Speicherort des Zertifikat Speicher darstellt.

## <a name="remarks"></a>Bemerkungen

Der Wert der **Location** -Eigenschaft entspricht dem Wert, der beim Öffnen des Stores für den *storeloation* -Parameter der [**Open**](store-open.md) -Methode bereitgestellt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,1 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Speicher**](store.md)
</dt> </dl>

 

 
