---
description: Ruft eine angegebene Anzahl zufälliger Bytes aus dem Zufallszahlengenerator des Systems ab.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: SystemPrng-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemPrng
api_type:
- DllExport
api_location:
- Ksecdd.sys
- Cng.sys
ms.openlocfilehash: eae1a46b43278c836ff6ce318dfdce7302bb0e052664a7326f9043a60eec72d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905629"
---
# <a name="systemprng-function"></a>SystemPrng-Funktion

\[**SystemPrng ist** für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]

Die **SystemPrng-Funktion** ruft eine angegebene Anzahl zufälliger Bytes aus dem Zufallszahlengenerator des Systems ab.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie eine benutzerdefinierte Headerdatei erstellen.

 

## <a name="syntax"></a>Syntax


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbRandomData* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die abgerufenen Bytes empfängt.

</dd> <dt>

*cbRandomData* \[ In\]
</dt> <dd>

Die Anzahl der abzurufenden Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **TRUE zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Vista mit \[ SP1-Desktop-Apps\]<br/>                                                                                                                                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                                                                                                           |
| DLL<br/>                      | <dl> <dt>Ksecdd.sys unter Windows Server 2008 und Windows Vista mit SP1;</dt> <dt>Cng.sys auf Windows 7 und Windows Server 2008 R2</dt> </dl> |



 

 




