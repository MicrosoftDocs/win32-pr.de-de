---
description: Ruft ein Decoder-Objekt ab, sofern vorhanden.
ms.assetid: b8a1c7c9-e7ac-4b0e-a342-5b923ab83df3
title: Encodeddata. Decoder-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Decoder
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 334895ed683d0c582628b4b623a7343ca561be22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367752"
---
# <a name="encodeddatadecoder-method"></a>Encodeddata. Decoder-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**AsnEncodedData-Klasse**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **decodermethode** erhält ein Decoder-Objekt, sofern vorhanden.

## <a name="syntax"></a>Syntax


```VB
EncodedData.Decoder()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Wenn die codierten Daten nicht über ein Decoder-Objekt verfügen, wird **null** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
