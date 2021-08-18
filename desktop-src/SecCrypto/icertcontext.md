---
description: Ermöglicht den Zugriff auf den Kontext eines CAPICOM X.509v3-Zertifikatobjekts. Dieser Kontext ermöglicht die Verwendung des CAPICOM-Zertifikats in anderen Ableitungen von CryptoAPI.
ms.assetid: 084a3a7b-7523-419f-a504-6fd397030d78
title: ICertContext-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 693e259c730209049f669d1499001d026b3d11088c7bef09616826a4673cac0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006038"
---
# <a name="icertcontext-interface"></a>ICertContext-Schnittstelle

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **ICertContext-Schnittstelle** ermöglicht den Zugriff auf den Kontext eines CAPICOM X.509v3-Zertifikatobjekts. [](certificate.md) Dieser Kontext ermöglicht die Verwendung des CAPICOM-Zertifikats in anderen Ableitungen von CryptoAPI.

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Schnittstelle, wenn Sie [](certificate.md) ein CAPICOM-Zertifikatobjekt in einer anderen Ableitung von CryptoAPI verwenden müssen.

## <a name="members"></a>Member

Die **ICertContext-Schnittstelle** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ICertContext-Schnittstelle** verfügt über diese Methoden.



| Methode                                          | Beschreibung                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**FreeContext**](icertcontext-freecontext.md) | Gibt einen PCCERT \_ CONTEXT frei, der über die [**CertContext-Eigenschaft erworben**](icertcontext-certcontext.md) wurde.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **ICertContext-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                   | Zugriffstyp           | Beschreibung                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**CertContext**](icertcontext-certcontext.md)<br/> | Lesen/Schreiben<br/> | Legt den PCCERT CONTEXT eines Zertifikats \_ fest oder ruft sie ab.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




