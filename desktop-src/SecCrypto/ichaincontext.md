---
description: Ermöglicht den Zugriff auf den Kontext eines CAPICOM Chain-Objekts. Dieser Kontext ermöglicht die Verwendung der CAPICOM-Zertifikatvertrauenskette in anderen Ableitungen von CryptoAPI.
ms.assetid: ee258586-028e-486e-8129-07f43b6cc468
title: IChainContext-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a3ac2f2234c986c9a86073e25e1277fa1af4f10f2809e013bc65849120b90c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005438"
---
# <a name="ichaincontext-interface"></a>IChainContext-Schnittstelle

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **IChainContext-Schnittstelle** ermöglicht den Zugriff auf den Kontext eines CAPICOM [**Chain-Objekts.**](chain.md) Dieser Kontext ermöglicht die Verwendung der CAPICOM-Zertifikatvertrauenskette in anderen Ableitungen von CryptoAPI.

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Schnittstelle, wenn Sie ein CAPICOM [**Chain-Objekt**](chain.md) in einer anderen Ableitung von CryptoAPI verwenden müssen.

## <a name="members"></a>Member

Die **IChainContext-Schnittstelle** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IChainContext-Schnittstelle** verfügt über diese Methoden.



| Methode                                           | Beschreibung                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**FreeContext**](ichaincontext-freecontext.md) | Gibt einen PCCERT \_ CHAIN \_ CONTEXT frei, der über die [**ChainContext-Eigenschaft erworben**](ichaincontext-chaincontext.md) wurde.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IChainContext-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Zugriffstyp           | Beschreibung                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [**ChainContext**](ichaincontext-chaincontext.md)<br/> | Lesen/Schreiben<br/> | Legt den PCCERT CHAIN CONTEXT eines Zertifikats \_ fest oder ruft sie \_ ab.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




