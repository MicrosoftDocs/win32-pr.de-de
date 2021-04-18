---
description: Ruft eine angegebene Anzahl zufälliger Bytes aus dem System Zufallszahlen-Generator ab.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: Systemprng-Funktion
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
ms.openlocfilehash: d847d34ffd11e158170f55599de0ceb3acf3c697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344058"
---
# <a name="systemprng-function"></a>Systemprng-Funktion

\[**Systemprng** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]

Die **systemprng** -Funktion Ruft eine angegebene Anzahl zufälliger Bytes aus dem System Zufallszahlen-Generator ab.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen.

 

## <a name="syntax"></a>Syntax


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbrandomdata* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die abgerufenen Bytes empfängt.

</dd> <dt>

*cbrandomdata* \[ in\]
</dt> <dd>

Die Anzahl der abzurufenden Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **true** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista mit SP1 \[ Desktop-Apps\]<br/>                                                                                                                                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                                                                                                           |
| DLL<br/>                      | <dl> <dt>Ksecdd.sys unter Windows Server 2008 und Windows Vista mit SP1 </dt> <dt>Cng.sys unter Windows 7 und Windows Server 2008 R2</dt> </dl> |



 

 




