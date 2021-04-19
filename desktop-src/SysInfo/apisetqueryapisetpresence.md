---
description: Diese API ist nur für die interne Verwendung vorgesehen und sollte nicht in Ihrem Code verwendet werden.
ms.assetid: 836A7515-8C22-4032-9E99-F89B32C21685
title: Apisetqueryapisetpresence-Funktion (apiquery. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApiSetQueryApiSetPresence
api_type:
- DllExport
api_location:
- api-ms-win-core-apiquery-l1-1-0.dll
- ntdll.dll
ms.openlocfilehash: 738a69b0d08f7e619dbd64229d0c13b2ae7dfaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364260"
---
# <a name="apisetqueryapisetpresence-function"></a>Apisetqueryapisetpresence-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Diese API ist nur für die interne Verwendung vorgesehen und sollte nicht in Ihrem Code verwendet werden.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI ApiSetQueryApiSetPresence(
  _In_  PCUNICODE_STRING Namespace,
  _Out_ PBOOLEAN         Present
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Namespace* \[ in\]
</dt> <dd></dd> <dt>

*Vorhanden* \[ vorgenommen\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                                                                                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                                                                                                                  |
| Header<br/>                   | <dl> <dt>Apiquery. h</dt> </dl>                                                                                                                 |
| Bibliothek<br/>                  | <dl> <dt>API-MS-WIN-Core-apiquery-L1. lib; </dt> <dt>API-MS-WIN-Core-apiquery-L1-1 -0. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt> </dl>                                                                                        |



 

 




