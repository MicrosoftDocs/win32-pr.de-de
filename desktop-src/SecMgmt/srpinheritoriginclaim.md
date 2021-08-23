---
description: Diese Funktion übernimmt das Ursprungsattribut, sofern es aus dem Ursprungstoken vorhanden ist, legt es auf ein Duplikat des erbenden Tokens fest und gibt das doppelte Token zurück.
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: srpInheritOriginClaim-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- srpInheritOriginClaim
api_type:
- DllExport
api_location:
- srpapi.dll
ms.openlocfilehash: 64436c699f5cb24b2a12675342078242a340fb2e53de3a6a8f3224d8b88beac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004887"
---
# <a name="srpinheritoriginclaim-function"></a>srpInheritOriginClaim-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Diese Funktion übernimmt das Ursprungsattribut, sofern es aus dem Ursprungstoken vorhanden ist, legt es auf ein Duplikat des erbenden Tokens fest und gibt das doppelte Token zurück. Der Aufrufer kann dann die Identität des zurückgegebenen Tokens annehmen. Dieser Funktion ist keine Importbibliothek zugeordnet. Sie müssen die [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch mit srpapi.dll zu verknüpfen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI srpInheritOriginClaim(
  _In_ Handle OriginToken,
  _In_ Handle InheritingToken,
       Handle ResultToken
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OriginToken* \[ In\]
</dt> <dd>

Behandeln Sie das Token, das dupliziert wird und das geerbte Ursprungsattribut empfängt. Dieses Handle muss mit dem Zugriffsrecht TOKEN DUPLICATE geöffnet \_ werden.

</dd> <dt>

*InheritingToken* \[ In\]
</dt> <dd>

Behandeln Sie das Token, das dupliziert wird und das geerbte Ursprungsattribut empfängt. Dieses Handle muss mit dem Zugriffsrecht TOKEN DUPLICATE geöffnet \_ werden. 

</dd> <dt>

*ResultToken* 
</dt> <dd>

Bei Erfolg empfängt das duplizierte Token. Der Aufrufer kann die Identität annehmen, um Vorgänge mit dem geerbten Ursprungsattribut auszuführen. Der Aufrufer übernimmt den Besitz dieses Handles und muss es schließen. 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Srpapi.dll</dt> </dl> |



 

