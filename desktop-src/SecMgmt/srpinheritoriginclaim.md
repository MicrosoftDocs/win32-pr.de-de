---
description: Diese Funktion nimmt das Ursprungs Attribut an, wenn es aus dem Ursprungs Token vorhanden ist, und legt Sie auf ein Duplikat des vererbenden Tokens fest und gibt das doppelte Token zurück.
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: srpinvereroriginclaim-Funktion
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
ms.openlocfilehash: 3edf274622bc1a2611bc49d710a809bd80bd501a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348760"
---
# <a name="srpinheritoriginclaim-function"></a>srpinvereroriginclaim-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Diese Funktion nimmt das Ursprungs Attribut an, wenn es aus dem Ursprungs Token vorhanden ist, und legt Sie auf ein Duplikat des vererbenden Tokens fest und gibt das doppelte Token zurück. Der Aufrufer kann dann die Identität des zurückgegebenen Tokens annehmen. Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Sie müssen die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit srpapi.dll zu verknüpfen.

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

*Origintoken* \[ in\]
</dt> <dd>

Handle für das Token, das dupliziert wird und das geerbte Ursprungs Attribut empfängt. Dieses Handle muss mit dem Token für \_ doppelte Zugriffsrechte geöffnet werden.

</dd> <dt>

*Vererbe Token* \[ in\]
</dt> <dd>

Handle für das Token, das dupliziert wird und das geerbte Ursprungs Attribut empfängt. Dieses Handle muss mit dem Token für \_ doppelte Zugriffsrechte geöffnet werden. 

</dd> <dt>

*Resulttoken* 
</dt> <dd>

Bei Erfolg empfängt das duplizierte Token. Der Aufrufer kann ihn annehmen, um Vorgänge mit dem geerbten Ursprungs Attribut auszuführen. Der Aufrufer übernimmt den Besitz dieses Handles und muss ihn schließen. 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Srpapi.dll</dt> </dl> |



 

