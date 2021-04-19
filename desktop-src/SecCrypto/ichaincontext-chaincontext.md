---
description: Legt den pccert- \_ Ketten Kontext eines Zertifikats fest oder ruft ihn ab \_ .
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: 'Ichaincontext:: ChainContext-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36b2f6f5811c844e4e43544f5b56b8de66cb3bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355281"
---
# <a name="ichaincontextchaincontext-property"></a>Ichaincontext:: ChainContext-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **chainContext** -Eigenschaft legt den pccert- \_ Ketten \_ Kontext eines Zertifikats fest oder ruft ihn ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a>Eigenschaftswert

Der pccert- \_ Ketten \_ Kontext des Zertifikats.

## <a name="error-codes"></a>Fehlercodes

Wenn die Eigenschaften Zugriffsmethoden **\_ chainContext platzieren** und **\_ chainContext** erfolgreich abrufen, geben Sie S \_ OK zurück.

Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Zum Freigeben des Kontexts muss entweder die [**freecontext**](ichaincontext-freecontext.md) -Methode oder die [**certfreecertificatechain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) -Funktion aufgerufen werden.

Wenn Sie die **chainContext** -Eigenschaft festlegen, wird der Status des gesamten [**Kette**](chain.md) -Objekts zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ichaincontext**](ichaincontext.md)
</dt> </dl>

 

 




