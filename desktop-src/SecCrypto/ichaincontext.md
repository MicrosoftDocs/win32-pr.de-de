---
description: Bietet Zugriff auf den Kontext eines CAPICOM-Ketten Objekts. In diesem Kontext kann die CAPICOM-Zertifikats Vertrauenskette in anderen Ableitungen von CryptoAPI verwendet werden.
ms.assetid: ee258586-028e-486e-8129-07f43b6cc468
title: Ichaincontext-Schnittstelle
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
ms.openlocfilehash: 34ba471c50ceb9475121139c3ecb997cf1d26f2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361266"
---
# <a name="ichaincontext-interface"></a>Ichaincontext-Schnittstelle

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **ichaincontext** -Schnittstelle bietet Zugriff auf den Kontext eines CAPICOM- [**Ketten**](chain.md) Objekts. In diesem Kontext kann die CAPICOM-Zertifikats Vertrauenskette in anderen Ableitungen von CryptoAPI verwendet werden.

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Schnittstelle, wenn Sie in einer anderen Ableitung von CryptoAPI ein CAPICOM- [**Ketten**](chain.md) Objekt verwenden müssen.

## <a name="members"></a>Member

Die **ichaincontext** -Schnittstelle verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ichaincontext** -Schnittstelle verfügt über diese Methoden.



| Methode                                           | BESCHREIBUNG                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Freecontext**](ichaincontext-freecontext.md) | Gibt einen pccert- \_ Ketten kontextfrei, \_ der über die [**chainContext**](ichaincontext-chaincontext.md) -Eigenschaft abgerufen wurde.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **ichaincontext** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Zugriffstyp           | BESCHREIBUNG                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [**ChainContext**](ichaincontext-chaincontext.md)<br/> | Lesen/Schreiben<br/> | Legt den pccert- \_ Ketten Kontext eines Zertifikats fest oder ruft ihn ab \_ .<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




