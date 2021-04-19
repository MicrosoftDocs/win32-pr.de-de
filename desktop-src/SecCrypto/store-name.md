---
description: Ruft den Namen des Zertifikat Speicher ab, der von diesem-Objekt dargestellt wird.
ms.assetid: db61b464-0e8e-4b19-be12-04e00d6bba53
title: Store.Name-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85679bb594bdb59c41773b7f956deea95021381f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372516"
---
# <a name="storename-property"></a>Store.Name-Eigenschaft

\[Die [**Name**](store-location.md) -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die [**Name**](store-location.md) -Eigenschaft ruft den Namen des Zertifikat Speicher ab, der von diesem-Objekt dargestellt wird.

## <a name="syntax"></a>Syntax


```VB
Store.Name As String
```



## <a name="property-value"></a>Eigenschaftswert

Der **Zeichen** folgen Wert, der den Namen des Zertifikat Speicher darstellt.

## <a name="remarks"></a>Bemerkungen

Beispiele für Zertifikat Speicher Namen sind My und root.

Der Wert der [**Name**](store-location.md) -Eigenschaft ist identisch mit dem Wert, der beim Öffnen des Stores für den *StoreName* -Parameter der [**Open**](store-open.md) -Methode bereitgestellt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,1 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Speicher**](store.md)
</dt> </dl>

 

 
